{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"fayl",
"uzadılması",
"fayl formatı",
"Excel",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "OTS fayl formatı və OTS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "OTS - OpenDocument Spreadsheet Şablon Fayl Format",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-azs"
}
},
  "lastmod": "2021-01-19"
}

## OTS faylı nədir?

.ots genişləndirilməsi olan fayl Apache OpenOffice-ə daxil olan Calc tətbiqi proqramı ilə yaradılmış OpenDocument Cədvəl Şablonu faylıdır. Calc tətbiqi proqramı Microsoft Office-də mövcud olan Excel proqramına bənzəyir. OTS fayl formatı üslublar, şriftlər, məlumatlar, cədvəl tərtibatı və formatlaşdırma ilə bağlı əvvəlcədən təyin edilmiş parametrləri ehtiva edən şablonlar yaratmaq üçün istifadə olunur. OTF fayllarında `mime tipli proqram/vnd.oasis.opendocument.spreadsheet-template` var. Bu şablon faylları [ODS file format](/spreadsheet/ods/)-də saxlanılan faktiki data fayllarını yaratmaq və saxlamaq üçün başlanğıc nöqtəsi kimi istifadə edilə bilər. OTS faylları OpenOffice və LibreOffice kimi proqramlarla istifadə edilə bilər.

## OTS fayl formatı

OTS faylları [ZIP](/compression/zip/) arxivi kimi paketi olan bir neçə subsənədlər toplusundan ibarət OASIS-in OpenDocument XML əsaslı fayl formatında saxlanılır. Hər bir zip arxivi tam sənədin bir hissəsini saxlayır və hər bir alt sənəd sənədin müəyyən bir tərəfini saxlayır. Məsələn, bir alt sənəddə stil məlumatı, digər alt sənəddə isə sənədin məzmunu var. Tipik bir ODF sənədi aşağıdakı komponentlərə malikdir:

### OTS Content.xml

content.xml faylı sənədin faktiki məzmununu ehtiva edir. Buna baxmayaraq, şəkillər kimi ikili data daxil deyil.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS Fayl Formatının Styles.xml

styles.xml faylı üslub məlumatlarını ehtiva edir və formatlaşdırma və tərtibat üçün çox istifadə olunur. Stil növlərinə aşağıdakılar daxildir:

 * Paraqraf üslubları
 * Səhifə üslubları
 * Xarakter üslubları
 * Çərçivə üslubları
 * Üslubların siyahısı

### Meta.xml

Meta.xml faylında Müəllif, Son Dəyişiklik Tarixi və s. kimi fayl metaməlumatları haqqında məlumat var.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

`settings.xml` faylına böyütmə faktoru və kursor mövqeyi kimi sənəd səviyyəsi parametrləri daxildir.

## İstinadlar ##

* [OpenDocument 1.2 spesifikasiyası](https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/OpenDocument)


