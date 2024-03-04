{
  "date": "2019-12-12",
  "keywords": [
"EPUB",
"failą",
"pratęsimas",
"formatu",
"E-knyga",
"Skaitmeninė knyga"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie EPUB failo formatą ir API, kurios gali kurti ir atidaryti EPUB failus.",
  "title": "Kas yra EPUB failas?",
  "linktitle": "EPUB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-epu-ltb"
}
},
  "lastmod": "2019-12-12"
}

## Kas yra EPUB failas?

Failai su plėtiniu .epub yra el. knygų failo formatas, suteikiantis standartinį skaitmeninio leidinio formatą leidėjams ir vartotojams. Formatas iki šiol buvo toks įprastas, kad jį palaiko daugelis el. skaitytuvų ir programinės įrangos. Pavyzdžiui, Mac OS sistemoje iš anksto įdiegta **Books** programinė įranga palaiko tokius failus. Be to, yra daug suderinamos programinės įrangos, skirtos išmaniesiems telefonams, planšetiniams kompiuteriams ir kompiuteriams. EPUB failų standartus palaiko [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). EPUB 3 versiją taip pat patvirtino Book Industry Study Group (BISG), pirmaujanti knygų prekybos asociacija, teikianti standartizuotą geriausią praktiką, tyrimus, informaciją ir renginius, susijusius su turinio pakavimu.

## Trumpa EPUB failo formato istorija

* **2007 m. spalio mėn.** – EPUB 2.0 patvirtintas

* **2010 m. rugsėjis** – išleistas techninės priežiūros naujinimas

* **2011 m. spalio mėn.** – įsigaliojo EPUB 3.0 specifikacijos

* **2014 m. birželio mėn.** – buvo išleistas nedidelis priežiūros atnaujinimas, pakeičiantis 3.0 versiją

* **2017 m. sausio mėn.** – įsigaliojo EPUB 3.1


## EPUB failo formatas

EPUB failo formatas yra archyvas, kurį galima pervardyti į [ZIP](/compression/zip/) plėtinį, o jo turinį galima peržiūrėti išskleidus archyvą bet kuriuo archyvo ištraukikliu. Tai atviras XML formatas, kurį sudaro HTML failai, vaizdai, CSS stiliaus lapai ir kiti elementai. Jį taip pat galima konvertuoti į PDF, Mobi ir keletą kitų failų formatų naudojant daugybę programinės įrangos ir API.

{{< figure src="../epub.png" alt="EPUB failo formatas" >}}

**EPUB el. knyga atidaryta naudojant Mac OS Books programą**

EPUB failo formatas yra pagrįstas šiais trimis atvirais standartais.

### Atvira viešoji struktūra (OPS) ###

EPUB 2.0 failas naudoja XHTML 1.1, kad sukurtų leidinio turinį. Iš esmės tai reiškia, kad EPUB failą sudaro vienas ar daugiau tinklalapių. Net jei galėtumėte įtraukti visą knygos ar laikraščio turinį į vieną puslapį, geriau, kad toks failas neviršytų 300 000 tiek dėl našumo, tiek dėl suderinamumo priežasčių. Kaip ir įprastuose tinklalapiuose, stilius ir išdėstymas apibrėžiami naudojant pakopinius stiliaus lapus (CSS). EPUB failuose turi būti naudojamas CSS2 poaibis (ribota komandų serija). Daugelis naujų CSS3 funkcijų, tokių kaip suapvalinti langeliai ar šešėliai, dar nepasiekiamos. Siekdamas atgalinio suderinamumo, kūrėjas taip pat gali naudoti DTBook, o ne XHTML, kad koduotų turinį.

### Atviras pakuotės formatas (OPF) ###

Ši specifikacijų dalis susijusi su struktūrine informacija, tokia kaip metaduomenys (kas yra autorius ir leidėjas, koks pavadinimas,...), manifestas (visų epub failo failų sąrašas) ir turinys. Visi šie duomenys yra įterpti naudojant XML.

### Atidaryti konteinerio formatą (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## Palaikomi vaizdo failų formatai ##

EPUB failo formatas palaiko šiuos vaizdo failų formatus.

* [GIF](/image/gif/)

* [JPG](/image/jpeg/)

* [PNG](/image/png/)

* [SVG](/page-description-language/svg/)

## Nuorodos Nr.

* [EPUB – Vikipedija](https://en.wikipedia.org/wiki/EPUB)


