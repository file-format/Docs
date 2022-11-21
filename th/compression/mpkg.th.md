{
  "date" : "2019-10-11",
  "keywords" :[ "ไฟล์ mpkg", "รูปแบบไฟล์ mpkg", "ไฟล์ mpkg คืออะไร", "ไฟล์", "ตัวอย่าง mpkg", "นามสกุลไฟล์ mpkg", "นามสกุล", "รูปแบบ" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"รูปแบบไฟล์ MPKG - ไฟล์แพ็คเกจ Meta",
  "description":"เรียนรู้เกี่ยวกับรูปแบบไฟล์ MPKG และ API ที่สามารถสร้างและเปิดไฟล์ MPKG",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## ไฟล์ MPKG คืออะไร??

ไฟล์ที่มีนามสกุล .mpkg คือไฟล์ตัวติดตั้งที่เก็บถาวรซึ่งส่วนใหญ่พบในระบบปฏิบัติการ MacOS ประกอบด้วยไฟล์การติดตั้งที่จำเป็นทั้งหมดของแอปพลิเคชันโดยไม่จำเป็นต้องแยกไฟล์ที่เกี่ยวข้องออกจากกัน ไฟล์ MPKG ไฟล์เดียวสามารถมีไฟล์แพ็คเกจ [PKG](/th/compression/pkg/) เป็นหนึ่งในไฟล์ติดตั้งเพิ่มเติมจากไฟล์อื่นๆ ไม่สามารถเปิดไฟล์ MPKG ด้วยซอฟต์แวร์ทั่วไปได้ และจะดำเนินการโดยอัตโนมัติบน MacOS โดยใช้ Apple Installer

## รูปแบบไฟล์ MPKG

ไฟล์ MPKG ประกอบด้วยไฟล์ประเภทต่างๆ ที่จำเป็นสำหรับการติดตั้งแพ็คเกจต่างๆ สามารถดูได้จากภาพด้านล่างซึ่งเป็นโครงสร้างแบบต้นไม้ของไฟล์ MPKG ตัวอย่าง โครงสร้างแบบต้นไม้นี้ส่งออกโดยใช้คำสั่ง `tree` บนเทอร์มินัล MacOS

{{< figure src="../mpkg.png" alt="รูปแบบไฟล์ MPKG" >}}

คำอธิบายองค์ประกอบต่าง ๆ ในภาพมีดังนี้

`Packages Directory` - เก็บรายการไฟล์ pkg นั่นคือรายการของแพ็คเกจย่อย
`Resources Directory` - จัดเก็บทรัพยากรที่ใช้โดย pkg เช่น ทรัพยากรและรูปภาพที่แปลเป็นภาษาท้องถิ่น เอกสาร Rtf เอกสาร pdf เป็นต้น
`ไฟล์ Distribution.dist` - เอกสาร xml ที่มีข้อมูล เช่น แพ็คเกจย่อยที่จะติดตั้งและสคริปต์รันไทม์

ไฟล์ XML ตัวอย่างสำหรับไฟล์ MPKG สามารถมีลักษณะดังต่อไปนี้ขึ้นอยู่กับแพ็คเกจย่อยที่เกี่ยวข้อง

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>,
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/th/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - เป็นแพ็คเกจย่อยที่จะติดตั้ง เป็นไดเร็กทอรีของโครงสร้าง Bundle ในรูปแบบ pkg ประกอบด้วยไดเร็กทอรีย่อยของ Contents

## อ้างอิง

* [แพ็คเกจ OSX Flat](https://matthew-brett.github.io/docosx/flat_packages.html)
* [ตัวจัดการแพ็คเกจ C++ MPKG](https://github.com/puellavulnerata/mpkg)

