{
  "date": "2019-10-11",
  "keywords": [
"webp fails",
"webp faila formātā",
"kas ir webp fails",
"failu",
"webp piemērs",
"webp faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WEBP — Google rastra attēla faila formāts",
  "description": "Uzziniet par WEBP failu formātu un API, kas var izveidot un atvērt WEBP failus.",
  "linktitle": "WEBP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-webp"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir WEBP fails?

WebP, ko ieviesa Google, ir moderns rastra tīmekļa attēlu faila formāts, kura pamatā ir bezzudumu un zudumu saspiešana. Tas nodrošina tādu pašu attēla kvalitāti, vienlaikus ievērojami samazinot attēla izmēru. Tā kā lielākā daļa tīmekļa lapu izmanto attēlus kā efektīvu datu attēlojumu, WebP attēlu izmantošana tīmekļa lapās nodrošina ātrāku tīmekļa lapu ielādi. Saskaņā ar Google datiem WebP bezzudumu attēli ir par 26% mazāki salīdzinājumā ar [PNGs](/image/png/), savukārt WebP attēli ar zudumiem ir par 25–34% mazāki nekā salīdzināmie [JPEG](/image/jpeg/) attēli. Attēli tiek salīdzināti, pamatojoties uz strukturālās līdzības (SSIM) indeksu starp WebP un citiem attēlu failu formātiem. WebP ir [WebM](https://en.wikipedia.org/wiki/WebM) multivides konteinera formāta māsas projekts.

## WebP funkciju pārskats ##

WebP attēli izmanto saspiešanas procesu, pamatojoties uz pikseļu prognozēšanu no apkārtējiem blokiem, kā rezultātā pikseļi tiek izmantoti vairākas reizes vienā failā. Tas atbalsta animētus attēlus un paredzams, ka nākotnē tas atbalstīs vairāk funkciju. Google ir darījis pieejamu avota kodu [online](https://developers.google.com/speed/webp/download) savam kodētājam un dekodētājam, lai to varētu izmantot, kur nepieciešams. WebP attēls nodrošina atbalstu:

* **Zuduma saspiešana:** zaudējuma saspiešana ir balstīta uz [VP8](https://en.wikipedia.org/wiki/VP8) atslēgas kadra kodējumu. VP8 ir video saspiešanas formāts, ko izveidoja On2 Technologies kā VP6 un VP7 formātu pēcteci.

* **Bezzudumu saspiešana:** bezzudumu saspiešanas formātu ir izstrādājusi WebP komanda.

* **Caurspīdīgums:** 8 bitu alfa kanāls ir noderīgs grafiskiem attēliem. Alfa kanālu var izmantot kopā ar zudumiem RGB — šī funkcija pašlaik nav pieejama nevienā citā formātā.

* **Animācija:** atbalsta īstu krāsu animētus attēlus.

* **Metadati:** var būt EXIF un XMP metadati (piemēram, tos izmanto kameras).

* **Krāsu profils:** var būt iegults ICC profils.


Lossy WebP saspiešana izmanto jutīgo kodēšanu, lai kodētu attēlu, to pašu metodi, ko izmanto VP8 video kodekā, lai saspiestu atslēgu kadrus videoklipos. Prognozējošā kodēšana izmanto blakus esošo pikseļu bloku vērtības, lai prognozētu vērtības blokā, un pēc tam kodē tikai atšķirību.

Bezzudumu WebP saspiešana izmanto jau redzētus attēlu fragmentus, lai precīzi rekonstruētu jaunus pikseļus. Tas var izmantot arī vietējo paleti, ja netiek atrasta interesanta atbilstība.

## Faila formāts ##

WebP faila formāts ir balstīts uz RIFF (resursu apmaiņas faila formāta) dokumenta formātu. WebP konteiners nodrošina atbalstu vairākām funkcijām, ne tikai satur vienu attēlu, kas kodēts kā VP8 atslēgas rāmis. RIFF faila pamatelements ir gabals, kas sastāv no:


|Lauks|Apraksts
---|---|
|Chunk FourCC: 32 biti|ASCII četru rakstzīmju kods, ko izmanto gabala identifikācijai
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or paddi-lvng
|Rakmens slodze: Daļas lieluma baiti|Datu lietderīgā slodze. Ja gabala lielums ir nepāra, tiek pievienots viens polsterējuma baits ~-~-, kuram jābūt 0 ~-~-
|ChunkHeader ('ABCD')|Izmanto, lai aprakstītu atsevišķu gabalu FourCC un Chunk Size galveni, kur ABCD ir FourCC gabalam. Šī elementa izmērs ir 8 baiti.

### WebP galvene ###

WebP faila galvene ir šāda:

* RIFF galvene — 32 biti, kas attēlo ASCII rakstzīmes 'R' 'I' 'F' 'F'

* Faila lielums — 32 biti (uint32), kas apzīmē faila lielumu baitos, sākot ar nobīdi 8. Šī lauka maksimālā vērtība ir 2^32 mīnus 10 baiti, un tādējādi visa faila lielums ir ne vairāk kā 4 GiB mīnus 2 baiti. .

* 'WEBP' — 32 biti, kas apzīmē ASCII rakstzīmes 'W' 'E' 'B' 'P'


### Zaudēts faila formāts ###

WebP attēliem tiek izmantots zaudējuma faila formāts, ja attēla pamatā ir zudumu kodējums un nav nepieciešami nekādi uzlaboti/paplašināti līdzekļi, piemēram, caurspīdīgums, animācija, alfa utt. Zaudēti attēli ir mazāki, un tos atbalsta arī vecākas lietojumprogrammas.

WebP fails šajā gadījumā sastāv no:

* 12 baitu WebP faila galvene

* VP8 gabals


[VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) ilustrē VP8 bitu straumes formāta specifikācijas.

### Bezzudumu faila formāts ###

Šis izkārtojums tiek izmantots, ja attēla pamatā ir nezaudējošs kodējums un nav nepieciešamas papildu funkcijas, ko nodrošina ārējais formāts. Tomēr vecākas lietojumprogrammas var nespēt nolasīt šādus failus.

WebP fails šajā gadījumā sastāv no:

* 12 baitu WebP faila galvene

* VP8L gabals


## Atsauces Nr.

* [WebP izstrādātāja uzziņa — no Google](https://developers.google.com/speed/webp/)

* [WebP faila formāts — Wikipedia](https://en.wikipedia.org/wiki/WebP)


