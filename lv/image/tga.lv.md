{
  "date": "2019-10-11",
  "keywords": [
"tga failu",
"tga faila formātā",
"kas ir tga fails",
"failu",
"tga piemērs",
"tga faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGA faila formāts — TARGA grafiskā attēla fails",
  "description": "Uzziniet par TGA failu formātu un API, kas var izveidot un atvērt TGA failus.",
  "linktitle": "TGA",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-tg-lva"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir TGA fails?

Fails ar paplašinājumu .tga ir rastra grafikas formāts, un to izveidoja Truevision Inc. Tas bija paredzēts TARGA (Truevision Advanced Raster Adapter) platēm un nodrošināja Highcolor/truecolor displeja atbalstu ar IBM saderīgiem personālajiem datoriem. Tas atbalsta 8, 16, 24 un 32 bitus uz pikseļu un 8 bitu alfa kanālu. Tā atbalsta arī bezzudumu RLE saspiešanu, ko var izmantot, lai samazinātu attēla izmēru. Digitālās fotogrāfijas un faktūras izmanto TGA attēla formātu.

## Īsa vēsture

TGA faila formātu 1984. gadā izveidoja AT&T EPICenter (vēlāk tika iegūta un izveidota kā neatkarīga vienība, kas pazīstama kā Truevision), kas strādāja pie AT&T izstrādāto jauno tehnoloģiju mārketinga krāsu kadru buferiem. EPICenter jau strādāja pie pirmajām divām kartēm — VDA (video displeja adapteris) un ICB (attēlu uztveršanas plate), kurām jau tika strādāts pie diviem failu tipiem — .vda un .icb. Šie failu formāti tika kodificēti un tika ieviests mazāk specifisks failu formāts TGA. TGA bija paplašinājums jau izmantotajam, un sniedza tādu informāciju kā platums, augstums, pikseļu dziļums, saistīto krāsu karte un attēla izcelsme.

TGA 2.0 versija, kas publicēta 1989. gadā, ietvēra vairākas uzlabotas funkcijas, piemēram:

 * Sīktēli
 * Alfa kanāls
 * Gamma vērtība
 * Tekstuālie metadati

TGA 2.0 versijas galvenie atbalstītāji ir Šons Steiners no Truevision, Kevins Fidlijs un Deivids Spoelstra.

## TGA TARGA faila formāta specifikācijas

TGA fails sastāv no 2 galvenajām daļām:

 * Virsraksts
 * Krāsu pikseļu informācija

Visas vērtības TGA failā ir mazā formātā atbilstoši formāta specifikācijām.

### TGA galvene

TGA faila galvene sastāv no šādiem 5 laukiem.

|Lauka nr.|Garums |Lauka nosaukums |Apraksts|
---|---|---|---|
|1| 1 baits |ID garums| Attēla ID lauka garums (0-255)|
|2| 1 baits |Krāsu kartes veids| Vai ir iekļauta krāsu karte (0 — norāda, ka šajā attēlā nav iekļauti krāsu kartes dati. 1 — norāda, ka šajā attēlā ir iekļauta krāsu karte.)|
|3| 1 baits |Attēla veids| Saspiešana un krāsu veidi (0 — nav iekļauti attēla dati. 1 — nesaspiests, krāsu kartēts attēls, 2 — nesaspiests, patiesas krāsas attēls, 9 — iestrādes garuma kods, krāsains kartēts attēls, 11 — kodēts darbības ilgums, melnbalts attēls )|
|4| 5 baiti |Krāsu kartes specifikācija| Apraksta krāsu karti|
|5| 10 baiti |Attēla specifikācija| Attēla izmēri un formāts|

### Attēlu un krāsu kartes dati

|Lauks Nr. |Garums |Lauks |Apraksts|
---|---|---|---|
|6 |No attēla ID garuma lauka| Attēla ID| Neobligāts lauks, kurā ietverta identifikācijas informācija|
|7 |No krāsu kartes specifikācijas lauka| Krāsu kartes dati| Uzmeklēšanas tabula ar krāsu kartes datiem|
|8 |No attēla specifikācijas lauka| Attēla dati| Saglabāts saskaņā ar attēla deskriptoru|

### Izstrādātāju apgabals (neobligāti)

TGA versija 2.0 nodrošina atbalstu papildu uzlabojumiem/ekstras, kuras daudzi izstrādātāji vēlējās saglabāt vairāk informācijas. Informācija nav obligāta, tāpēc, ja TGA dekodētājs nevar to interpretēt, tā tiks ignorēta.

### Paplašinājuma apgabals (pēc izvēles)

|Lauks nr.| Garums| Lauks |Apraksts|
---|---|---|---|
|10| 2 baiti |Paplašinājuma lielums |Paplašinājuma apgabala lielums baitos, vienmēr 495|
|11| 41 baits| Autora vārds |Autora vārds. Ja baiti netiek izmantoti, tie jāiestata uz NULL (\0) vai atstarpes|
|12| 324 baiti| Autora komentārs| Komentārs, kas sakārtots kā četras rindiņas, katra sastāv no 80 rakstzīmēm plus NULL|
|13| 12 baiti| Datuma/laika zīmogs |Attēla izveides datums un laiks|
|14| 41 baits| Darba ID||
|15| 6 baiti| Darba laiks| Stundas, minūtes un sekundes, kas pavadītas faila izveidei (rēķiniem utt.)|
|16| 41 baits| Programmatūras ID |Lietojumprogramma, kas izveidoja failu.|
|17| 3 baiti| Programmatūras versija||
|18| 4 baiti| Atslēgas krāsa||
|19| 4 baiti| Pikseļu malu attiecība ||
|20| 4 baiti| Gamma vērtība||
|21| 4 baiti| Krāsu korekcijas nobīde |Baitu skaits no faila sākuma līdz krāsu korekcijas tabulai, ja tāda ir|
|22| 4 baiti| Pastmarka | Baitu skaits no faila sākuma līdz pastmarkas attēlam, ja tāds ir|
|23| 4 baiti| Skenēšanas līnijas nobīde| Baitu skaits no faila sākuma līdz skenēšanas līniju tabulai, ja tāda ir|
|24| 1 baits| Atribūtu veids| Norāda alfa kanālu|

### Faila kājene (neobligāti)

Pēdējie 26 faila baiti ir kājene, kas, ja tāda ir, visticamāk, ir TGA 2. versijas fails.

|Lauks Nr.| Garums| Lauks| Apraksts|
---|---|---|---|
|28| 4 baiti| Pagarinājuma nobīde| Nobīde baitos no faila sākuma|
|29| 4 baiti| Izstrādātāja apgabala nobīde| Nobīde baitos no faila sākuma|
|30| 16 baiti| Paraksts| Satur TRUEVISION-XFILE|
|31| 1 baits| | Satur .|
|32| 1 baits| | Satur NULL|


## Atsauces

 * [TGA 2.0 File Format Specifications](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
 * [TGA no Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

