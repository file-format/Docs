{
  "date": "2021-05-24",
  "keywords": [
"zul",
"فایل",
"افزونه",
"فرمت فایل",
"فرمت فایل",
"باز کن"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "فایل رابط کاربری ZUL - ZK",
  "description": "درباره فرمت فایل ZUL و APIهایی که می‌توانند فایل‌های ZUL را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "ZUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-zu-fal"
}
},
  "lastmod": "2021-05-24"
}

## فایل ZUL چیست؟

یک فایل با پسوند .zul یک فایل وب است که با زبان نشانه گذاری رابط کاربری (ZUML) ایجاد شده است و شامل تعاریفی برای عناصر رابط کاربری است. کلاس‌های Ajax و Java از ZUML مبتنی بر [XML](/web/xml/) برای توسعه فایل‌های سمت سرور پشتیبانی می‌کنند. فرمت فایل ZUL توسط ZK توسعه داده شده است، یک چارچوب UI که به شما امکان می دهد بدون دانش جاوا اسکریپت یا AJAX برنامه های وب و موبایل بسازید.

## فرمت فایل ZUL

ZUL files are XML-based, consisting of different elements to construct user interface. The ZK loader uses each XML element to create a component. The overall processing of the page elements such as page title, description, etc. are described by each XML processing instruction of ZUML.

### مثال ZUL

در مثال زیر از کد ZUML، خط اول عنوان صفحه را مشخص می کند، خط دوم یک جزء ریشه با عنوان و حاشیه ایجاد می کند، و خط سوم یک دکمه با برچسب و یک شنونده رویداد ایجاد می کند.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
طرح ZUL را می توان از https://www.zkoss.org/2005/zul/zul.xsd دانلود کرد.
## منابع

* [ZUL - توسط ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)

* [شما ZUL] (https://www.zkoss.org/2005/zul/zul.xsd)


