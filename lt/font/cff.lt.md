{
  "date": "2020-08-20",
  "keywords": [
"cff failą",
"cff failo formatas",
"kas yra cff failas",
"failą",
"cff pavyzdys",
"cff failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF - kompaktiškas šrifto failo formatas",
  "description": "Sužinokite apie CFF failo formatą ir API, kad sukurtumėte ir atidarytumėte CFF failus.",
  "linktitle": "CFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cf-ltf"
}
},
  "lastmod": "2020-10-21"
}

## Kas yra CFF failas?

Failas su plėtiniu .cff yra kompaktinio šrifto formatas ir taip pat žinomas kaip 1 tipo PostScript arba CIDFont. CFF veikia kaip talpykla, skirta saugoti kelis šriftus viename vienete, žinomame kaip FontSet. CFF šriftų dizainas leidžia įterpti PostScript kalbos kodą, kuris suteikia papildomo lankstumo ir išplečiamo formato, naudojamo spausdintuvo aplinkoje. CFF šrifto failus galima atidaryti ir konvertuoti naudojant API, pvz., [Aspose.Font](https://products.aspose.com/font).

## CFF failo formatas

CFF failai yra dvejetainiai failai, kuriuose yra struktūrinis duomenų išdėstymas, apibrėžti duomenų tipai, antraštė, glifų organizavimas ir lentelių žodynai. Daugiau informacijos apie tai rasite [compact font format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Duomenų išdėstymas
CFF failo formato duomenų išdėstymas yra toks, kaip parodyta toliau.

|Įrašas|Komentarai|
---|---|
|Antraštė|–|
|VardasINDEX|–|
|Geriausias DICT RODYKLĖ|–|
|Eilutė INDEX|–|
|Global Subr INDEX|–|
|Koduotės–Rašmenų rinkiniai|–|
|FDSelect|Tik CIDFontai|
|CharStrings INDEX|už šriftą|
|Šriftas DICT INDEX|už šriftą, tik CIDFontai|
|Privatus DICT|už šriftą|
|Local Subr INDEX|už šriftą arba privatų DICT, skirtą CIDFontams|
|Autorių teisių ir prekių ženklų pranešimai|–|

### Duomenų tipai

CFF duomenų tipai yra tokie, kaip parodyta šioje lentelėje.

|Vardas|Diapazonas|Aprašymas|
---|---|---|
|Kortelė8|0 –255|1 baito nepasirašytas numeris|
|Kortelė16|0 – 65535|2 baitų nepasirašytas numeris|
|Poslinkis|kinta|1, 2, 3 arba 4 baitų poslinkis (nurodytas OffSize lauke)|
|OffSize|1–4|1 baito nepaženklintas skaičius nurodo poslinkio lauko ar laukų dydį|
|SID|0 – 64999|2 baitų eilutės identifikatorius|

### Antraštė

Dvejetainiai duomenys prasideda antrašte, kurios formatas parodytas šioje lentelėje.

|Tipas|Vardas|Aprašymas|
---|---|---|
|Card8|major|Formatuoti pagrindinę versiją (pradedant nuo 1)|
|Card8|minor|Formatuoti mažąją versiją (pradedant nuo 0)|
|Kortelė8|hdrDydis| Antraštės dydis (baitais)|
|OffSize|offSize|Absoliutus poslinkis (0) dydis|

## Nuorodos

 * [Compact Font Format Table](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
 * [CFF failo formatas](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
 * [CFF2 diagramų rinkinys](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

