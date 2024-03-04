{
  "date": "2019-12-09",
  "keywords": [
"3mf failas",
"3mf failo formatas",
"kas yra 3mf failas",
"failą",
"3mf pavyzdys",
"3mf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "Sužinokite apie 3MF failų formatą ir API, kurios gali atidaryti ir kurti 3MF failus.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-ltf"
}
},
  "lastmod": "2019-12-09"
}

## Kas yra 3MF failas?

3MF, 3D gamybos formatas, naudojamas programose 3D objektų modeliams pateikti įvairioms kitoms programoms, platformoms, paslaugoms ir spausdintuvams. Jis buvo sukurtas siekiant išvengti apribojimų ir problemų, susijusių su kitais 3D failų formatais, pvz., [STL](/cad/stl/), dirbant su naujausiomis 3D spausdintuvų versijomis. 3MF yra palyginti naujas failo formatas, kurį sukūrė ir paskelbė 3MF konsorciumas. Jis yra pakankamai turtingas, kad būtų galima visiškai apibūdinti modelį, išlaikant vidinę informaciją, spalvą ir kitas charakteristikas, todėl jį galima išplėsti, kad būtų palaikomos naujos 3D spausdinimo naujovės. Formatas yra išplečiamas, gali būti plačiai naudojamas ir neturi problemų, galinčių sukelti kitus plačiai naudojamus failų formatus.

## Trumpa 3MF failo formato istorija

Esami modelių aprašomųjų failų formatų, tokių kaip STL ir kiti, apribojimai verčia pirmaujančius prekių ženklus susiburti ir suformuluoti labiau išplečiamą 3D spausdinimo failo formatą. Svarbus dalykas buvo tai, kaip programos turėtų perduoti modelio duomenis 3D spausdintuvams. Taigi 3MF konsorciumas buvo sukurtas siekiant paremti naują 3D failo formatą, vadinamą 3MF, siekiant, kad jis būtų pakankamai išplėstas, kad atitiktų 3D spausdinimo poreikius. Šiam konsorciumui priklausė kelios įmonės, įskaitant Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP ir kt. Microsoft paaukojo savo 3D failo formato nebaigtą darbą kaip atspirties tašką 3MF konsorciumui bendradarbiaujant toliau plėtojant specifikaciją.

## 3MF failo formatas – daugiau informacijos

3MF yra XML pagrindu sukurtas duomenų formatas – žmogaus skaitomas suglaudintas XML – apimantis su 3D gamyba susijusių duomenų apibrėžimus, įskaitant trečiųjų šalių pritaikytų duomenų išplėtimą. 3MF failo formatas buvo sukurtas atsižvelgiant į apribojimus ir problemas, su kuriomis susiduria kiti 3D failų formatai. Dėl to buvo sukurtas 3MF failo formatas, kuris yra:

* **Užbaigta:** viename archyve yra visa reikalinga modelio, medžiagos ir nuosavybės informacija

* **Žmogaus skaitoma:** naudojant įprastas struktūras, tokias kaip OPC, [ZIP] (/compression/zip/) ir XML, kad būtų lengviau kurti

* **Paprasta:** trumpa, aiški specifikacija, palengvinanti kūrimą ir greitą patvirtinimą

* **Plėstinas:** naudojant XML vardų sritis, galima naudoti tiek viešuosius, tiek privačius plėtinius, išlaikant suderinamumą

* **Nedviprasmiška:** aiškios kalbos ir atitikties testai užtikrina, kad failas visada būtų nuoseklus nuo skaitmeninio iki fizinio

* **Nemokama:** prieiga prie 3MF specifikacijos ir jos įgyvendinimas yra ir visada bus be honorarų, patentų ir licencijų


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## 3MF failo formato specifikacijos

3MF failo formatas savo fiziniam modeliui naudoja Open Packaging specifikacijas ZIP archyvo forma. Jis apima tiksliai apibrėžtą dalių ir ryšių rinkinį, kuris atitinka tam tikrą dokumento paskirtį. Dėl to formatas taip pat atitinka paketo funkciją, įskaitant skaitmeninius parašus ir miniatiūras.

### 3MF dokumentas – apžvalga

Įprastas 3MF dokumentas atrodo taip:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Vardas**|**Aprašas**|**Santykių šaltinis**|**Privaloma / Pasirenkama**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Pagrindinės savybės|OPC dalis, kurioje yra įvairios dokumento ypatybės.|Paketas|PASIRENKAMA
|Skaitmeninio parašo kilmė|OPC dalis, kuri yra paketo skaitmeninių parašų šaknis.|Paketas|PASIRENKAMA
|Skaitmeninis parašas|OPC dalys, kurių kiekvienoje yra skaitmeninis parašas.|Skaitmeninio parašo kilmė|PASIRENKAMA
|Skaitmeninio parašo sertifikatas|OPC dalys, kuriose yra skaitmeninio parašo sertifikatas.|Skaitmeninis parašas|PASIRENKAMA
|PrintTicket|Pateikia nustatymus, kurie bus naudojami išvedant 3D objektą (-us) 3D modelio dalyje.|3D modelis|PASIRENKAMA
|Miniatiūra|Yra mažas JPEG arba PNG vaizdas, vaizduojantis 3D objektus pakete arba visą paketą.|Paketas|PASIRENKAMA
|3D tekstūra|Yra tekstūra, naudojama spalvoms pritaikyti 3D objektui 3D modelio dalyje (galima su plėtiniais)|3D modelis|PASIRENKAMA
|Priskirtos dalys|OPC dalys, susietos su metaduomenimis|Paketas|PASIRENKAMA

Specifikacijų dokumento skyriuose [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) ir [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) pateikiama išsami informacija apie 3MF dokumentą.

## Nuorodos Nr.

* [3MF failo formato specifikacijos](https://github.com/3MFConsortium/spec_core)

* [3MF – Vikipedija](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


