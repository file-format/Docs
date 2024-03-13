{
  "date": "2019-10-11",
  "keywords": [
"odp faylı",
"odp fayl formatı",
"odp faylı nədir",
"fayl",
"odp nümunəsi",
"odp fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODP - OpenOffice Təqdimat Fayl Formatı",
  "description": "ODP faylları yarada və aça bilən ODP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "ODP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-od-azp"
}
},
  "lastmod": "2019-09-10"
}

## ODP faylı nədir?

.odp uzantılı fayllar OpenOffice.org tərəfindən OASISOpen standartında istifadə olunan təqdimat faylı formatını təmsil edir. Təqdimat faylı hər bir slaydın mətn, şəkillər, formatlaşdırma, animasiyalar və digər mediadan ibarət ola biləcəyi slaydlar toplusudur. Bu slaydlar xüsusi təqdimat parametrləri ilə slayd şouları şəklində tamaşaçılara təqdim olunur. ODP faylları OpenDocument formatına (OpenOffice və ya StarOffice kimi) uyğun gələn proqramlar tərəfindən açıla bilər.

## Qısa tarix

ODP fayl formatının spesifikasiyası ODF spesifikasiyası kimi hazırlanmış standarta əsaslanır. Bu spesifikasiyalar keçmişdə aşağıdakı kimi OASIS tərəfindən hazırlanmış və nəşr edilmiş üç versiya şəklində inkişaf etmişdir:

`2005` - Versiya 1.0 2005-ci ilin may ayında nəşr edilmişdir
`2007` - Versiya 1.1 2007-ci ilin fevralında nəşr edilib
`2011` - Versiya 1.2 2011-ci ilin sentyabrında nəşr edilib

ODF 1.0-dan 1.1 versiyalarına keçiddə olduqca kiçik dəyişikliklər oldu. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) ODF spesifikasiyaları üçün ən son versiyadır və ODS oxuması/yazması ilə bağlı proqramların hazırlanması üçün tərtibatçılar tərəfindən məsləhətləşməlidir.

## Fayl Formatının Xüsusiyyətləri

OpenDocument formatı, [ZIP](/compression/zip/) arxivi kimi paket daxilində bir neçə subsənəd toplusu ilə yanaşı, tək XML sənədi kimi sənəd təqdimatını dəstəkləyir. ZIP arxivindəki faylların hər biri tam sənədin bir hissəsini saxlayır. Hər bir alt sənəd sənədin müəyyən bir tərəfini saxlayır. Məsələn, bir alt sənəddə stil məlumatı, digər alt sənəddə isə sənədin məzmunu var. Tipik bir ODF sənədi aşağıdakı komponentlərə malikdir:

* `content.xml` – Sənəd məzmunu və məzmunda istifadə olunan avtomatik üslublar.

* `styles.xml` – Sənədin məzmununda istifadə olunan üslublar və üslubların özlərində istifadə olunan avtomatik üslublar.

* `meta.xml` – Müəllif və ya son saxlama əməliyyatının vaxtı kimi sənəd meta məlumatı.

* `settings.xml` – Pəncərə ölçüsü və ya printer məlumatı kimi proqrama xas parametrlər.


Bunlardan əlavə, paketdə sənədin eskizləri, şəkillər və s. kimi bir çox digər alt sənədlər ola bilər.

Elektron cədvəl sənəd faylları məzmunun (vərəqlərin) content.xml alt sənədində saxlandığı ODF fayllarının alt çoxluğudur.

## İstinadlar

* [OpenDocument - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/OpenDocument)


