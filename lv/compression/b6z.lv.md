{
  "date": "2019-10-11",
  "keywords": [
"b6z fails",
"b6z faila formāts",
"kas ir b6z fails",
"failu",
"b6z piemērs",
"b6z faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "B6Z - B6ZIP arhīva faila formāts",
  "description": "Uzziniet par B6Z failu formātu un API, kas var izveidot un atvērt B6Z failus.",
  "linktitle": "B6Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-b6-lvz"
}
},
  "lastmod": "2021-04-05"
}

## Kas ir B6Z fails?

Fails ar paplašinājumu .b6z ir saspiests arhīva fails, kas izveidots macOS programmatūras lietojumprogrammā [B6Zip](http://b6zip.com), ko izmanto failu saspiešanai un atspiešanai. Tas ir salīdzinoši jauns arhīva formāts, kas nodrošina lielāku saspiešanas pakāpi. B6Z ir atvērta arhitektūra un atbalsta failu izmērus līdz 900 000 PB. Tā atbalsta datu saspiešanu, kļūdu atkopšanu un failu pārslēgšanu. B6Zip utilīta programmatūra ir pieejama bez maksas operētājsistēmā MacOS, lai atvērtu dažāda veida saspiestus failus, tostarp B6Z.

## B6Z faila formāts

B6Z faila formāts ir balstīts uz atvērtu arhitektūru un nodrošina stabilu saspiešanu ar AES-256 šifrēšanas algoritmu. Tas izmanto LZMA2 kā noklusējuma saspiešanas metodi, bet atbalsta arī citas saspiešanas metodes, kā norādīts tālāk.

|Metode|Apraksts|
---|---|
|LZMA |LZ77 algoritma optimizēta versija|
|LZMA2| Uzlabota LZMA versija|
|Deflācija| Parastais LZ77 algoritms|
|BZip2| Standarta BWT algoritms|
|PPMD| Dmitrija Škarina PPMdH|

B6Zip utilīta atbalsta visus šos saspiešanas standartus un ir ļoti optimizēta, nodrošinot lielu ātrumu. Tā atbalsta darbu ar [ZIP](/compression/zip/), [TAR](/compression/tar/) un [RAR](/compression/rar/) failu formātiem. B6Z failiem ir MIME tipa lietojumprogramma/x-b6z saspiests.

## Atsauces

* [B6Zip](http://b6zip.com)


