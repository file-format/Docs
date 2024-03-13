{
  "date": "2019-10-11",
  "keywords": [
"ott faylı",
"ott fayl formatı",
"ott faylı nədir",
"fayl",
"misal",
"ott fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTT - OpenDocument Şablon Faylı",
  "description": "OTT fayl formatı və OTT faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OTT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-ot-azt"
}
},
  "lastmod": "2019-09-10"
}

## OTT faylı nədir?

OTT genişləndirilməsi olan fayllar OASIS-in OpenDocument standart formatına uyğun olaraq tətbiqlər tərəfindən yaradılan şablon sənədləri təmsil edir. Bunlar pulsuz OpenOffice Writer kimi mətn prosessoru proqramları ilə yaradılmışdır və bu şablon fayllarından yeni sənədlər yaratmaq üçün istifadə edilə bilən parametrləri saxlaya bilər. Bu parametrlərə səhifə kənarları, sərhədlər, başlıqlar, altbilgilər və digər səhifə parametrləri daxildir. Bu cür şablonlar şirkət blankları və standart formalar kimi rəsmi sənədlərdə istifadə olunur.

## Qısa tarix ##

ODP fayl formatının spesifikasiyası ODF spesifikasiyası kimi hazırlanmış standarta əsaslanır. Bu spesifikasiyalar keçmişdə aşağıdakı kimi OASIS tərəfindən hazırlanmış və nəşr edilmiş üç versiya şəklində inkişaf etmişdir:

**2005:** Versiya 1.0 2005-ci ilin may ayında nəşr edilmişdir

**2007:** Versiya 1.1 2007-ci ilin fevralında nəşr edilmişdir

**2011:** Versiya 1.2 2011-ci ilin sentyabrında nəşr edilib

ODF 1.0-dan 1.1 versiyalarına keçiddə olduqca kiçik dəyişikliklər oldu. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) ODF spesifikasiyaları üçün ən son versiyadır və ODS oxuması/yazması ilə bağlı proqramların hazırlanması üçün tərtibatçılar tərəfindən məsləhətləşməlidir.

## Fayl Formatının Xüsusiyyətləri

OpenDocument formatı, [ZIP](/compression/zip/) arxivi kimi paket daxilində bir neçə subsənəd toplusu ilə yanaşı, tək XML sənədi kimi sənəd təqdimatını dəstəkləyir. ZIP arxivindəki faylların hər biri tam sənədin bir hissəsini saxlayır. Hər bir alt sənəd sənədin müəyyən bir tərəfini saxlayır. Məsələn, bir alt sənəddə stil məlumatı, digər alt sənəddə isə sənədin məzmunu var. Tipik bir ODF sənədi aşağıdakı komponentlərə malikdir:

* content.xml – Sənəd məzmunu və məzmunda istifadə olunan avtomatik üslublar.

* styles.xml – Sənəd məzmununda istifadə olunan üslublar və üslubların özlərində istifadə olunan avtomatik üslublar.

* meta.xml – Müəllif və ya sonuncu saxlama əməliyyatının vaxtı kimi sənəd meta məlumatı.

* settings.xml – Pəncərə ölçüsü və ya printer məlumatı kimi proqrama xas parametrlər.


Bunlardan başqa, paketdə sənədin miniatürü, şəkillər və s. kimi bir çox digər subsənədlər ola bilər. Sənəd faylları məzmunun (vərəqlərin) //content.xml// alt sənədində saxlandığı ODF fayllarının alt çoxluğudur.

## İstinadlar ##

* [OpenDocument - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/OpenDocument)


