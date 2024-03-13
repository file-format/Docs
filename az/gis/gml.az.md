{
  "date": "2019-10-11",
  "keywords": [
"gml faylı",
"gml faylı nədir",
"fayl",
"gml nümunəsi",
"gml fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GML - Coğrafiya İşarələmə Dili Fayl Formatı",
  "description": "GML fayl formatı və GML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "GML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gm-azl"
}
},
  "lastmod": "2019-09-10"
}

## GML faylı nədir?

GML Açıq Geoməkan Konsorsiumu (OGC) tərəfindən hazırlanmış XML spesifikasiyalarına əsaslanan Coğrafiya İşarələmə Dili deməkdir. Bu format müxtəlif fayl formatları arasında mübadilə üçün coğrafi məlumat xüsusiyyətlərini saxlamaq üçün istifadə olunur. O, coğrafi sistemlər üçün modelləşdirmə dili, eləcə də internetdə coğrafi əməliyyatlar üçün açıq mübadilə formatı kimi xidmət edir.

## GML Fayl Format ##

Əksər XML əsaslı qrammatikada olduğu kimi, qrammatikanın da iki hissəsi var - sənədi təsvir edən sxem və faktiki məlumatları ehtiva edən nümunə sənədi. GML sənədi GML sxemindən istifadə etməklə təsvir edilir. Bu, istifadəçilərə və tərtibatçılara nöqtələri, xətləri və çoxbucaqlıları ehtiva edən ümumi coğrafi məlumat dəstlərini təsvir etməyə imkan verir. Tətbiq sxemlərindən istifadə edərək, istifadəçilər nöqtələr, xətlər və çoxbucaqlılar əvəzinə yollara, magistral yollara və körpülərə istinad edə bilərlər.

Qeyd etmək lazımdır ki, GML xəritələrdə məkan məlumatlarının təsviri üçün şərh edilməməlidir. GML məzmununun təqdimatı GML-in yaradıldığı məqsəddən fərqlidir. Qısacası, GML XML-ə bənzəyir, çünki o, yalnız ekran məqsədləri üçün xəritəçəkmə tətbiqləri ilə istifadə edilə bilən məkan məzmununu saxlamaq üçün istifadə olunur.

### GML-də Məzmun formalaşması ###

GML represents spatial data using features which is a list of properties and geometries. A Property has a name, type and value description. Geometries are composed of basic geometry building blocks such as:

* xal

* xətlər

* əyrilər

* səthlər və

* çoxbucaqlılar


GML-in gələcək versiyalarının 3D həndəsəsini, eləcə də xüsusiyyətlər arasında topoloji əlaqələri dəstəkləməsi planlaşdırılır.

GML kodlaşdırması artıq kifayət qədər mürəkkəb funksiyalara imkan verir. Məsələn, bir xüsusiyyət digər xüsusiyyətlərdən ibarət ola bilər. Beləliklə, hava limanı kimi tək bir xüsusiyyət taksi yolları, uçuş-enmə zolaqları, asılqanlar və hava terminalları kimi digər xüsusiyyətlərdən ibarət ola bilər. Coğrafi obyektin həndəsəsi də bir çox həndəsə elementlərindən ibarət ola bilər. Beləliklə, həndəsi cəhətdən mürəkkəb xüsusiyyət nöqtələr, xətt sətirləri və çoxbucaqlılar daxil olmaqla həndəsə növlərinin qarışığından ibarət ola bilər.

### Nümunələr ###

GML 1.0 və 2.0 Poliqonları, Nöqtələri və LineString obyektlərini aşağıdakı kimi kodlayır:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## İstinadlar ##

* [GML Spesifikasiyaları](https://www.ogc.org/standard/gml/)

* [GML - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Geography_Markup_Language)


