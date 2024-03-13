{
  "date": "2019-12-10",
  "keywords": [
"ODS",
"fayl",
"uzadılması",
"fayl formatı",
"OpenDocument elektron cədvəli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "ODS faylının və onları yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "ODS faylı nədir? ",
  "linktitle": "ODS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-od-azs"
}
},
  "lastmod": "2019-12-10"
}

## ODS faylı nədir?

.ods uzadılması olan fayllar istifadəçi tərəfindən redaktə edilə bilən OpenDocument Cədvəl Sənədi formatı üçün nəzərdə tutulub. Məlumatlar ODF faylında sətir və sütunlarda saxlanılır. O, XML əsaslı formatdır və Açıq Sənəd Formatları (ODF) ailəsindəki bir neçə alt növdən biridir. Format OASIS tərəfindən dərc edilmiş və saxlanılan ODF 1.2 spesifikasiyalarının bir hissəsi kimi müəyyən edilmişdir. Windows və digər əməliyyat sistemlərindəki bir sıra proqramlar Microsoft Excel, NeoOffice və LibreOffice daxil olmaqla redaktə və manipulyasiya üçün ODS fayllarını aça bilər. ODS faylları müxtəlif proqramlar vasitəsilə [XLS](/spreadsheet/xls/), [XLSX](/spreadsheet/xlsx/) və başqaları kimi digər cədvəl formatlarına da çevrilə bilər.

## Qısa tarix ##

ODS fayl formatının spesifikasiyası ODF spesifikasiyası kimi hazırlanmış standarta əsaslanır. Bu spesifikasiyalar keçmişdə aşağıdakı kimi OASIS tərəfindən hazırlanmış və nəşr edilmiş üç versiya şəklində inkişaf etmişdir:

`2005`- Versiya 1.0 2005-ci ilin may ayında nəşr edilmişdir

`2007` - Versiya 1.1 2007-ci ilin fevralında nəşr edilib

`2011` - Versiya 1.2 2011-ci ilin sentyabrında nəşr edilib

ODF 1.0-dan 1.1 versiyalarına keçiddə olduqca kiçik dəyişikliklər oldu. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) ODF spesifikasiyaları üçün ən son versiyadır və ODS oxuması/yazması ilə bağlı proqramların hazırlanması üçün tərtibatçılar tərəfindən məsləhətləşməlidir.

## ODS Fayl Format ##

OpenDocument formatı, [ZIP](/compression/zip/) arxivi kimi paket daxilində bir neçə subsənəd toplusu ilə yanaşı, tək XML sənədi kimi sənəd təqdimatını dəstəkləyir. ZIP arxivindəki faylların hər biri tam sənədin bir hissəsini saxlayır. Hər bir alt sənəd sənədin müəyyən bir tərəfini saxlayır. Məsələn, bir alt sənəddə stil məlumatı, digər alt sənəddə isə sənədin məzmunu var. Tipik bir ODF sənədi aşağıdakı komponentlərə malikdir:

* `content.xml` – Sənəd məzmunu və məzmunda istifadə olunan avtomatik üslublar.

* `styles.xml` – Sənədin məzmununda istifadə olunan üslublar və üslubların özlərində istifadə olunan avtomatik üslublar.

* `meta.xml` – Müəllif və ya son saxlama əməliyyatının vaxtı kimi sənəd meta məlumatı.

* `settings.xml` – Pəncərə ölçüsü və ya printer məlumatı kimi proqrama xas parametrlər.


Bunlardan əlavə, paketdə sənədin eskizləri, şəkillər və s. kimi bir çox digər alt sənədlər ola bilər.

Elektron cədvəl sənəd faylları məzmunun (vərəqlərin) content.xml alt sənədində saxlandığı ODF fayllarının alt çoxluğudur.

## İstinadlar ##

* [OpenDocument - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/OpenDocument)


