{
  "date": "2019-10-11",
  "keywords": [
"amf",
"فایل amf",
"فرمت فایل amf",
"فرمت فایل",
"3 بعدی"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل AMF و APIهایی که می‌توانند فایل‌های AMF را باز کرده و ایجاد کنند، بیاموزید.",
  "title": "AMF - فایل ساخت افزودنی",
  "linktitle": "AMF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-am-faf"
}
},
  "lastmod": "2019-09-10"
}

## فایل AMF چیست؟
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## فرمت فایل AMF

Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.

### عناصر یک فایل AMF

پنج عنصر سطح بالای تعریف شده با<AMF> برچسب ها به شرح زیر است. وجود یک عنصر شی منفرد برای یک فایل AMF کاملاً کاربردی ضروری است.

`<object> ` - عنصر شی حجم یا حجم هایی از مواد را تعریف می کند که هر کدام با یک شناسه ماده برای چاپ مرتبط هستند. حداقل یک عنصر شی باید در فایل موجود باشد. اشیاء اضافی اختیاری هستند.

`<material> ` - عنصر ماده اختیاری یک یا چند ماده را برای چاپ با شناسه مواد مرتبط تعریف می کند. اگر هیچ عنصر مادی گنجانده نشده باشد، یک ماده پیش فرض واحد فرض می شود.

`<texture> ` - عنصر بافت اختیاری یک یا چند تصویر یا بافت را برای نگاشت رنگ یا بافت تعریف می کند که هر کدام دارای شناسه بافت مرتبط هستند.

`<constellation> - عنصر صورت فلکی اختیاری به صورت سلسله مراتبی اجسام و سایر صورت های فلکی را در یک الگوی نسبی برای چاپ ترکیب می کند.

`<metadata> ` - عنصر فراداده اختیاری اطلاعات اضافی در مورد شی(ها) و عناصر موجود در فایل را مشخص می کند.

## مثال AMF

در زیر نمونه ای از فایل AMF آورده شده است که می توان آن را در یک فایل [text](/word-processing/txt/) کپی کرد و به عنوان فایل فشرده شده [zip](/compression/zip/) برای باز کردن ذخیره کرد.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## منابع

 * [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [مشخصات AMF در ISO](https://www.iso.org/standard/67472.html)

