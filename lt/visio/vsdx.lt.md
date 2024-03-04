{
  "date" : "2019-10-11",
  "keywords" : [ "vsdx file", "vsdx file format", "what is a vsdx file", "file", "vsdx example", "vsdx file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSDX",
  "description":"Sužinokite apie VSDX failo formatą ir API, kurios gali kurti ir atidaryti VSDX failus.",
  "linktitle" : "VSDX",
  "menu" : {
    "docs" : {
	"identifier":"visio-vsdx-lt",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas yra VSDX failas?

Failai su plėtiniu .vsdx yra Microsoft Visio failo formatas, pristatytas nuo Microsoft Office 2013. Jis buvo sukurtas siekiant pakeisti dvejetainį failo formatą [.VSD](/visio/vsd/), kurį palaiko ankstesnės Microsoft Visio versijos. Jis taip pat palaikomas Microsoft SharePoint Server 2013 Visio Services ir nereikalauja tarpinio failo formato, kad būtų galima paskelbti SharePoint Server. Visio failai naudojami kuriant brėžinius, kuriuose yra vaizdiniai objektai, srautų diagramos, UML diagramos, informacijos srautas, organizacinės diagramos, programinės įrangos diagramos, tinklo išdėstymas, duomenų bazių modeliai, objektų žemėlapiai ir kita panaši informacija. Failus, sugeneruotus naudojant Visio, taip pat galima eksportuoti į skirtingus failų formatus, pvz., [PNG](/image/png/), [BMP](/image/bmp/), [PDF](/pdf/) ir kitus.

## Dokumento formatas ##

VSDX failai yra pagrįsti atvirojo pakavimo konvencijomis ir XML, o kūrėjai gali pasinaudoti šiuo formatu, išmokę dirbti su šiais failais programiškai. Formatas paveldi daug tų pačių XML struktūrų kaip ir jo dalys iš Visio XML Drawing failo formato (.vdx). Sąveika su Visio failais labai padidėja, nes trečiosios šalies programinė įranga gali manipuliuoti Visio failais failo formato lygiu.

Tam tikri kiti failų tipai, apimantys Visio 2013 failo formatą, apima:

* .vsdm (piešinys su „Visio“ makrokomandomis)

* .vssx („Visio“ trafaretas)

* .vssm („Visio“ makrokomandos įgalintas trafaretas)

* .vstx („Visio“ šablonas)

* .vstm („Visio“ makrokomandos įgalintas šablonas)


Po gaubtu Visio 2013 failo formatas naudoja struktūrizuotas priemones programų duomenims kartu su susijusiais ištekliais saugoti archyve, pvz., [ZIP](/compression/zip/). ZIP failą galima išgauti naudojant bet kurią standartinę ištraukimo programą, kurioje yra ir kitų tipų failų. Norėdami pamatyti VSDX failo turinį, galite tiesiog pakeisti .vsdx failo plėtinį .zip.

Kiekvienas Visio failas vadinamas paketu, kuriame yra kiti failai ar dalys. Paketo dalis gali būti XML failas, vaizdas ar net VBA sprendimas. Paketo dalys gali būti suskirstytos į dokumento ir santykių dalis.

### Dokumentas ###

Dokumento dalyse yra tikrasis Visio failo turinys ir metaduomenys, pvz., failo pavadinimas, pirmasis puslapis ir visos jame esančios figūros ir netgi figūrų duomenų ryšiai. Paketo vaizdai ir tekstiniai failai laikomi dokumento dalimis.

### Santykiai ###

Visio failo santykių dalys saugomos aplanke \_rels ir aprašoma, kaip paketo dalys yra susijusios su kiekviena. Taip pat pateikiama failo struktūra. Atskiras XML dokumentas naudoja elementų pirminį ir antrinį ryšį, kad nustatytų objektų ryšį vienas su kitu. Tinkamame Visio 2013 failo formate yra tinkamas dalių rinkinys, o pakete yra dalių ryšiai.

Ryšių dalys yra XML dokumentai, apibūdinantys ryšius tarp skirtingų paketo dokumentų dalių. Jie apibrėžia ryšį tarp dviejų elementų: nurodyto šaltinio (apibrėžto pagal ryšio failo pavadinimą ir vietą) ir nurodytos tikslinės dokumento dalies. Pavyzdžiui, ryšių dalys naudojamos apibūdinti, kurios formos šablonai yra susieti su failu, kaip puslapiai yra susiję su failu ir vienas su kitu arba kaip vaizdai ir objektai yra susiję su konkrečiu puslapiu.

## Nuorodos Nr.

* [Įvadas į „Visio“ failo formatą](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


