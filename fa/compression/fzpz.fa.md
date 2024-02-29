{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل FZPZ - فایل قسمت Fritzing",
  "description": "درباره اینکه فایل FZPZ چیست و APIهایی که می توانند فایل های FZPZ را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-faz"
}
}،
  "lastmod": "2022-06-20"
}

## فایل FZPZ چیست؟

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## فرمت فایل FZPZ - اطلاعات بیشتر

فایل‌های FZPZ به عنوان بایگانی‌های فشرده شده [ZIP](/compression/zip/) در دیسک ذخیره می‌شوند. می توانید نام پسوند را از fzpz. به .zip تغییر دهید و از هر ابزار استاندارد رفع فشرده سازی مانند WinZIP برای استخراج فایل ها از بایگانی استفاده کنید.

### اطلاعات ساختار فایل FZPZ

همانطور که گفته شد، یک فایل FZPZ یک فایل بایگانی است که حاوی چندین فایل برای نمایش بخشی مورد استفاده در برد مدار چاپی است. FZPZ حاوی فایل های زیر است:

 * چهار فایل SVG - که نمایانگر تخته نان، شماتیک، PCB و تصاویر نماد قطعه است.
 * «فایل FZP» - یک فایل XML که حاوی اطلاعاتی در مورد ویژگی‌های قطعه، رابط‌ها و گذرگاه‌ها است

فایل ها معمولا به صورت زیر نام گذاری می شوند.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## منابع ##

* [قطعات جدید با پسوند fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


