{
  "date": "2019-10-11",
  "keywords": [
"djvu failu",
"djvu faila formātā",
"kas ir djvu fails",
"failu",
"djvu piemērs",
"djvu faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DJVU faila formāts",
  "description": "Uzziniet par DJVU failu formātu un API, kas var izveidot un atvērt DJVU failus.",
  "linktitle": "DJVU",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-djv-lvu"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DJVU fails?

DjVu, ko izrunā kā déjà vu”, ir grafikas faila formāts, kas paredzēts skenētiem dokumentiem un grāmatām, īpaši tiem, kas satur teksta, zīmējumu, attēlu un fotogrāfiju kombinācijas. To izstrādāja AT&T Labs. Tas izmanto vairākas metodes, piemēram, teksta un fona attēlu attēla slāņu atdalīšanu, progresīvu ielādi, aritmētisko kodēšanu un zudumu saspiešanu bitonālajiem attēliem. Tā kā DJVU fails var saturēt saspiestus, taču augstas kvalitātes krāsu attēlus, fotogrāfijas, tekstu un zīmējumus, un to var saglabāt mazākā vietā, tas tiek izmantots tīmeklī kā e-grāmatas, rokasgrāmatas, avīzes, seni dokumenti utt.

DjVu var novērtēt kā labāku alternatīvu [PDF](/pdf/). Ar DjVu saistītie failu paplašinājumi ir .DJVU vai .DJV. DjVu var sasniegt aptuveni 5–10 labākus saspiešanas koeficientus nekā esošās metodes, piemēram, [JPEG](/image/jpeg/) un [GIF](/image/gif/) krāsainiem dokumentiem, un 3–8 reizes labākus nekā [TIFF](/image/tiff/) melnbaltos dokumentos. Skenētus dokumentus ar izšķirtspēju 300 DPI ar pilnkrāsu līdz 25 MB var saspiest līdz 30 līdz 100 KB. Līdzīgi melnbaltos dokumentus var saspiest līdz 5 līdz 30 KB. Vidējā HTML lapa var būt līdz 50 KB, tāpēc šos dokumentus var bez problēmām augšupielādēt tīklā.

## Īsa vēsture ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. DjVu faila formātam ir veiktas dažādas pārskatīšanas, jaunākās no 2005. gada.


|Versija|Izlaiduma datums|Piezīmes
---|---|---|
|1–19|1996–1999|Šīs ir izstrādes versijas.
|20|1999. gada aprīlis|Viena lapa tika mainīta uz vairāku lappušu formātu.
|23|2002. gada jūlijs|CID gabals
|24|2003. gada februāris|LTAnno gabals
|21|1999. gada septembris|Aizstāts netiešās uzglabāšanas formāts. Teksta meklēšanas slānis ir pievienots.
|22|2001. gada aprīlis|Lapas orientācija, krāsa JB2
|25|2003. gada maijs|NAVM gabals. Tika pievienots atbalsts DjVu grāmatzīmēm.
|26|2005. gada aprīlis|Teksta/rindiņu anotācijas

## DjVu faila formāts ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. Šajā sadaļā ir aplūkoti dažādi DjVu dokumentu veidi un atbilstošās daļas, no kurām tie sastāv.


|Chunk ID|Lietojums
---|---|
|FORM|Salikts gabals, kurā ir pirmie četri FORM gabala datu baiti, kas ir sekundārie identifikatori.
|FORM:DJVM|Dauglapu DjVu dokuments. Salikts gabals, kas satur DIRM gabalu.
|FORM:DJVU|Vienas lapas DjVu dokuments. Salikts gabals, kas satur gabalus, kas veido lapu djvu dokumentā.
|FORM:DJVI|koplietots” DjVu fails, kas ir iekļauts, izmantojot INCL daļu. Koplietojamās anotācijas un formu vārdnīca.
|FORM:THUM|Salikts gabals, kas satur TH44 gabalus, kas ir iegultie sīktēli.
|DIRM|Lapas nosaukuma informācija vairāku lappušu dokumentiem.
|NAVM|Grāmatzīmju informācija
|ANTa, ANTz|Anotācijas, kas ietver gan sākotnējos skata iestatījumus, gan pārklājošās hipersaites, tekstlodziņus utt.
|TXTa, TXTz|Unicode Teksta un izkārtojuma informācija.
|Djbz|Koplietojamo formu tabula.
|Sjbz|BZZ saspiesti JB2 bitonālie dati, ko izmanto maskas glabāšanai.
|FG44|IW44 dati, ko izmanto priekšplāna glabāšanai
|BG44|IW44 dati, ko izmanto fona glabāšanai
|TH44|IW44 dati, ko izmanto iegulto sīktēlu attēlu glabāšanai
|WMRM|JB2 dati, kas nepieciešami ūdenszīmes noņemšanai
|FGbz|Krāsu JB2 dati. Katram atbilstošajā Sjbz daļā tiek nodrošināta krāsa (blīvējums vai forma?).
|INFO|Informācija par a DjVu lapu
|INCL|Iekļautā FORM:DJVI gabala ID.
|BGjp|JPEG kodēts fons
|FGjp|JPEG kodēts priekšplāns
|Smmr|G4 kodēta maska

### DJVU saspiešana

Viens attēls tiek sadalīts daudzos dažādos attēlos, un pēc tam katrs attēls tiek saspiests atsevišķi. Lai izveidotu DjVu failu, attēls vispirms tiek sadalīts trīs attēlos, fonā, priekšplānā un maskas attēlā. Parasti fona un priekšplāna attēli ir zemākas izšķirtspējas krāsu attēli; bet maskas attēls ir augstākas izšķirtspējas attēls, un parasti teksts tiek saglabāts tur. Pēc atdalīšanas priekšplāna un fona attēli tiek saspiesti, izmantojot viļņu saspiešanas algoritmu IW44, savukārt maskas attēls tiek saspiests, izmantojot citu metodi, ko sauc par JB2.

JB2 kodēšanas metode novērš lielu daļu teksta attēla dublēšanas, identificējot lapā identiskas formas, piemēram, vairākas rakstzīmes noteiktā fontā. JB2 vispirms kodē katras unikālās formas bitkarti, izmantojot dublēšanas priekšrocības starp līdzīgām formām. Pēc tam tas kodē vietas, kurās katra forma parādās lapā. Gan JB2, gan IW44 paļaujas uz jauna veida adaptīvo bināro aritmētisko kodētāju, ko sauc par ZP kodētāju, kas izspiež atlikušo dublēšanos dažu procentu robežās no Šenona robežas. ZP kodētājs ir adaptīvs un ātrāks nekā citi aptuvenie binārie aritmētiskie kodētāji.

## Atsauces Nr.

* [DjVu — Wikipedia](https://en.wikipedia.org/wiki/DjVu)

* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

