{
  "date": "2019-10-11",
  "keywords": [
"mf failą",
"mf",
"pratęsimas",
"formatu",
"mf failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MF – Java manifesto failo formatas",
  "description": "Sužinokite apie MF failo formatą ir API, kurios gali kurti ir atidaryti MF failus.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-ltf"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra MF failas?

Failas su plėtiniu .mf yra Java manifesto failas, kuriame yra informacijos apie atskirus [JAR](/programming/jar/) failo įrašus. Pats MF failas yra JAR faile ir pateikia visą plėtinį ir su paketu susijusį apibrėžimą. JAR failus galima sukurti ir naudoti kaip vykdomąjį failą. Tokiu atveju mainfest failas nurodo pagrindinę programos klasę, kurioje yra **`public static void main`** teiginys. Manifesto failai pavadinti MANIFEST.MF ir gali būti atidaryti naudojant bet kurią teksto rengyklę Windows, MacOS ir Linux operacinėse sistemose.

## Manifesto failo formato specifikacijos

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Pagrindinės skiltys

Pagrindinis skyrius:

* yra informacijos apie JAR failo saugumą ir konfigūraciją

* yra informacijos apie programą arba plėtinį, kurio dalis yra JAR failas

* apibrėžia pagrindinius kiekvieno atskiro manifesto elemento atributus


**Pastaba**: joks atributas šioje skiltyje negali būti pavadintas Vardas.

### Atskiri skyriai

Atskiras skyrius apibrėžia įvairius JAR failo paketų ar failų atributus. Kiekviena sekcija turi prasidėti atributu pavadinimu Pavadinimas, kurio reikšmė turi būti santykinis kelias į failą arba absoliutus URL, nurodantis duomenis už archyvo ribų.

### Manifesto specifikacijos

|Požiūriai|Aprašymas|
---|---|
|manifesto failas|pagrindinės dalies naujoji eilutė *individuali sekcija|
|pagrindinis skyrius|informacija apie versiją nauja eilutė *pagrindinis atributas|
|version-info|Manifesto versija : versijos numeris|
|versijos numeris|skaitmuo+{.skaitmuo+}*|
|main-tribute|(bet koks teisėtas pagrindinis atributas) nauja eilutė|
|individual-section|Vardas : reikšmė nauja eilutė *perentry-atribute|
|perentry-tribute|(bet koks teisėtas nuolatinis atributas) nauja eilutė|
|nauja eilutė|CR LF | LF | CR (ne po LF)|
|skaitmuo|{0-9}|

## Nuorodos

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [JAR failo formatas](https://en.wikipedia.org/wiki/JAR_(file_format))

