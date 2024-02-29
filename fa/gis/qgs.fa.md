{
  "date": "2019-10-11",
  "keywords": [
"فایل qgs",
"فرمت فایل qgs",
"فایل qgs چیست",
"فایل",
"مثال qgs",
"پسوند فایل qgs",
"افزونه",
"قالب"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "QGS - قالب فایل پروژه QGIS",
  "description": "درباره فرمت فایل QGS و APIهایی که می‌توانند فایل‌های QGS را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "QGS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-fas"
}
}،
  "lastmod": "2019-09-10"
}

## فایل QGS چیست؟

A file with .qgs extension is a project file created with [QGIS](https://www.qgis.org/en/site/), which is an open-source cross-platform GIS application. All the project settings such as layer properties and auxiliary data for the project. It is created when a map project is saved to disc. It is actually a configuration file that retains information such as pointers to the GIS data, styling information about the layers, and project title. QGS files can be opened with QGIS software that is freely available to download.

## فرمت فایل QGS

فایل‌های QGS در قالب [XML](/web/xml/) هستند و داده‌های پروژه را به‌عنوان تگ XML ذخیره می‌کنند. یک فایل QGS حاوی اطلاعاتی از قبیل:

 * عنوان پروژه
 * پروژه CRS
 * درخت لایه
 * تنظیمات snapping
 * روابط
 * وسعت بوم نقشه
 * مدل های پروژه
 * افسانه
 * اسکله های مپ ویو (دو بعدی و سه بعدی)
 * لایه هایی با پیوندهایی به مجموعه داده های زیرین (منابع داده) و سایر ویژگی های لایه از جمله میزان، SRS، اتصال، استایل ها، رندر، حالت ترکیبی، کدورت و موارد دیگر.
 * خواص پروژه

### برچسب های XML سطح بالای QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### تگ های لایه پروژه سطح بالا توسعه یافته

{{< figure src="../qgstoplevel.png" title="" >}}

## منابع

* [QGIS](https://www.qgis.org/en/site/)


