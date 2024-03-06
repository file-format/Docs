{
  "date": "2021-04-08",
  "keywords": [
"pkg fails",
"pkg faila formātā",
"kas ir pkg fails",
"failu",
"pkg piemērs",
"pkg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PKG — paplašināms arhīva faila formāts",
  "description": "Uzziniet par PKG faila formātu un API, kas var izveidot un atvērt PKG failus.",
  "linktitle": "PKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pk-lvg"
}
},
  "lastmod": "2021-04-13"
}

## Kas ir PKG fails?

Fails ar paplašinājumu .pkg ir instalēšanas pakotnes fails, kas tiek izmantots programmatūras instalēšanai operētājsistēmā MacOS. Papildus Macintosh datoriem tas tiek izmantots arī iPhone. Iebūvēto Apple instalēšanas programmu var izmantot, lai instalētu PKG faila saturu. PKG fails ir līdzīgs MSI failam, ko Windows operētājsistēmā izmanto programmatūras instalēšanai. Instalēšanas laikā šie pakotnes faili var reģistrēt ziņojumus, kas sniedz priekšstatu par to, kādas papildu lietas ir instalētas šajā pakotnē.

## PKG faila formāts

PKR ir bināri faili, kas tiek saspiesti, lai samazinātu kopējo faila lielumu. Kopš OSX 10.5 Apple ir ieviesis vienotas pakotnes ar vienu instalēšanas failu. Tie atšķiras no iepriekšējiem iepakojuma formātiem, kas tika piegādāti kā komplekti, nevis atsevišķi faili. Šajās komplektētajās pakotnēs bija strukturēta direktoriju hierarhija, kurā faili tika glabāti tā, lai atvieglotu to izgūšanu, izmantojot kādu indeksa failu. Plakanais PKG faila formāts patiesībā ir [XAR](/compression/xar/) arhīvs, kuram ir:

 * Header — definē izmēru, kontrolsummu un versiju informāciju
 * Satura rādītājs — XML dokuments, kas ir (un tam ir jābūt) kodētam kā UTF-8 un tiek saglabāts faila sākumā, atvieglojot skenēšanu arhīvā, lai izvilktu atsevišķu failu.
 * Kaudze — nestrukturēta datu kaudze, uz kuru atsaucas TOC

## Atsauces

* [Flat Package File Format](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)

* [PKG — Wikipedia](https://en.wikipedia.org/wiki/.pkg)


