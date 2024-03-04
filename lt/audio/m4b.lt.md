{
  "date": "2021-06-09",
  "keywords": [
"m4b",
"mp3",
"failą",
"pratęsimas",
"formatu",
"kas yra m4b failo formatas",
"muzika",
"m4b failo formatas",
"M4b prieš MP3",
"m4b failo formato specifikacija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie M4B failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti M4B failus.",
  "title": "M4B – MPEG-4 garso knygos failo formatas",
  "linktitle": "M4B",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-ltb"
}
},
  "lastmod": "2021-06-09"
}

## Kas yra M4B failas?

Failas su plėtiniu .m4b yra garsinė knyga, paprastai naudojama Apple Books ir iTunes. Šiame formate naudojamas garso įrašas yra saugomas MPEG-4 ir suglaudinamas naudojant AAC kodavimą. M4B failas yra labai panašus į M4A, tačiau palaiko su garsine knyga susijusias funkcijas, pvz., žymėjimą ir skyrių pertraukas. M4B failai yra prieinami tiek DRM, tiek nemokamų DRM versijų. DRM užšifruotos garso knygos paprastai yra mokamos garso knygos iš iTunes Store. Tuo tarpu DRM nemokamai galima rasti internete.

## M4B failo formatas

Garso knygos failus, kuriuose yra metaduomenų, vaizdų, žymių ir hipersaitų, galima išsaugoti naudojant .m4a plėtinį, tačiau paprastai išsaugant naudojamas plėtinys .m4b, tik norint nurodyti, kad failas turi garso knygos failo formatą. Fairplay DRM (skaitmeninių teisių valdymas) naudojamas programos, kad apsaugotų savo M4B failus. Taigi iš iTunes atsisiųstus failus galima leisti tik įgaliotuose įrenginiuose ar kompiuteriuose.


## M4B prieš M4A

Tiek M4B, tiek [MP3](/audio/mp3/) yra tik garso failų formatai.

**M4B**: laimi lyginant su MP3 kokybės požiūriu, jei abu koduojami tuo pačiu bitų dažniu. M4B yra garso knygos failas, suglaudintas naudojant AAC kodavimą. Iš esmės tai siejama su MPEG-4 garso sluoksniu, failai su plėtiniu .m4b yra MPEG-4 filmų garso sluoksnis, tačiau turi papildomų funkcijų, susijusių su garso knyga. Jo tikslas yra aplenkti MP3 ir tapti nauju garso glaudinimo standartu. Daugeliu atžvilgių jis yra labai artimas MP3, bet sukurtas taip, kad būtų geresnė to paties ar net mažesnio dydžio failo kokybė. M4B formatą pirmą kartą pristatė Apple. Formato tipas taip pat realizuojamas kaip Apple Losless Encoder (ALE).

Todėl šiuo metu M4B negali sulaukti pagrindinės MP3 sėkmės, nes garso formatas dar nėra įprastas.

**Mp3**: visiems gerai pažįstamas skaitmeninio garso formatas. Pats pirmasis suspaudimo formatas scenoje ir labai išgarsėjo tarp muzikos klausytojų. Jo pagrindinė sėkmė yra tokia greita, kad failo tipas gali būti grojamas visuotinai ir suderinamas su beveik viskuo, aparatine ar programine įranga. Bendrąja prasme M4A sukurs geresnę garso kokybę, tačiau daugelis ginčytųsi, ar tai tiesa, ar ne, garso skirtumas nėra palyginamas ir būtų gaištamas laikas bandant konvertuoti MP3 failus į M4A failus. Galiausiai, konvertuojant tiesiog prarasite pradinę garso kokybę.

## M4B failo formato specifikacija

Panašiai kaip ir [M4A](/audio/m4a/), M4B failus taip pat sudaro nuoseklūs gabalai. Kiekvienas gabalas turi 8 baitų antraštę ir yra padalintas į:
- 4 baitų gabalo dydis (didelis baitas, pirmas didelis baitas)
- 4 baitų gabalo tipas - vienas iš iš anksto nustatytų parašų: ftyp, mdat, moov, pnot, moof, udta, uuid, free, ctab, praleisti, jP2, platus, apkelti, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT , scpt, ssrc.

Similar to M4A the First chunk in M4B will be of type "ftype" and has a sub-type at offset 8. M4B, apibrėžtas potipiu, kuris turi būti M4B_.

Iteruojant gabalus, kol bus aptiktas nežinomo tipo gabalas, bus sukurtas M4B (MPEG-4 garso) failas.

## Nuorodos

* [MPEG-4 14 dalis – Vikipedija](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 14 dalies garso (M4A,M4B,M4P) formato ir atkūrimo pavyzdys](https://www.file-recovery.com/m4a-signature-format.htm)


