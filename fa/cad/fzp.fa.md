{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "درباره فرمت فایل FZP و API هایی که می توانند فایل های FZP را ایجاد و باز کنند، بیاموزید.",
  "title": "فرمت فایل FZP - فایل توضیحات قسمت Fritzing XML",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-fap"
}
}،
  "lastmod": "2022-06-20"
}

## فایل FZP چیست؟

یک فایل FZP یک فایل XML است که توسط برنامه نمونه‌سازی و طراحی مدار الکترونیکی [Fritzing](https://fritzing.org/) ایجاد شده است. این شامل اطلاعاتی در مورد ویژگی‌های قطعه، رابط‌ها و گذرگاه‌ها در قالب فایل [XML](/web/xml/) است. فایل های FPZ را نمی توان به طور مستقل در Fritzing استفاده کرد. در عوض، آنها به عنوان بخشی از فایل آرشیو FZPZ وارد می شوند.

## فرمت فایل FZP - اطلاعات بیشتر

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## مثال ساختار فایل FZP

یک فایل FZP معمولی دارای ساختار XML زیر است.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## منابع

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [قطعات جدید با پسوند fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


