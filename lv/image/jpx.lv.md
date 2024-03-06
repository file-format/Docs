{
  "date": "2021-02-10",
  "keywords": [
"jpx failu",
"jpx faila formātā",
"kas ir jpx fails",
"failu",
"jpx piemērs",
"jpx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPX — attēla faila formāts",
  "description": "Uzziniet par JPX failu formātu un API, kas var izveidot un atvērt JPX failus.",
  "linktitle": "JPX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-lvx"
}
},
  "lastmod": "2021-02-10"
}

## Kas ir JPX fails? ##

Fails ar paplašinājumu .jpx ir JPEG 2000 faila formāta paplašinājums. Tas galvenokārt izmanto JPEG 2000 saspiešanu un nodrošina arī uzlabotas funkcijas, piemēram, vairākus attēla slāņus, dažādas krāsu telpas, necaurredzamību un sadrumstalotas koda straumes. JPX papildus JPEG 2000 saspiešanai pieļauj arī citas kompresijas, piemēram, JBIG, CCITT Group3, CCITT Group4 utt. JPX faila formāts tika apstiprināts kā [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) standarts, taču nevarēja saņemt siltu uzņemšanu, jo plaši tika izmantots [JPEG](/image/jpeg/) faila formāts. Lietojumprogrammas, kas var atvērt JPX failus, ietver Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 un CorelDraw Graphics Suite 2020.

## Īsa vēsture

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. 2004. gadā ISO/IEC 15444-2 formāts tika publiski pieņemts kā JP2 faila formāta paplašinājums.

## JPX faila formāts

JPX faila formāts tika izveidots tā, lai atbilstu to lietojumprogrammu prasībām, kurām bija nepieciešamas datu struktūras, kas pārsniedz [JP2](/image/jp2/) faila formātā noteikto funkcionalitāti. JP2 fails ar nesaderīgiem paplašinājumiem var radīt neskaidrības tirgū, jo daži lasītāji var interpretēt dažus JP2 failus, bet ne citus. JPX ir atbilde, lai izvairītos no šādām problēmām lietojumprogrammās.

### Faila identifikācija

JPX faili tiek saglabāti kā [JPF](/image/jpf/), ja tie tiek glabāti tradicionālajā datora failu sistēmā. Tāpēc JPX termins tiek izmantots vismazāk, salīdzinot ar JPF. JPX fails sākas ar šādiem baitiem:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Failu organizācija

Līdzīgi kā JP2, JPX fails ir lodziņu kolekcija, kam ir bināra struktūra un kastes ir sakārtotas blakus secībā. Pirmais lodziņš norāda faila sākumu ar tā pirmo baitu, un pēdējā lodziņa pēdējais baits apzīmē faila pēdējo baitu.
Kastītes binārā struktūra JPX failā ir identiska tai, kas definēta faila formātā [JP2](/image/jp2/).

### CodeStream glabāšana JPX formātā

JPX faila formāts ļauj attēla koda straumi sadalīt fragmentos. Tādējādi ir iespējams modificēt vienu attēla elementu un ierakstīt modificēto elementu faila beigās, nepārrakstot visu failu. Sākotnējais faila formāts [JP2](/image/jp2/) ierobežo visas koda straumes glabāšanu blakus esošā faila daļā, kas var radīt problēmas attēlu rediģēšanas lietojumprogrammām, kuras var vēlēties modificēt vienu attēla elementu un sasniegt iepriekš minēto JPX atbalstu. faila formātā. Attēla koda straumes sadrumstalotība padara JPX faila formātu pārāku par JP2 faila formātu. Turklāt JPX faila formāts ļauj apvienot vairākas kodu plūsmas un iegūt renderētu rezultātu. Kodu straumes var apvienot kā kompozīciju un animāciju.

## Atsauces Nr.

* [Pārskats par JPEG 2000](https://jpeg.org/jpeg2000/)


