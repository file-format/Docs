{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OAM failas – „Adobe Edge Animate Widget“ failo formatas",
  "description" : "Sužinokite, kas yra OAM failas ir API, kurios gali sukurti ir atidaryti OAM failą.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam-lt",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Kas yra OAM failas?

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
Vartotojai gali kurti OAM failus publikuodami iš Edge Animate projekto (.AN failo).

## OAM failo formatas

OAM failas išsaugomas diske kaip suspaustas [ZIP](/compression/zip/) archyvas. Tai reiškia, kad galite pervardyti failo plėtinį į .zip ir išskleisti naudodami bet kurią glaudinimo priemonę, pvz., WinZIP arba WinRAR. Sumažintas failo dydis palengvina animacijos perkėlimą ir bendrinimą su kitais vartotojais internetu.

### OAM failo struktūra

Vidinė .oam failo struktūra yra patentuota ir Adobe jos viešai nedokumentuoja. Tačiau žinoma, kad .oam failuose yra rinkinys failų ir išteklių (pvz., grafikos, garso ir ActionScript kodo), supakuotų į vieną failą. .oam failo turinys gali apimti [XML](/web/xml/) failus, SWF failus ir kitus išteklių failus. Tiksli .oam failo struktūra priklauso nuo konkrečios Adobe Animate versijos, naudojamos jam sukurti, taip pat nuo animacijos tipo ir į failą įtrauktų išteklių.

OAM faile yra ši informacija.

Ištekliai: informacija apie animacijoje naudojamus grafikos, garso ir vaizdo išteklius.

Elgesys: animacijoje vykstančių veiksmų ir sąveikų aprašymai.

ActionScript kodas: kodas, naudojamas animacijos veikimui ir interaktyvumui valdyti.

Paskelbimo nustatymai: informacija apie platformą ir formatą, kuriuo bus paskelbta animacija, pvz., HTML5 arba AIR.

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## Kaip atidaryti OAM failą?

Norėdami atidaryti OAM failus, galite naudoti šias programas.

 * Adobe Edge Animate CC (nutrūksta)
 * Adobe Animate 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## Nuorodos

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)


