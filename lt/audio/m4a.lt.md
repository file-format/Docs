{
  "date": "2021-04-26",
  "keywords": [
"m4a",
"mp3",
"failą",
"pratęsimas",
"formatu",
"kas yra m4a failo formatas",
"muzika",
"m4a failo formatas",
"M4A prieš MP3",
"m4a failo formato specifikacija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie M4A failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti M4A failus.",
  "title": "M4A – MPEG-4 garso failas",
  "linktitle": "M4A",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-lta"
}
},
  "lastmod": "2021-04-26"
}

## Kas yra M4A failas?

**M4A failo formatas** yra garso failas, sukurtas naudojant AAC (išplėstinį garso kodavimą), kuris yra žinomas kaip nuostolingas glaudinimas. Žodis M4A sutrumpintas kaip MPEG 4 Audio. Šie garso failai paprastai turi .m4a failo plėtinį. Tai ypač pasakytina apie neapsaugotą turinį. Jame gali būti saugomas įvairaus tipo garso turinys, pvz., garso knygos, dainos ir podcast'ai. M4A paprastai realizuojamas kaip pažangesnis formatas nei MP3, kuris paprastai nebuvo skirtas tik garsui. Tai tik garso sluoksnis MPEG 1 arba 2 vaizdo failuose.

M4A formatą užšifruoja FairPlay Digital Rights Management, nes buvo parduota per iTunes Store, naudojamas .m4p plėtinys. Apple iPhone skambėjimo tonams naudojamas MPEG-4 garsas, tačiau šie garso failai naudoja plėtinį .m4r.


## M4A prieš MP3

Tiek M4A, tiek [MP3](/audio/mp3/) yra tik garso failų formatai.

**M4A**: geresnis nei MP3 kokybės ir dydžių atžvilgiu, kai užkoduotas tuo pačiu bitų greičiu. .m4a failo plėtinys yra toks įprastas, nes Apple juos naudojo naudodamas iTunes muzikos parduotuvėje. M4A yra garso failas, suglaudintas naudojant MPEG-4 technologiją; nuostolingo glaudinimo algoritmas. Iš esmės tai siejama su MPEG-4 garso sluoksniu, failai su plėtiniu .m4a yra MPEG-4 filmų garso sluoksnis. Jis skirtas aplenkti MP3 ir tapti nauju garso glaudinimo standartu. Daugeliu atžvilgių jis yra labai artimas MP3, tačiau sukurtas siekiant geresnės kokybės to paties ar net mažesnio failo dydžio. M4A formatą pirmą kartą pristatė Apple. Formato tipas taip pat realizuojamas kaip Apple Losless Encoder (ALE).

Todėl šiuo metu M4A negali sulaukti pagrindinės MP3 sėkmės, nes garso formatas dar nėra įprastas. Tai kažkaip apsiriboja tik MacOS, iPod ir kitais Apple produktais.

**Mp3**: garsiausias skaitmeninio garso formatas. Tai taip pat buvo vienas iš pirmųjų suspaudimo formatų scenoje ir tapo labai populiarus tarp muzikos mylėtojų. Jo pagrindinė sėkmė yra tokia greita, kad failo tipas gali būti paleistas visuotinai ir su beveik bet kuo, aparatine ar programine įranga. Bendrąja prasme M4A sukurs geresnę garso kokybę, tačiau daugelis ginčytųsi, ar tai tiesa, ar ne, garso skirtumas nėra pastebimas, o MP3 failus konvertuoti į M4A failus būtų gaištamas laikas. Galų gale, konversija tiesiog privers prarasti pradinę garso kokybę.

## M4A failo formato specifikacija

M4A failus sudaro nuoseklūs gabalai. Kiekvienas gabalas turi 8 baitų antraštę ir yra padalintas į:
- 4 baitų gabalo dydis (didelis baitas, pirmas didelis baitas)
- 4 baitų gabalo tipas – vienas iš iš anksto nustatytų parašų: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, platus, įkelti, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt , ssrc, PICT.

First chunk will be of type "ftype" and has a sub-type at offset 8. M4A, apibrėžtas potipiu, kuris turi būti M4A_, M4B potipis turi būti M4B_, o M4P potipis turi būti M4P_.

Iteruojant gabalus, kol bus aptiktas nežinomo tipo gabalas, bus sukurtas M4A (MPEG-4 garso) failas.

## Nuorodos Nr.

* [MPEG-4 14 dalis – Vikipedija](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 14 dalies garso (M4A,M4B,M4P) formato ir atkūrimo pavyzdys](https://www.file-recovery.com/m4a-signature-format.htm)


