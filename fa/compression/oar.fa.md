{
  "date": "2021-04-08",
  "keywords": [
"فایل oar",
"فرمت فایل oar",
"فایل oar چیست",
"فایل",
"نمونه پارو",
"پسوند فایل oar",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR - فرمت فایل بایگانی OpenSimulator",
  "description": "درباره فرمت فایل OAR و API هایی که می توانند فایل های OAR ایجاد و باز کنند، بیاموزید.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-far"
}
},
  "lastmod": "2021-04-15"
}

## فایل OAR چیست؟

یک فایل با پسوند .oar یک فایل بایگانی است که توسط برنامه OpenSimulator استفاده می شود که یک سرور برنامه سه بعدی منبع باز برای ایجاد یک محیط مجازی قابل دسترسی برای چند کاربر از طریق شبکه است. فرمت فایل OAR داده‌های دارایی لازم را برای بارگیری کامل زمین، بافت‌های شی و موجودی‌ها در یک سیستم متفاوت فراهم می‌کند. OpenSimulator همچنین دارای هایپرشبکه اختیاری است که به کاربران امکان می دهد از سایر نصب های OpenSimulator در سراسر وب بازدید کنند. فایل‌های OAR دارای برنامه/oar نوع MIME اینترنتی هستند و حاوی یک یا چند فایل بایگانی شده هستند.


## فرمت فایل OAR

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. یک فایل OAR یک فایل tar.gz (tar.gz) با فرمت اصلی یونیکس tar (نه USTAR) است.

## نمونه مناطق OAR
فایل های AOR می توانند شامل چندین منطقه باشند. ساختار آرشیو به شرح زیر است (این مثال شامل 4 منطقه است):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

فایل کنترل بایگانی حاوی یک شماره نسخه اصلی برای تعریف سازگاری با تغییرات قالب آینده است. وجود دارایی ها در قالب OAR با عنصر بولی نشان داده می شود<assets_included> . اطلاعات مربوط به مناطق گنجانده شده در مانیفست موجود در فایل کنترل موجود است. نمونه ای از Archive.xml به شرح زیر است.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## منابع

 * [فرمت OAR نسخه 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

