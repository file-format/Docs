{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XAR - فرمت فایل بایگانی قابل توسعه",
  "description":"درباره فرمت فایل XAR و APIهایی که می‌توانند فایل‌های XAR را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar-fa",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-13"
}

## فایل XAR چیست؟

فایلی با پسوند xar (فرمت بایگانی توسعه پذیر) یک بایگانی یونیکس است که ممکن است در فرمت فشرده یا غیر فشرده باشد. همچنین در سیستم عامل مک برای نصب بسته ها استفاده می شود. XAR منبع باز است و بخشی از Mac OS X 10.5 برای استفاده با مرورگر Safari است.

## فرمت فایل XAR

یک فایل [XAR](https://github.com/mackyle/xar/wiki/xarformat) دارای سه منطقه اصلی است.

 * سرتیتر
 * فهرست مطالب
 * پشته

### سربرگ XAR

هدر XAR به شکل زیر ساخته شده است.

|فیلد|نوع داده|اندازه بر حسب بایت|
---|---|---|
|Magic|Int بدون امضا 32|4|
|سایز|Int بدون امضا 16|2|
|نسخه|Int بدون امضا 16|2|
|طول TOC فشرده|Int بدون علامت 64|8|
|طول TOC فشرده نشده|Int بدون علامت 64|8|
|Checksum|Int بدون امضا 32|4|
|نام خلاصه پیام |Null Terminated||

ساختار C هدر XAR را می توان به صورت زیر تعریف کرد.
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
توجه داشته باشید که تمام فیلدهای هدر (جادو، اندازه، نسخه، toc_length_compressed، toc_length_uncompressed، cksum_alg) همیشه در فایل‌های XAR به ترتیب بایت شبکه (معروف به big endian) ذخیره می‌شوند.

### فهرست مطالب XAR (TOC)

The table of contents is an XML document that is (and must) be encoded as UTF-8. در ابتدای فایل ذخیره می‌شود و اسکن کردن بایگانی برای استخراج فایل‌های جداگانه را آسان می‌کند. بایگانی XAR به شما امکان می‌دهد فایل‌های جداگانه موجود در بایگانی را به طور مستقل با استفاده از طرح‌های فشرده‌سازی مختلف مانند [GZIP](/compression/gz/)، [BZIP2](/compression/bz2/) و موارد مشابه فشرده یا رمزگذاری کنید.  

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

### پشته

هپ بلافاصله پس از فشرده سازی شروع می شود. این یک پشته بدون ساختار از داده است که توسط TOC ارجاع شده است. مقادیر Offset فهرست شده در TOC از ابتدای پشته شروع می شود. مقادیر طول در toc به تعداد واقعی بایت‌های ذخیره شده در پشته (فشرده یا غیرفشرده) اشاره دارد، در حالی که مقدار اندازه به اندازه استخراج شده از آیتم (پس از خارج کردن فشرده در صورت لزوم) اشاره دارد.

## منابع

* [XAR](https://github.com/mackyle/xar/wiki/xarformat)

* [XAR - Wikipedia](https://en.wikipedia.org/wiki/Xar_(archiver))


