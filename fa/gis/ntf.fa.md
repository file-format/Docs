{
  "date": "2021-07-28",
  "keywords": [
"فایل ntf",
"فرمت فایل ntf",
"فایل ntf چیست",
"فایل",
"مثال ntf",
"پسوند فایل ntf",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF - فایل های فرمت انتقال ملی",
  "description": "درباره فرمت فایل NTF و APIهایی که می توانند فایل های NTF ایجاد و باز کنند، بیاموزید.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-faf"
}
},
  "lastmod": "2021-07-28"
}

## فایل NTF چیست؟
فایل های با پسوند ntf. ** فرمت انتقال ملی (NTF) ** فایل ها نامیده می شوند. بیشتر توسط بررسی مهمات بریتانیا (OS) استفاده می شود. به طور خاص برای انتقال داده های مکانی. توسط موسسه استاندارد بریتانیا اداره می شود. این فرمت استاندارد انتقال داده های دیجیتال Ordnance Survey شده است. طرح شبکه ملی بریتانیا، که نوعی مرکاتور عرضی است، تمام اطلاعات جغرافیایی مرجع برای فایل‌های NTF را در خود نگه می‌دارد.

## فرمت فایل NTF
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. این فرمت فایل برای رفع محدودیت بخش برداری **PCIDSK** معرفی شد که تنها یک فیلد مشخصه در هر ساختار دارد، اما ویژگی های مختلفی وجود دارد که می توان با داده های برداری استخراج کرد. برای دور زدن فرمت فایل NTF دارای دو بخش است. هر بخش از بردارهای یکسان، اما با ویژگی های متفاوت تشکیل شده است. اولین بخش از یک فایل برداری NTF شامل بردارهایی با شماره کد ویژگی به عنوان ویژگی است. بخش دوم شامل بردارهایی با مقدار به عنوان ویژگی است.

### سیستم ارجاع مختصات
کتابخانه GDB داده های شطرنجی و برداری را با ویژگی های طرح ریزی TM مناسب نشان می دهد:

- طول مرجع: 49.0
- عرض جغرافیایی مرجع: 2.0
- مشرق کاذب: 400000
- شمال کاذب: -100000
- مقیاس: 0.9996012717
- Ellipsoid: Airy 1830 (E009)
هیچ پشتیبانی برای به‌روزرسانی یا نوشتن فایل‌های NTF در دسترس نیست، و همچنین نمی‌توان فایل‌های DTM را به آن‌ها پیوند داد.

### مثال Ogrinfo
مثال زیر از **ogrinfo** در یک فایل NTF برای بازیابی اعداد لایه استفاده می کند:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## منابع

* [فرمت انتقال ملی بریتانیا (NTF)] (https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [نقشه برداری وب - تصویر شده توسط تایلر میچل](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


