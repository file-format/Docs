{
  "date": "2021-03-18",
  "author": {
    "display_name": "Muhammad Umar",
    "keywords": [
"QGD",
"QGIS layihəsinin Sqlite verilənlər bazası",
"uzadılması",
"format",
"QGIS",
"Köməkçi verilənlər bazası",
"QGD faylı nədir"
]
},
  "draft": "false",
  "toc": true,
  "title": "QGD - QGIS Layihəsinin Sqlite verilənlər bazası",
  "description": "QGIS layihəsinin sqlite verilənlər bazası olan QGD və QGD fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "QGD",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-qg-azd"
}
},
  "lastmod": "2021-03-18"
}

## QGD faylı nədir?

.QGD fayl uzantısı olan fayl əslində layihə üçün köməkçi məlumatları özündə cəmləşdirən **QGIS** layihəsinin əlaqəli sqlite verilənlər bazasıdır. Layihə üçün heç bir köməkçi məlumat olmadıqda QGD faylı boş qalacaq.

## QGD Fayl Formatına dair təfərrüatlar

Klassik rejimdə köməkçi verilənlər bazası xml faylı boyunca .qgd uzantılı fayl kimi saxlanılır. **Köməkçi verilənlər bazası** sistemi alternativ üsul kimi sistemdə verilənləri oxumağa və yazmağa imkan verir. Sıkıştırılmış konteyner olan QGZ yaradarkən, .qgd faylı .qgz-ə daxildir.

## Köməkçi verilənlər bazası nədir?
Köməkçi verilənlər bazası əslində hədəf verilənlər bazasının təkrarlanmasına cavab olaraq yaradılan gözləmə rejimində olan db sistemidir. Köməkçi verilənlər bazası əslində dublikat verilənlər bazası halıdır ki, sizin dublikat etdiyiniz verilənlər bazası olacaq. Məsələn, dublikat verilənlər bazasından istifadə edərək gözləmə verilənlər bazası qurarsanız, mənbə verilənlər bazası hədəf olacaq və gözləmə verilənlər bazası köməkçi kimi tanınacaq.


## İstinadlar

* [QGZ – QGIS üçün yeni standart layihə fayl formatı](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)

* [QGIS File Formats](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

