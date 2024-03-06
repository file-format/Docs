{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OAM fails — Adobe Edge animācijas logrīka faila formāts",
  "description" : "Uzziniet, kas ir OAM fails un API, kas var izveidot un atvērt OAM failu.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam-lv",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Kas ir OAM fails?

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
Lietotāji var izveidot OAM failus, publicējot tos no Edge Animate projekta (.AN fails).

## OAM faila formāts

OAM fails tiek saglabāts diskā kā saspiests [ZIP](/compression/zip/) arhīvs. Tas nozīmē, ka varat pārdēvēt faila paplašinājumu uz .zip un izvilkt ar jebkuru saspiešanas utilītu, piemēram, WinZIP vai WinRAR. Samazinātais faila lielums atvieglo animācijas pārsūtīšanu un kopīgošanu ar citiem lietotājiem internetā.

### OAM faila struktūra

.oam faila iekšējā failu struktūra ir patentēta, un Adobe to nav publiski dokumentējusi. Tomēr ir zināms, ka .oam faili satur failu un resursu kolekciju (piemēram, grafiku, audio un ActionScript kodu), kas ir iepakoti vienā failā. .oam faila saturs var ietvert [XML](/web/xml/) failus, SWF failus un citus resursu failus. Precīza .oam faila struktūra ir atkarīga no konkrētās Adobe Animate versijas, kas izmantota tā izveidošanai, kā arī no animācijas veida un failā iekļautajiem līdzekļiem.

OAM failā ir šāda informācija.

Līdzekļi: informācija par animācijā izmantotajiem grafikas, audio un video līdzekļiem.

`Uzvedības:` Animācijā notiekošo darbību un mijiedarbības apraksti.

ActionScript kods: kods, ko izmanto, lai kontrolētu animācijas darbību un interaktivitāti.

Publicēšanas iestatījumi: informācija par platformu un formātu, kādā animācija tiks publicēta, piemēram, HTML5 vai AIR.

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## Kā atvērt OAM failu?

Lai atvērtu OAM failus, varat izmantot šādas lietojumprogrammas.

 * Adobe Edge Animate CC (beigta)
 * Adobe Animate 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## Atsauces

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)


