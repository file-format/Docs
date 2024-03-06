{
  "date": "2021-07-29",
  "keywords": [
"md5 failu",
"md5 faila formātā",
"kas ir md5 fails",
"failu",
"md5 piemērs",
"md5 faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD5 — MD5 kontrolsummas fails",
  "description": "Uzziniet par MD5 failiem un API, kas var izveidot un atvērt MD5 failus.",
  "linktitle": "MD5",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-md-lv5"
}
},
  "lastmod": "2021-07-29"
}

## Kas ir MD5 fails?

MD5 fails ir kontrolsummas fails, ko izmanto faila integritātes pārbaudei. Tas ir līdzīgs saistītā faila pirksta nospiedumam un tiek unikāli ģenerēts, izmantojot algoritmu, kas izmanto failā esošo bitu skaitu. To izmanto, lai pārbaudītu failu ar tādu programmatūru kā [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Viena no MD5 failu izmantošanas priekšrocībām ir pārbaudīt, vai lejupielādētie faili nav bojāti.

## MD5 faila formāts — plašāka informācija

Parasti MD5 fails tiek saglabāts ar tādu pašu nosaukumu kā sākotnējā faila nosaukums, bet ar paplašinājumu .md5. Piemēram, ja saistītā faila nosaukums ir abc_987_123456.grb”, atbilstošais MD5 faila nosaukums būs abc_987_123456.grb.md5”. MD5 faili palīdz noteikt, vai saņemtais vai lejupielādētais fails nav bojāts vai to neietekmē ļaunprātīgs saturs. Īsāk sakot, MD5 faili garantē faila pilnīgumu.


## Kā pārbaudīt MD5 kontrolsummu?

Vienu failu var pārbaudīt/verificēt MD5, izmantojot rīku [md5sum](https://en.wikipedia.org/wiki/Md5sum), kā norādīts tālāk.

```
md5sum -c abc_987_123456.grb.md5
```

## Atsauces

* [md5sum — Wikipedia](https://en.wikipedia.org/wiki/Md5sum)


