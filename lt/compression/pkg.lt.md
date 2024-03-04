{
  "date": "2021-04-08",
  "keywords": [
"pkg failą",
"pkg failo formatas",
"kas yra pkg failas",
"failą",
"pkg pavyzdys",
"pkg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PKG – išplečiamo archyvo failo formatas",
  "description": "Sužinokite apie PKG failo formatą ir API, kurios gali kurti ir atidaryti PKG failus.",
  "linktitle": "PKG",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-pk-ltg"
}
},
  "lastmod": "2021-04-13"
}

## Kas yra PKG failas?

Failas su plėtiniu .pkg yra diegimo programos paketo failas, naudojamas programinei įrangai įdiegti MacOS. Be Macintosh kompiuterių, jis naudojamas ir iPhone. Integruota Apple diegimo programa gali būti naudojama PKG failo turiniui įdiegti. PKG failas yra panašus į MSI failą, naudojamą Windows operacinėje sistemoje programinei įrangai įdiegti. Diegimo metu šie paketo failai gali registruoti pranešimus, kurie suteikia supratimą, kokius papildomus dalykus įdiegė šis paketas.

## PKG failo formatas

PKR yra dvejetainiai failai, kurie suglaudinami siekiant sumažinti bendrą failo dydį. Nuo OSX 10.5 versijos Apple pristatė vienodus paketus su vienu diegimo programos failu. Tai skiriasi nuo ankstesnių pakuočių formatų, kurie buvo pateikti kaip paketai, o ne pavieniai failai. Šiuose susietuose paketuose buvo struktūrizuota katalogų hierarchija, kurioje failai saugomi taip, kad būtų lengviau juos gauti naudojant tam tikrą indekso failą. Plokščiasis PKG failo formatas iš tikrųjų yra [XAR](/compression/xar/) archyvas, kuriame yra:

 * Antraštė – apibrėžia dydį, kontrolinę sumą ir informaciją apie versiją
 * Turinys – XML dokumentas, kuris yra (ir turi būti) užkoduotas kaip UTF-8 ir yra saugomas failo pradžioje, todėl jį lengva nuskaityti per archyvą, kad būtų galima išskirti atskirą failą.
 * Krūva – nestruktūrizuota duomenų krūva, nurodyta TOC

## Nuorodos

* [Flat Package File Format](http://s.sudre.free.fr/Stuff/Ivanhoe/FLAT.html)

* [PKG – Vikipedija](https://en.wikipedia.org/wiki/.pkg)


