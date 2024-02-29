{
  "date": "2021-05-24",
  "keywords": [
"xul",
"فایل",
"افزونه",
"فرمت فایل",
"فرمت فایل",
"زبان رابط کاربری XML"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL - فایل زبان رابط کاربری XML",
  "description": "درباره فرمت فایل XUL و APIهایی که می‌توانند فایل‌های XUL را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-fal"
}
},
  "lastmod": "2021-05-24"
}

## فایل XUL چیست؟

فایلی با پسوند xul. ([XUL](https://wiki.mozilla.org/XUL:Home_Page) مخفف زبان رابط کاربری XML) یک فایل زبان نشانه گذاری مبتنی بر [XML](/web/xml/) برای ایجاد رابط کاربری است. این توسط موزیلا برای توسعه دهندگان توسعه داده شد تا عناصر رابط کاربری گرافیکی مشابه سایر زبان های نشانه گذاری مورد استفاده برای ایجاد صفحات وب ایجاد کنند. XUL به طور گسترده توسط موزیلا در مرورگر فایرفاکس خود استفاده می‌شود، جایی که از پایگاه کد موزیلا استفاده می‌کرد. رندر XUL با استفاده از
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). فورک های فایرفاکس مانند Pale Moon، Basilisk و Waterfox از افزونه های XUL پشتیبانی می کنند. فایل های XUL با نوع MIME شناسایی می شوند: application/vnd.mozilla.xul+xml.

## فرمت فایل XUL

فایل‌های XUL به صورت متن ساده و بر اساس فرمت فایل XML نوشته می‌شوند و با استفاده از موتور Gecko ارائه می‌شوند. سه بخش اصلی یک ساختار XUL عبارتند از:

 * محتوا - این شامل اعلانات پنجره و عناصر رابط کاربری موجود در آنها می شود.
 * Skin' - شامل هر نوع برگه های سبک، تصاویر و سایر فایل های مرتبط با موضوع است. ظاهر یک پنجره در شیوه نامه ها توضیح داده شده است.
 * محلی - متن نمایش داده شده در یک پنجره به طور جداگانه ذخیره می شود و چندین مجموعه از فایل های زبان می توانند توسط کاربران استفاده شوند.

### مثال XUL

مثال زیر سه دکمه را ایجاد می کند که در جهت عمودی روی هم قرار گرفته اند.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## منابع

* [XUL - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/XUL)

* [اسناد آرشیو شده XUL - توسط موزیلا](https://wiki.mozilla.org/XUL:Home_Page)


