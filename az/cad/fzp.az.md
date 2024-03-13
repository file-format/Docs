{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "FZP faylları yarada və aça bilən FZP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "FZP Fayl Format - Fritzing XML Part Təsvir Fayl",
  "linktitle": "FZP",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-fz-azp"
}
},
  "lastmod": "2022-06-20"
}

## FZP faylı nədir?

FZP faylı [Fritzing](https://fritzing.org/) elektron dövrə prototipi və dizayn tətbiqi tərəfindən yaradılmış XML faylıdır. O, [XML](/web/xml/) fayl formatında hissənin xassələri, birləşdiriciləri və avtobusları haqqında məlumatları ehtiva edir. FPZ faylları Fritzing-də müstəqil olaraq istifadə edilə bilməz. Bunun əvəzinə, onlar FZPZ arxiv faylının bir hissəsi kimi idxal edilir.

## FZP Fayl Format - Ətraflı Məlumat

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/page-description-language/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## FZP fayl strukturu nümunəsi

Tipik bir FZP faylı aşağıdakı XML strukturuna malikdir.

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
## İstinadlar

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Fzpz uzantılı yeni hissələr](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


