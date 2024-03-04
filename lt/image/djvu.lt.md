{
  "date": "2019-10-11",
  "keywords": [
"djvu failą",
"djvu failo formatas",
"kas yra djvu failas",
"failą",
"djvu pavyzdys",
"djvu failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DJVU failo formatas",
  "description": "Sužinokite apie DJVU failo formatą ir API, kurios gali kurti ir atidaryti DJVU failus.",
  "linktitle": "DJVU",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-djv-ltu"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra DJVU failas?

DjVu, tariamas kaip déjà vu, yra grafikos failo formatas, skirtas nuskaitytiems dokumentams ir knygoms, ypač tiems, kuriuose yra teksto, piešinių, vaizdų ir nuotraukų derinys. Jį sukūrė AT&T Labs. Jame naudojami keli būdai, pavyzdžiui, teksto ir fono vaizdų atskyrimas vaizdo sluoksniais, laipsniškas įkėlimas, aritmetinis kodavimas ir nuostolingas bitoninių vaizdų glaudinimas. Kadangi DJVU faile gali būti suspaustų, tačiau aukštos kokybės spalvotų vaizdų, nuotraukų, teksto ir piešinių, todėl jį galima išsaugoti mažiau vietos, jis naudojamas žiniatinklyje kaip el. knygos, žinynai, laikraščiai, senoviniai dokumentai ir kt.

DjVu gali būti įvertinta kaip geresnė [PDF](/pdf/) alternatyva. Su DjVu susiję failų plėtiniai yra .DJVU arba .DJV. DjVu gali pasiekti 5–10 geresnių glaudinimo koeficientų nei esami metodai, pvz., [JPEG](/image/jpeg/) ir [GIF](/image/gif/) spalvotiems dokumentams ir 3–8 kartus geresni nei [TIFF](/image/tiff/) nespalvotiems dokumentams. Nuskaityti dokumentai 300 DPI ir spalvoti iki 25 MB gali būti suglaudinti iki 30–100 KB. Panašiai nespalvotus dokumentus galima suglaudinti iki 5–30 KB. Vidutinis HTML puslapis gali būti iki 50 KB, todėl šiuos dokumentus galima be jokių problemų įkelti į tinklą.

## Trumpa istorija ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. DjVu failo formatas buvo peržiūrėtas įvairiais būdais, naujausias – 2005 m.


|Versija|Išleidimo data|Pastabos
---|---|---|
|1–19|1996–1999|Tai yra tobulinimo versijos.
|20|1999 m. balandžio mėn.|Vieno puslapio formatas pakeistas į kelių puslapių formatą.
|23|2002 m. liepos mėn.|CID dalis
|24|2003 m. vasario mėn.|LTAnno gabalas
|21|1999 m. rugsėjo mėn.|Pakeistas netiesioginės saugojimo formatas. Pridėtas teksto paieškos sluoksnis.
|22|2001 m. balandžio mėn.|Puslapio orientacija, spalva JB2
|25|2003 m. gegužės mėn.|NAVM dalis. Pridėtas DjVu žymių palaikymas.
|26|2005 m. balandžio mėn.|Teksto / eilučių anotacijos

## DjVu failo formatas ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. Šiame skyriuje aptariami įvairūs DjVu dokumentų tipai ir atitinkamos juos sudarančios dalys.


|Chunk ID|Naudojimas
---|---|
|FORM|Sudėtinis gabalas, turintis pirmuosius keturis FORM gabalo duomenų baitus, kurie yra antrinis identifikatorius.
|FORM:DJVM|Kelių puslapių DjVu dokumentas. Sudėtinis gabalas, kuriame yra DIRM dalis.
|FORMA:DJVU|Vieno puslapio DjVu dokumentas. Sudėtinis gabalas, kuriame yra dalys, sudarančios djvu dokumento puslapį.
|FORM:DJVI|Bendrinamas DjVu failas, įtrauktas per INCL gabalą. Bendrinami komentarai ir formų žodynas.
|FORM:THUM|Sudėtinė dalis, kurioje yra TH44 dalys, kurios yra įterptosios miniatiūros.
|DIRM|Kelių puslapių dokumentų puslapio pavadinimo informacija.
|NAVM|Žymės informacija
|ANTa, ANTz|Komentarai, įskaitant pradinio rodinio nustatymus ir persidengiančius hipersaitus, teksto laukelius ir kt.
|TXTa, TXTz|Unicode Teksto ir išdėstymo informacija.
|Djbz|Bendros formos lentelė.
|Sjbz|BZZ suglaudinti JB2 bitoniniai duomenys, naudojami kaukei saugoti.
|FG44|IW44 duomenys, naudojami pirmajam planui saugoti
|BG44|IW44 duomenys, naudojami fonui saugoti
|TH44|IW44 duomenys, naudojami įterptųjų miniatiūrų vaizdams saugoti
|WMRM|JB2 duomenys, reikalingi vandens ženklui pašalinti
|FGbz|Spalvokite JB2 duomenis. Pateikiama kiekvieno atitinkamo Sjbz gabalo spalva (blit ar forma?).
|INFO|Informacija apie a DjVu puslapį
|INCL|Įtraukto FORM:DJVI gabalo ID.
|BGjp|JPEG koduotas fonas
|FGjp|JPEG koduotas pirmas planas
|Smmr|G4 koduota kaukė

### DJVU suspaudimas

Vienas vaizdas yra padalintas į daugybę skirtingų vaizdų, o tada kiekvienas vaizdas suglaudinamas atskirai. Norint sukurti DjVu failą, vaizdas pirmiausia yra padalintas į tris vaizdus: foną, priekinį planą ir kaukės vaizdą. Paprastai fono ir priekinio plano vaizdai yra mažesnės skyros spalvoti vaizdai; bet kaukės vaizdas yra didesnės raiškos vaizdas ir paprastai ten saugomas tekstas. Po atskyrimo priekinio plano ir fono vaizdai suglaudinami naudojant bangele pagrįstą glaudinimo algoritmą IW44, o kaukės vaizdas suglaudinamas naudojant kitą metodą, vadinamą JB2.

JB2 kodavimo metodas pašalina didžiąją dalį teksto vaizdo pertekliaus, nes puslapyje nustatomos identiškos formos, pvz., keli simboliai tam tikrame šrifte. JB2 pirmiausia užkoduoja kiekvienos unikalios formos bitų žemėlapį, pasinaudodamas panašių formų pertekliumi. Tada jis koduoja vietas, kuriose kiekviena forma rodoma puslapyje. Tiek JB2, tiek IW44 remiasi naujo tipo adaptyviu dvejetainiu aritmetiniu kodavimu, vadinamu ZP kodavimu, kuris išstumia bet kokį likusį perteklinį perteklių per kelis procentus nuo Šenono ribos. ZP kodavimo įrenginys yra prisitaikantis ir greitesnis nei kiti apytiksliai dvejetainiai aritmetiniai kodai.

## Nuorodos Nr.

* [DjVu – Vikipedija](https://en.wikipedia.org/wiki/DjVu)

* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

