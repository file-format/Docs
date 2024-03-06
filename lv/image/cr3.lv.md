{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR3 faila formāts — Canon Raw 3 attēla fails",
  "description":"Uzziniet par CR3 faila formātu un API, kas var izveidot un atvērt CR3 failus.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3-lv",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Kas ir CR3 fails?

CR3 fails ir Canon RAW attēla faila formāts, kas izveidots atsevišķās Canon digitālajās kamerās. To ieviesa Canon, lai aizstātu CR2 faila formātu, un to izmanto dažas Canon digitālās ierīces. CR3 faili saglabā sākotnējos neapstrādātos bezzudumu attēla datus, kas uzņemti ar kameru. Šo neapstrādāto attēlu izmantošana nodrošina augstas kvalitātes attēlus un ļauj fotogrāfiem daudz vietas rediģēt. Papildus galvenajiem attēla datiem CR3 faili saglabā arī metadatu informāciju par attēlu.

## CR3 faila formāts

CR3 faili tiek saglabāti diskā kā bināri faili ISO bāzes multivides faila formātā (ISO/IEC 14496-12), un tie ietver arī pielāgotu [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid). Tas ietver arī [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), kas ir JPEG-LS (Rice-Golomb + RLE kodēšana) un JPEG-2000 (LeGall 5/3 DWT + kvantifikācija) sajaukums.

## CR3 pielāgotie tagi

CR3 faili satur pielāgotus tagus dažādiem mērķiem. Daži no šiem tagiem ir šādi.

|Taga ID| Atzīmes nosaukums| Rakstāms |Vērtības / Piezīmes|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Tags|
|'CMT1' |IFD0| - |--> EXIF tagi|
|'CMT2' |ExifIFD| - |--> EXIF tagi|
|'CMT3' |MakerNoteCanon| - |--> Canon Tags|
|'CMT4' |GPSIinfo| - |--> GPS atzīmes|
|'CNCV' |CompressorVersion| nē| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH tagi|
|'THMB' |ThumbnailImage| nē| |

## Atsauces

 * [CR2 faila formāts] (http://lclevy.free.fr/cr2/)
 * [Canon tagi](https://exiftool.org/TagNames/Canon.html#uuid)

