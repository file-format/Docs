{
  "date": "2021-01-21",
  "keywords": [
"ai failą",
"ai failo formatas",
"kas yra ai failas",
"failą",
"ai pavyzdys",
"ai failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AI – „Adobe Illustrator“ meno kūrinio failas",
  "description": "Sužinokite apie AI failo formatą ir API, kurios gali kurti ir atidaryti AI failus.",
  "linktitle": "AI",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-a-lti"
}
},
  "lastmod": "2021-01-21"
}

## Kas yra AI failas?

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## AI failo formatas

AI yra patentuotas Adobe Illustrator failų formatas ir naudoja dvigubo kelio metodą, panašų į PGF, kad išsaugotų su EPS suderinamus failus. [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) pateikia išsamią kūrėjo nuorodą, kurioje pateikiama vidinė šio failo formato informacija. Visi Adobe Illustrator sukurti dokumentai (failai) yra PostScript kalbos dokumentai ir turi dvi pagrindines dalis, atitinkančias dokumentų struktūrizavimo konvencijas: prolog ir skriptą.

### Prologas

Prolog skyriuje yra informacija, reikalinga failo interpretavimui. Pavyzdys galėtų būti apribojantis laukelis, kuriame yra visi puslapio ženklai. Jame taip pat yra informacijos apie išteklius, pvz., šriftus ir procedūrų apibrėžimus. Šie ištekliai logiškai sugrupuoti į rinkinius, vadinamus procsets, ir juose yra aiškūs jų procedūrų inicijavimo ir užbaigimo metodai.

### Scenarijus

Puslapio grafiniai elementai aprašomi scenarijaus. Scenarijuje yra nuorodų į operatorius ir procedūras prologe, taip pat operandus ir duomenis. Trys loginės scenarijaus dalys:

 * Setup Sequence – kuri inicijuoja ir suaktyvina prologe nurodytus išteklius
 * Aprašomųjų operatorių seka
 * Anonsas, išjungiantis išteklius

Scenarijaus operatoriai yra grafinių elementų sekos, parašytos prologo procsets apibrėžta kalba. Šios sekos susideda iš duomenų elementų rinkinių, grafinių atributų apibrėžimų ir procetuose apibrėžtų procedūrų iškvietimų.

### Objekto žymos

Objektų žymos naudojamos priskirtai informacijai pridėti prie Adobe Illustrator meno objekto. Žymos susideda iš:

 * Žymos identifikatorius
 * Žymės tipas
 * Duomenys

## Nuorodos
* [Adobe Illustrator failo formato specifikacijos](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)

* [AI failo formatas, sukurtas PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)


