{
  "date": "2021-06-16",
  "keywords": [
"LZO",
"Saspiests",
"Fails",
"Pagarinājums",
"Faila formāts",
"Lempel-Ziv-Oberhume"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LZO faila formāts",
  "description": "Uzziniet par LZO failu formātu un API, kas var izveidot un atvērt LZO failus.",
  "linktitle": "LZO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-lvo"
}
},
  "lastmod": "2021-06-16"
}

## Kas ir LZO fails? ##

Fails ar paplašinājumu .lzo ir apvienots ar failu arhivēšanas līdzekļiem, kas var samazināt visu saspiestā faila failu lielumu. Visi saspiestie faili var ietvert vienu vai vairākus failus vai pat saistvielu grupas ar vairākiem dažāda veida un izmēra failiem. Saspiestā faila izmērs ir mazāks, salīdzinot ar visu LZO saspiestajā failā saglabāto failu un mapju kopējo lielumu. Visi LZO saspiestie faili tiek glabāti LZO formātā un tiek tieši izpildīti ar saspiešanas līdzekļiem, ko izmanto LZOP failu saspiešanas un atspiešanas programmatūra. Visas saspiešanas specifikācijas ir apvienotas šajā failu saspiešanas un atspiešanas programmā, kas ir izveidota no Lempel-Ziv-Oberhume failu saspiešanas bibliotēkas. Šajos LZO failos ir apvienots arī ātrāks dekompresijas ātrums un attīstītas saspiešanas pakāpes.

## LZO specifikācija ##

Markus Franz Xaver Johannes Oberhumer developed the original "lzop" algorithm, based on earlier algorithms by Abraham Lempel and Jacob Ziv, in 1996. Šī bibliotēka ievieš dažādus algoritmus ar šādām īpašībām:

* Ātrāka saspiešana nekā DEFLATE

* Ātra dekompresija

* Papildu buferi, kas nepieciešami saspiešanas laikā (8 KB vai 64 KB, atkarībā no saspiešanas līmeņa)

* Avota un mērķa buferi ir visa atmiņa, kas nepieciešama dekompresijai

* Nodrošina kontroli gan pār kompresijas pakāpi, gan kompresijas ātrumu


Kā bloku saspiešanas algoritms LZO veic saspiešanu, kas pārklājas, kā arī dekompresiju vietā. Lai panāktu saspiešanu, kas pārklājas, gan saspiešanas, gan dekompresijas bloka lielumam ir jāsakrīt. LZO saspiešanas algoritms sadala ievades datus atbilstībās (slīdošā vārdnīca) un nesakrītošajos literāļos, nodrošinot labus rezultātus ar ļoti liekiem datiem un pieņemamus rezultātus ar nesaspiežamiem datiem, tikai palielinot nesaspiežamos datus par 1/64 no sākotnējā. Izmērs.

## Problēmas, atverot LZO failu ##

Tālāk ir norādītas dažas problēmas, kas var izraisīt sliktu LZO faila formāta darbību:
  
* Fails var būt bojāts. Lai atrisinātu šo problēmu, lejupielādējiet failu vēlreiz vai lūdziet sūtītājam vēlreiz nosūtīt failu
* Otrs iemesls ir inficēts fails, šajā gadījumā skenējiet failu pareizi
* Nepareizas saites uz LZO failu
  *	 Removal of the description of the LZO 
* Nepietiek aparatūras resursu
* Novecojuši iekārtas draiveri
  
## Atsauces Nr.

* [LZO — Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)


