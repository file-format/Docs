{
  "date": "2020-03-02",
  "keywords": [
"SVG",
"failą",
"Dokumento formatas",
"Puslapio aprašymas Kalba",
"Skaliarinis"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie SVG failo formatą ir API, kurios gali kurti ir atidaryti SVG failus.",
  "title": "Kas yra SVG failas?",
  "linktitle": "SVG",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sv-ltg"
}
},
  "lastmod": "2020-03-02"
}

## Kas yra SVG failas? ##

An SVG file is a Scalar Vector Graphics file that uses XML based text format for describing the appearance of an image. The word Scalable refers to the fact that the SVG can be scaled to different sizes without losing any quality. Text-based description of such files makes them independent of resolution. It is one of the most used formats for building a website and print graphics in order to achieve scalability. The format can only be used for two-dimensional graphics though. SVG files can be viewed/opened in almost all modern browsers including Chrome, Internet Explorer, Firefox, and Safari.

## Trumpa istorija ##

SVG specifications are available as open standard by World Wide Web Consortium (W3C) since 1999. Prieš tai iki 1998 m. W3C buvo pateiktos panašios failų formatų specifikacijos šešiais skirtingais formatais. 2011 m. specifikacijos buvo atnaujintos ir jos versija buvo 1.1. 2016 m. SVG 2 buvo paskelbta kaip naujesnė versija su funkcijomis, be SVG 1.1.

## Failo formato specifikacijos ##

SVG dokumento objekto modelis (DOM) sudaro pagrindą visoms specifikacijoms ir sąsajoms, kurios atitinka konkrečias specifikacijų dalis. SVG peržiūros priemonės turi įdiegti SVG DOM sąsajas, kaip apibrėžta W3C specifikacijose. Jo DOM atskleidžia keletą sąsajų skirtingiems duomenų tipams ir elementams.

### SVG formos ###

SVG turi keletą iš anksto nustatytų formos elementų, kuriuos gali naudoti kūrėjai:

* Stačiakampis<rect>

* Apskritimas<circle>

* Elipsė<ellipse>

* Linija<line>

* Poliline<polyline>

* Poligonas<polygon>

* Kelias<path>


Remiantis šiomis formomis ir specifikacijomis, SVG funkcinės sritys yra tokios.

**Keliai** – keliai naudojami paprastiems ir sudėtiniams kontūrams pavaizduoti. Kodai naudojami operacijos pobūdžiui apibrėžti. Pavyzdžiui, M naudojamas perkėlimui į, L naudojamas linijai į, Z naudojamas kelio uždarymui ir pan.

**Pagrindinės formos** – galima nubrėžti tiesių linijų ir kelių sujungtų tiesių atkarpų (polilinijų) serijos, taip pat uždarus daugiakampius, apskritimus ir elipses. Stačiakampiai ir stačiakampiai su apvaliais kampais taip pat yra standartiniai elementai.

**Tekstas** – teksto atvaizdavimas išreiškiamas kaip XML simbolių duomenys, kuriuose tekstui galima pritaikyti daug vaizdinių efektų. Specifikacijos leidžia tvarkyti dvikryptį tekstą, vertikalų tekstą ir simbolius lenktu keliu.

**Tapyba** – Formos gali būti užpildytos ir (arba) kontūruojamos spalva, gradientu arba raštu, kad būtų galima padaryti jį nepermatomą arba bet kokio skaidrumo laipsnį. Linijos pabaigos ypatybės, tokios kaip rodyklių galvutės ar simboliai, atsirandantys daugiakampio viršūnėse, yra pavaizduoti žymekliais.

**Spalva** – SVG specifikacijos leidžia pritaikyti spalvas visiems matomiems SVG elementams tiesiogiai arba per užpildymą, brūkšnį ir kitas savybes. Įvairūs spalvų kodai gali būti naudojami norint nurodyti, pavyzdžiui, juodą arba mėlyną, šešioliktainį vaizdą, dešimtainį skaičių arba RGB formos procentais.

**Gradientai ir raštai** – SVG failo formos gali būti užpildytos arba nubrėžtos vientisomis spalvomis, gradientais arba pasikartojančiais raštais.

**Filtro efektai** – iš tikrųjų tai grafinių operacijų, kurios taikomos tam tikros šaltinio vektorinės grafikos elementams, kad būtų gautas modifikuotas rezultatas.

**Interaktyvumas** – vartotojai gali sąveikauti su SVG failais keisdami fokusavimą, spustelėdami pelę, slinkdami arba keisdami vaizdą. Interaktyvumas leidžia SVG vaizdams sąveikauti su vartotojais įvairiais būdais, kaip minėta pirmiau.

**Susiejimas** – SVG vaizduose gali būti hipersaitų į kitus dokumentus. Tai pasiekiama naudojant XML susiejimo kalbą arba XLink. Tai leidžia sukurti konkrečias rodinio būsenas, kurios naudojamos norint priartinti / nutolinti tam tikrą sritį arba apriboti vaizdą iki konkretaus elemento.

**Scenarijų rašymas** – panašiai kaip HTML, visi SVG dokumento aspektai yra pasiekiami manipuliavimui naudojant scenarijus. SVG DOM objektai pateikia gaires, kaip tai pasiekti naudojant SVG elementą ir atributą. Scenarijai yra įtraukti į script žymos elementus ir, jei reikia, gali būti vykdomi reaguojant į žymeklio, klaviatūros ar dokumento įvykius.

**Animacija** – DOM elementai<animate> ,<animateMotion> ir<animateColor> leidžia įtraukti animaciją į SVG turinį. Žinoma, tai neįmanoma pasiekti nenaudojant scenarijų ir įmontuotų laikmačių. Šios animacijos gali būti nenutrūkstamos ir gali būti kartojamos arba kartojamos, tuo pačiu reaguodamos į vartotojo įvykius.

**Šriftai** – SVG tekstas gali nurodyti išorinius šriftų failus, pvz., sistemos šriftus. Jei tokių šriftų nėra, tekstas SVG formatu nebus pateikiamas išvestyje. Tai galima įveikti įtraukiant reikiamus glifus į tokį failą kaip šriftą, kuris atvaizduojamas naudojant<text> elementas.

## Pavyzdžiai ##
Šiose eilutėse parodyta, kaip apskritimas vaizduojamas naudojant SVG scenarijų.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Šios kodo eilutės parodo, kaip naudoti<text> blokas, skirtas tekstui pateikti SVG formatu.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Nuorodos Nr.

* [W3C SVG specifikacijos](https://www.w3.org/TR/SVG2/Overview.html)

* [SVG – Vikipedija](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)


