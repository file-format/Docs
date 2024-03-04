{
  "date": "2021-06-09",
  "keywords": [
"m4p",
"mp3",
"failą",
"pratęsimas",
"formatu",
"kas yra m4p failo formatas",
"muzika",
"m4p failo formatas",
"M4b prieš MP3",
"m4p failo formato specifikacija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie M4P failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti M4P failus.",
  "title": "M4P – MPEG-4 garso knygos failo formatas",
  "linktitle": "M4P",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-m4-ltp"
}
},
  "lastmod": "2021-06-09"
}

## Kas yra M4P failas?
Failas su plėtiniu .m4p yra garso failas, kurį paprastai galima atsisiųsti Apple iTunes parduotuvėje. Kitaip tariant, galime pasakyti, kad M4P yra AAC failas, tačiau apsaugotas nuo kopijavimo naudojant skaitmeninių teisių valdymą (DRM). Tai reiškia, kad M4P failus galima leisti tik įgaliotose sistemose ar įrenginiuose. Paprastai M4P failai yra būdingi Apple daugialypės terpės įrenginiams. Taigi šiuos failus galima leisti tik Apple MacBook, podcast'uose, išmaniuosiuose telefonuose, tokiuose kaip iPhone 6 arba iPhone 7.

## M4P failo formatas
M4P reiškia MPEG 4 Protected (garsas), jis užkoduoja garsą pažangiu garso kodeku (AAC) ir apsaugo failą nuo neteisėto failo naudojimo. Šis failo formatas paprastai laikomas iTunes Music Store garso failo formatu. Apple naudoja savo FairPlay skaitmeninių teisių valdymo (DRM) sistemą, kad apsaugotų M4P failus. FairPlay DRM yra pagrįsta Veridisc sukurta technologija. Jo apsaugos mechanizmas veikia šifruodamas AAC garso srautą naudojant AES šifravimą. Vartotojas gauna pagrindinį raktą, kuris yra priskirtas jo paskyrai iššifruoti. Šis failo formatas buvo pristatytas kaip MP3 failo formato pakaitalas, nes MP3 iš pradžių buvo skirtas ne kaip garso failas, o kaip III sluoksnis MPEG 1 arba 2 vaizdo faile.


## M4P failo formato specifikacijos

Panašiai kaip [M4A](/audio/m4a/), M4P failai taip pat susideda iš nuoseklių dalių. Kiekvienas gabalas turi 8 baitų antraštę ir yra padalintas į:
- 4 baitų gabalo dydis (didelis baitas, pirmas didelis baitas)
- 4 baitų gabalo tipas – vienas iš iš anksto nustatytų parašų: mdat, moov, pnot, moof, udta, uuid, free, skip, ftyp, jP2, platus, apkrova, imap, matt, chap, kmat, clip, crgn, sync, tmcd, PICT, scpt , ctab, ssrc.

Similar to M4A the First chunk in M4P will be of type "ftype" and has a sub-type at offset 8. M4P, apibrėžtas potipiu, kuris turi būti M4P_.

Iteruojant gabalus, kol bus aptiktas nežinomo tipo gabalas, bus sukurtas M4P (MPEG-4 garso) failas.

## Nuorodos Nr.

* [MPEG-4 14 dalis – Vikipedija](https://en.wikipedia.org/wiki/MPEG-4_Part_14)

* [MPEG-4 14 dalies garso (M4A,M4B,M4P) formato ir atkūrimo pavyzdys](https://www.file-recovery.com/m4a-signature-format.htm)


