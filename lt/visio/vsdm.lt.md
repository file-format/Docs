{
  "date" : "2019-10-11",
  "keywords" : [ "vsdm file", "vsdm file format", "what is a vsdm file", "file", "vsdm example", "vsdm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDM – „Microsoft Visio“ piešinio failo formatas",
  "description":"Sužinokite apie VSDM failo formatą ir API, kurios gali kurti ir atidaryti VSDM failus.",
  "linktitle" : "VSDM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsdm-lt",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas yra VSDM failas?

Failai su .vsdm plėtiniu yra piešimo failai, sukurti naudojant Microsoft Visio programą, kuri palaiko makrokomandas. VSDM failai yra OPC / XML brėžiniai, panašūs į VSDX, bet taip pat suteikia galimybę paleisti makrokomandas, kai failas atidaromas. Makrokomandos yra vartotojo apibrėžti veiksmai / žingsniai, sukurti Visual Basic for Applications (VBA) ir gali būti naudojami atliekant pasikartojančias užduotis. VSDM failų formatas buvo pristatytas paleidus Microsoft Visio 2013. Visio failai naudojami kuriant brėžinius, kuriuose yra vaizdinių objektų, srautų diagramos, UML diagramos, informacijos srautas, organizacinės diagramos, programinės įrangos diagramos, tinklo išdėstymas, duomenų bazių modeliai, objektų žemėlapiai ir kt. panašią informaciją. Failai, sukurti naudojant Visio, taip pat gali būti eksportuojami į skirtingus failų formatus, pvz., [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ir kitus.

## VSDM failo formatas

VSDM failai yra pagrįsti atvirojo pakavimo konvencijomis ir XML, o kūrėjai gali pasinaudoti šiuo formatu, išmokę dirbti su šiais failais programiškai. Formatas paveldi daug tų pačių XML struktūrų kaip ir jo dalys iš Visio XML Drawing failo formato (.vdx). Sąveika su Visio failais labai padidėja, nes trečiosios šalies programinė įranga gali manipuliuoti Visio failais failo formato lygiu.

Kiekvienas Visio failas vadinamas paketu, kuriame yra kiti failai ar dalys. Paketo dalis gali būti XML failas, vaizdas ar net VBA sprendimas. Paketo dalys gali būti suskirstytos į dokumento ir ryšio dalis.

### Dokumentas ###

Dokumento dalyse yra tikrasis Visio failo turinys ir metaduomenys, pvz., failo pavadinimas, pirmasis puslapis ir visos jame esančios figūros ir netgi figūrų duomenų ryšiai. Paketo vaizdai ir tekstiniai failai laikomi dokumento dalimis.

### Santykiai ###

Visio failo santykių dalys saugomos aplanke \_rels ir aprašoma, kaip paketo dalys yra susijusios su kiekviena. Taip pat pateikiama failo struktūra. Atskiras XML dokumentas naudoja elementų pirminį ir antrinį ryšį, kad nustatytų objektų ryšį vienas su kitu. Tinkamame Visio 2013 failo formate yra tinkamas dalių rinkinys, o pakete yra dalių ryšiai.

Ryšių dalys yra XML dokumentai, apibūdinantys ryšius tarp skirtingų paketo dokumentų dalių. Jie apibrėžia ryšį tarp dviejų elementų: nurodyto šaltinio (apibrėžto pagal ryšio failo pavadinimą ir vietą) ir nurodytos tikslinės dokumento dalies. Pavyzdžiui, ryšių dalys naudojamos apibūdinti, kurios formos šablonai yra susieti su failu, kaip puslapiai yra susiję su failu ir vienas su kitu arba kaip vaizdai ir objektai yra susiję su konkrečiu puslapiu.

## Nuorodos Nr.

* [Įvadas į „Visio“ failo formatą](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


