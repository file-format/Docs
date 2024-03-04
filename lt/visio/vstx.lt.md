{
  "date" : "2019-10-11",
  "keywords" : [ "vstx file", "vstx file format", "what is a vstx file", "file", "vstx example", "vstx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTX – „Microsoft Visio“ failo formatas",
  "description":"Sužinokite apie VSTX failo formatą ir API, kurios gali kurti ir atidaryti VSTX failus.",
  "linktitle" : "VSTX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstx-lt",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas yra VSTX failas?

Failai su .vstx plėtiniais yra piešinių šablonų failai, sukurti naudojant Microsoft Visio 2013 ir naujesnę versiją. Šie VSTX failai yra pradinis taškas kuriant Visio brėžinius, išsaugotus kaip [.VSDX](/visio/vsdx/) failai su numatytuoju išdėstymu ir nustatymais. Apskritai Visio failai naudojami kuriant brėžinius, kuriuose yra vaizdinių objektų, srautų diagramų, UML diagramų, informacijos srautų, organizacinių schemų, programinės įrangos diagramų, tinklo išdėstymo, duomenų bazių modelių, objektų žemėlapių ir kitos panašios informacijos. Failus, sugeneruotus naudojant Visio, taip pat galima eksportuoti į skirtingus failų formatus, pvz., [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ir kitus. Programos, kurios atidaro VSTX failus, apima Microsoft Visio, skirtą Windows ir Mac, leidžiančias atidaryti šiuos failus peržiūrėti ir redaguoti. Tai taip pat leidžia konvertuoti Visio failų formatus į daugybę kitų formatų.

# VSTX failo formatas #

X failo plėtinyje reiškia OpenOffice failo formatą, kurį Microsoft pristatė kaip [ZIP](/compression/zip/) archyvo failo formatą, skirtą pakeisti anksčiau palaikomus dvejetainius failų formatus. Taigi VSTX failai yra pagrįsti OpenOffice specifikacijų XML failo formatu, skirtingai nei [.VST](/visio/vst/) failo formatas, kuris yra dvejetainio formato.

VSDX failai yra pagrįsti atvirojo pakavimo konvencijomis ir XML, o kūrėjai gali pasinaudoti šiuo formatu, išmokę dirbti su šiais failais programiškai. Formatas paveldi daug tų pačių XML struktūrų kaip ir jo dalys iš Visio XML Drawing failo formato (.vdx). Sąveika su Visio failais labai padidėja, nes trečiosios šalies programinė įranga gali manipuliuoti Visio failais failo formato lygiu.

Tam tikri kiti failų tipai, apimantys Visio 2013 failo formatą, apima:

* .vsdm (piešinys su „Visio“ makrokomandomis)

* .vssx („Visio“ trafaretas)

* .vssm („Visio“ makrokomandos įgalintas trafaretas)

* .vstx („Visio“ šablonas)

* .vstm („Visio“ makrokomandos įgalintas šablonas)


Po gaubtu Visio 2013 failo formatas naudoja struktūrizuotas priemones programų duomenims kartu su susijusiais ištekliais saugoti archyve, pvz., [ZIP](/compression/zip/). ZIP failą galima išgauti naudojant bet kurią standartinę ištraukimo programą, kurioje yra ir kitų tipų failų. Galite tiesiog pakeisti .VSTX failo plėtinį .ZIP Windows Explorer, kad pamatytumėte VSTX failo turinį.

Kiekvienas Visio failas vadinamas paketu, kuriame yra kiti failai ar dalys. Paketo dalis gali būti XML failas, vaizdas ar net VBA sprendimas. Paketo dalys gali būti suskirstytos į dokumento ir santykių dalis.

### Dokumentas ###

Dokumento dalyse yra tikrasis Visio failo turinys ir metaduomenys, pvz., failo pavadinimas, pirmasis puslapis ir visos jame esančios figūros ir netgi figūrų duomenų ryšiai. Paketo vaizdai ir tekstiniai failai laikomi dokumento dalimis.

### Santykiai ###

Visio failo santykių dalys saugomos aplanke _rels ir aprašoma, kaip paketo dalys yra susijusios su kiekviena. Taip pat pateikiama failo struktūra. Atskiras XML dokumentas naudoja elementų pirminį ir antrinį ryšį, kad nustatytų objektų ryšį vienas su kitu. Tinkamame Visio 2013 failo formate yra tinkamas dalių rinkinys, o pakete yra dalių ryšiai.

Ryšių dalys yra XML dokumentai, apibūdinantys ryšius tarp skirtingų paketo dokumentų dalių. Jie apibrėžia ryšį tarp dviejų elementų: nurodyto šaltinio (apibrėžto pagal ryšio failo pavadinimą ir vietą) ir nurodytos tikslinės dokumento dalies. Pavyzdžiui, ryšių dalys naudojamos apibūdinti, kurios formos šablonai yra susieti su failu, kaip puslapiai yra susiję su failu ir vienas su kitu arba kaip vaizdai ir objektai yra susiję su konkrečiu puslapiu.

## Nuorodos Nr.

* [Įvadas į „Visio“ failo formatą](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


