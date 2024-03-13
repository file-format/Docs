{
  "date": "2019-10-11",
  "keywords": [
"osm faylı",
"osm faylı nədir",
"fayl",
"osm nümunəsi",
"osm fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OSM - OpenStreetMap Fayl Formatı",
  "description": "OSM faylları yarada və aça bilən OSM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-os-azm"
}
},
  "lastmod": "2019-09-10"
}

## OSM faylı nədir?

OpenStreetMap (OSM) bu məlumatları bitlərə və baytlara çevirmək üçün müxtəlif kodlaşdırma sxemlərindən istifadə edərək, müxtəlif növ fayllarda könüllü olaraq yaradılmış coğrafi məlumat anbarlarının böyük toplusudur. OSM dünyanın pulsuz redaktə edilə bilən xəritəsinin yaradılması istiqamətində birgə səydir. Bu birgə səyin əsas nəticəsi xəritənin özündən çox coğrafi məlumatlardır. Dünyanın əksər hissəsində coğrafi məlumatın istifadəsi və ya mövcudluğu ilə bağlı məhdudiyyətlər OSM yaratmaq ehtiyacını doğurur.

OSM-dən əldə edilən məlumatlar klassik proqramlar (Facebook, Craigslist və s.) üçün Google Xəritələri və GPS qəbuledicilərinin tətbiqləri üçün defolt verilənləri əvəz etməyə hazırdır. Məlumatların keyfiyyəti bütün dünyada müxtəlif olsa da, OpenStreetMap məlumatları rahatlıqla patent məlumat mənbələri ilə müqayisə edilə bilər.

## OSM Fayl Formatının Qısa Tarixi

2004-cü ildə İngilis sahibkar Stiv Kost Wikipedia-nın uğurundan ilhamlanaraq Böyük Britaniyada bu icma əsaslı dünya xəritəsi layihəsini yaratdı. O, əvvəlcə Birləşmiş Krallığın xəritəsini çəkməyə diqqət yetirdi. OpenStreetMap Fondu ilk dəfə 2006-cı ilin aprelində hər kəs üçün pulsuz coğrafi məkanın təkamülünü, genişlənməsini və dövriyyəsini dəstəkləmək üçün yaradılmışdır. 2006-cı ilin dekabrında Yahoo OpenStreetMap-a xəritə istehsalı üçün hava fotoşəkilləri ilə kömək etdi.

Hollandiya üçün tam yol məlumatları və Hindistan və Çin üçün magistral yol məlumatları 2007-ci ilin aprelində Automotive Navigation Data (AND) tərəfindən OSM-ə təqdim edilmişdir. 2007-ci ilin dekabrında Oksford Universiteti OpenStreetMap məlumatlarını əsas veb-saytına inteqrasiya edən ən görkəmli təşkilat idi. O vaxtdan bəri, 2 milyondan çox qeydiyyatdan keçmiş istifadəçi GPS cihazları, aerofotoqrafiya və əl ilə sorğulardan istifadə edərək bu layihəyə məlumat verir. Bu icmanın töhfə verdiyi məlumatlar Açıq Verilənlər Bazası Lisenziyası altında təqdim olunur. İngiltərədə qeydiyyatdan keçmiş, qeyri-kommersiya təşkilatı OpenStreetMap Fondu OSM saytını qoruyub saxlayırdı.

## OSM Fayl Format

Coğrafi məlumatları saxlamaq üçün bir çox yol və fayl formatları var, lakin **OSM** fayl formatı OpenStreetMap ilə məhdudlaşdırılıb. OSM xüsusilə internet üzərindən asanlıqla daşınmaq üçün nəzərdə tutulmuş standart formatdır. XML-də kodlanmış strukturlaşdırılmış sifarişli format .osm faylını təşkil edir. OpenStreetMap-da topoloji məlumat strukturunu saxlamaq üçün dörd pivot element var:

{{< figure src="../OSM.png" alt="OSM Fayl Format" >}}


|Düyünlər|Yollar|Əlaqələr|Teqlər
---|---|---|---|
|<ul><li> Enlik və uzunluq cütləri kimi saxlanılan coğrafi mövqeyi təmsil edir.</li><li> Dağ zirvələri kimi ölçüsü olmayan xəritə xüsusiyyətlərini təmsil etmək üçün istifadə olunur.</li></ul> |<ul><li> Çoxbucaqlı və ya çoxbucaqlı ifadə edən qovşaqların çeşidlənmiş siyahıları</li><li> Yollar və çaylar kimi xətti xüsusiyyətləri və parkinq sahələri cəngəllikləri və parklar kimi zonaları təmsil edin.</li></ul> |<ul><li> Qovşaqların və yolların çeşidlənmiş siyahıları onların maneələr və u yollardakı döngələr, avtomobil yolları müxtəlif mövcud yolları və deşikli əraziləri əhatə edir.</li></ul> |<ul><li> Xəritə obyektləri haqqında metaməlumatları saxlayın.* Həmişə istənilən node, yola və ya əlaqəyə qoşulur</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

OSM öz əsas məlumatlarını saxlamaq üçün üç növ fayldan istifadə edir.

OSM bütün bu faylları formatlaşdırma təfərrüatları haqqında məlumatla idarə edir. Ancaq eyni daxili obyektlər bu fayllar tərəfindən istehsal olunur. Məlumat faylları üçün OSM obyektlərində görünən bayraq həmişə doğrudur, bu tarix və dəyişiklik faylları üçün belə deyil.

Ümumi istifadədə OSM fayl formatlarında müxtəliflik var. Fayl formatları diskdə və ya teldə məzmun kodlamasını bit və baytlarla müəyyən edir. OSM bu formatların maksimumunu oxumaq və yazmaq qabiliyyətinə malikdir.

**XML**

Orijinal OSM formatı XML əsaslıdır. Əsas OSM verilənlər bazası API-nin qaytarılması məlumatları XML formatındadır.

**PBF**

Protokol Buferləri kodlaşdırma ikili formatda dayanır və ən yığcam formatlardan biridir.

**O5M/O5C**

İkili formata əsaslanan daha sadə format, lakin nisbətən az istifadə olunur. OSM bu formatı oxuya bilər, lakin yaza bilməz.

**OPL**

Standart UNIX komanda xətti alətləri ilə istifadə etmək təklif olunan sadə format. CSV fayllarına yaxın, bir sətirdə bir OSM obyektinə imkan verir.

**SAKLAMA**

Sazlama üçün yaratmaq üçün nəzərdə tutulmuş mətn əsaslı format. OSM bu formatı yaza bilər, lakin oxuya bilmir.

**QARA DƏLİK**

Bütün məlumatları məhv edən dummy format. OSM bu formatı yaza bilər, lakin oxuya bilmir.

## OSM Məlumat Yaddaşı ##

OSM-in əsas **PostgreSQL** verilənlər bazası PostGIS genişləndirilməsi ilə OSM məlumatlarının əsas surətini saxlayır. Hər bir primitiv verilənlər üçün əsas verilənlər bazası cərgələrində fərdi obyektləri saxlayan cədvəli saxlayır. Bütün redaktələr bu verilənlər bazasını yeniləyir və bütün digər formatlar bu verilənlər bazasından istifadə etməklə formalaşır. Məlumatları bir yerdən digərinə ötürmək üçün çoxlu yüklənə bilən verilənlər bazası hovuzları yaradılmışdır. İki format, biri XML, digəri isə Protokol Bufer Binary Format (PBF) istifadə edərək bu hovuzları müəyyən edir. Tam məlumat planet.osm adlı faylda saxlanılır

## OSM fayllarında sıxılma ##

Mətn əsaslı formatlar (XML, OPL və Debug) isteğe bağlı olaraq gzip və ya bzip2 sıxılma istifadə edir.

## İstinadlar ##

* [OSM fayl formatları üzrə təlimat](https://osmcode.org/file-formats-manual/#file-types)

* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)

* [OSM öyrənin](https://learnosm.org/en/osm-data/getting-data/)


