{
  "date": "2021-07-28",
  "keywords": [
"ntf faylı",
"ntf fayl formatı",
"ntf faylı nədir",
"fayl",
"ntf nümunəsi",
"ntf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "NTF - Milli Transfer Formatlı Fayllar",
  "description": "NTF faylları yarada və aça bilən NTF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "NTF",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-nt-azf"
}
},
  "lastmod": "2021-07-28"
}

## NTF faylı nədir?
.ntf uzantısı olan fayllar **Milli Transfer Format (NTF)** Faylları adlanır; əsasən UK Ordnance Survey (OS) tərəfindən istifadə olunur; Xüsusilə coğrafi məlumatların ötürülməsi üçün. Britaniya Standartlar İnstitutu tərəfindən idarə olunur. Ordnance Survey rəqəmsal məlumatları üçün standart ötürmə formatına çevrildi. Transverse Mercator-un bir növü olan Böyük Britaniyanın Milli Şəbəkə proyeksiyası NTF faylları üçün bütün georeferanslı məlumatları özündə saxlayır.

## NTF fayl formatı
The NTF file format is owned by Ordnance Survey in the United Kingdom; supported by the GDB library for import. The Present version of the NTF file format is 2.0. Bu fayl formatı hər strukturda yalnız bir atribut sahəsi olan **PCIDSK** vektor seqmentinin məhdudiyyətini həll etmək üçün təqdim edilib, lakin vektor məlumatları ilə çıxarıla bilən müxtəlif atributlar var. NTF fayl formatı iki seqmentə sahib olaraq meydana gəlir. Hər bir seqment eyni vektorlardan ibarətdir, lakin fərqli atributlara malikdir. NTF vektor faylının birinci Seqmenti atribut kimi xüsusiyyət kodu nömrəsi olan vektorları ehtiva edir. İkinci seqment atribut kimi dəyəri olan vektorları ehtiva edir.

### Koordinat istinad sistemi
GDB kitabxanası müvafiq TM proyeksiya xüsusiyyətləri ilə rastr və vektor məlumatlarını təmsil edir:

- İstinad Uzunluğu: 49.0
- İstinad Eni: 2.0
- Yanlış Şərq: 400000
- Yanlış Şimal: -100000
- Ölçü: 0.9996012717
- Ellipsoid: Havadar 1830 (E009)
NTF fayllarını yeniləmək və ya yazmaq üçün heç bir dəstək mövcud deyil və ya DTM faylları ilə əlaqələndirilə bilməz.

### Ogrinfo nümunəsi
Aşağıdakı nümunə qat nömrələrini əldə etmək üçün NTF faylında **ogrinfo** istifadə edir:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## İstinadlar

* [UK Milli Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)

* [Veb Xəritəçəkmə - Tayler Mitchell tərəfindən təsvir edilmişdir](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)


