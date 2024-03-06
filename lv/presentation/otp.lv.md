{
  "date": "2021-01-21",
  "keywords": [
"otp fails",
"otp faila formātā",
"kas ir otp fails",
"failu",
"otp piemērs",
"otp faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTP — OpenDocument prezentācijas veidne",
  "description": "Uzziniet par OTP faila formātu un API, kas var izveidot un atvērt OTP failus.",
  "linktitle": "OTP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ot-lvp"
}
},
  "lastmod": "2021-01-21"
}

## Kas ir OTP fails?

Faili ar paplašinājumu .otp ir prezentācijas veidņu faili, ko lietojumprogrammas ir izveidojušas OASIS OpenDocument standarta formātā. Šāda faila saturs ietver prezentācijas informāciju slaidu veidā ar tekstu, attēliem, formām, multivides saturu, pārejas efektiem un citiem slaidu elementiem. Šie veidņu faili tiek izmantoti, lai ātri izveidotu jaunas prezentācijas, pamatojoties uz stila informāciju, kas saglabāta pašā veidnē. OTP failus var izveidot un saglabāt, izmantojot vairākas dažādas lietojumprogrammas, piemēram, Impress, kas tiek piegādāts kopā ar OpenOffice komplektu un Microsoft PowerPoint. OTP faila formāts ir līdzīgs Microsoft PowerPoint veidņu failiem [.pot](/presentation/pot/) un [.potx](/presentation/potx/).

## OTP faila formāts

OTP faila formāts ir balstīts uz OpenDocument standartu, kas atbalsta dokumentu attēlošanu kā vienu XML dokumentu, kā arī vairāku apakšdokumentu apkopošanu vienā zip pakotnē formātā [ZIP](/compression/zip/). Faila saturs tiek izplatīts vairākos xml failos, kas ir iesaiņoti kopā. Šie vairāki [XML](/web/xml/) faili satur informāciju par dokumenta stilu, saturu, metainformāciju un iestatījumiem, kā minēts tālāk.

* `content.xml` — dokumenta saturs un saturā izmantotie automātiskie stili.

* `styles.xml` — dokumenta saturā izmantotie stili un pašos stilos izmantotie automātiskie stili.

* `meta.xml` — dokumenta metainformācija, piemēram, autors vai pēdējās saglabāšanas darbības laiks.

* `settings.xml` — lietojumprogrammas iestatījumi, piemēram, loga izmērs vai printera informācija.


## Atsauces

* [OpenDocument — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


