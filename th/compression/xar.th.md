{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - รูปแบบไฟล์เก็บถาวรที่ขยายได้",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ XAR และ API ที่สามารถสร้างและเปิดไฟล์ XAR",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## ไฟล์ XAR คืออะไร??

ไฟล์ที่มีนามสกุล .xar (Extensible Archive Format) คือไฟล์เก็บถาวร UNIX ที่อาจอยู่ในรูปแบบที่บีบอัดหรือไม่บีบอัด นอกจากนี้ยังใช้บน Mac OS สำหรับการติดตั้งแพ็คเกจ XAR เป็นโอเพ่นซอร์สและเป็นส่วนหนึ่งของ Mac OS X 10.5 สำหรับการใช้งานกับเบราว์เซอร์ Safari

## รูปแบบไฟล์ XAR

ไฟล์ [XAR](https://github.com/mackyle/xar/wiki/xarformat) มีสามขอบเขตหลัก

* หัวข้อ
* สารบัญ
* กอง

### ส่วนหัว XAR

ส่วนหัว XAR มีโครงสร้างดังนี้

|ฟิลด์|ชนิดข้อมูล|ขนาดเป็นไบต์|
---|---|---|
|มายากล|Unsigned Int 32|4|
|ขนาด|Unsigned Int 16|2|
|เวอร์ชัน|Unsigned Int 16|2|
|บีบอัดความยาว TOC|Int ที่ไม่ได้ลงชื่อ 64|8|
|ความยาว TOC ไม่บีบอัด|Int ที่ไม่ได้ลงชื่อ 64|8|
|Checksum|Unsigned Int 32|4|
|ชื่อสรุปข้อความ |Null ถูกยกเลิก||

สามารถกำหนดโครงสร้าง C ของ XAR header ได้ดังนี้
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
โปรดทราบว่าฟิลด์ทั้งหมดของส่วนหัว (magic, size, version, toc_length_compressed, toc_length_uncompressed, cksum_alg) จะถูกจัดเก็บไว้ในไฟล์ XAR ตามลำดับไบต์เครือข่าย (หรือที่เรียกว่า big endian) เสมอ

### สารบัญ XAR (TOC)

สารบัญเป็นเอกสาร XML ที่เข้ารหัส (และต้อง) เป็น UTF-8 มันถูกเก็บไว้ที่ส่วนต้นของไฟล์ ทำให้ง่ายต่อการสแกนผ่านไฟล์เก็บถาวรเพื่อแยกไฟล์แต่ละไฟล์ ไฟล์เก็บถาวร XAR ให้คุณบีบอัด/เข้ารหัสไฟล์แต่ละไฟล์ในไฟล์เก็บถาวรโดยอิสระโดยใช้รูปแบบการบีบอัดต่างๆ เช่น [GZIP](/th/compression/gz/), [BZIP2](/th/compression/bz2/) และอื่นๆ ที่คล้ายกัน

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

###กอง

ฮีปเริ่มต้นทันทีหลังจากบีบอัด toc เป็นกองข้อมูลที่ไม่มีโครงสร้างซึ่งอ้างอิงโดย TOC ค่าออฟเซ็ตที่แสดงใน TOC เริ่มต้นจากจุดเริ่มต้นของฮีป ค่าความยาวใน toc อ้างอิงถึงจำนวนไบต์จริงที่จัดเก็บไว้ในฮีป (บีบอัดหรือไม่ก็ตาม) ในขณะที่ค่าขนาดอ้างอิงถึงขนาดที่แยกออกมาของรายการ (หลังจากคลายการบีบอัดหากจำเป็น)

## อ้างอิง

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))

