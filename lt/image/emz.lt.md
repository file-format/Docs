{
  "date": "2019-10-11",
  "keywords": [
"emz failą",
"emz failo formatas",
"kas yra emz failas",
"failą",
"emz pavyzdys",
"emz failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMZ failo formatas – Windows suspaustas patobulintas meta failas",
  "description": "Sužinokite apie EMZ failo formatą ir API, kurios gali kurti ir atidaryti EMZ failus.",
  "linktitle": "EMZ",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-ltz"
}
},
  "lastmod": "2020-10-24"
}

## Kas yra EMZ failas?

Failas su plėtiniu .emz yra suglaudintas patobulinto metafailo ([EMF](/image/emf/) failo) konteineris. Jie suglaudinami naudojant [GZIP](/compression/gz/) glaudinimo metodą, kuris yra dažniausiai naudojamas glaudinimo metodas UNIX ir LINUX operacinėse sistemose. Atsieti ZIP (/compression/zip/), GZIP suglaudina visą archyvą, o ne atskirus failus. EMZ failai yra mažesnio dydžio, palyginti su EMF failais, ir padeda greitai perkelti failus dalijantis internetu. Kai kurios programos, galinčios atidaryti EMZ failus, yra Microsoft Visio 2019, Microsoft Office 2019, XnView MP ir File Viewer Plus.

## EMZ failo formatas

EMZ failai yra [Gzip](/compression/gz/) suglaudinti ir viduje yra [EMF](/image/emf/). Gzip naudoja DEFLATE algoritmą archyvui suspausti ir skiriasi taikant glaudinimą. EMZ failą galima išspausti naudojant GZip glaudinimo priemones, pvz., GNU Zip. Failo formatas susideda iš:

 * Failo antraštė
 * Pasirenkamos antraštės
 * Suspausti duomenys
 * Failo poraštė

Internet Engineering Task Force (IETF) paskelbtame GZIP failo formate [specifications version 4.3](https://datatracker.ietf.org/doc/html/rfc1952) yra išsami informacija apie failo formatą.

## Nuorodos

 * [RFC1952: GZIP failo formato specifikacija](https://datatracker.ietf.org/doc/html/rfc1952), pateikė [IETF](https://www.ietf.org/)
 * [Windows MetaFile – Vikipedija](https://en.wikipedia.org/wiki/Windows_Metafile)

