{
  "date" : "2019-10-11",
  "keywords" : [ "vstm file", "vstm file format", "what is a vstm file", "file", "vstm example", "vstm file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "VSTM – „Microsoft Visio“ šablono failo formatas",
  "description":"Sužinokite apie VSTM failo formatą ir API, kurios gali kurti ir atidaryti VSTM failus.",
  "linktitle" : "VSTM",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vstm-lt",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}

## Kas yra VSTM failas?

Failai su VSTM plėtiniu yra šabloniniai failai, sukurti naudojant Microsoft Visio, palaikantys makrokomandas. Skirtingai nuo VSDX failų, iš VSTM šablonų sukurti failai gali paleisti makrokomandas, sukurtas Visual Basic for Applications (VBA) kodu. Galima sukurti šablono failą, kad būtų pateikti pagrindiniai dokumento nustatymai, kurie gali būti naudojami kuriant kitus dokumentus su šiais parametrais. Visio failai naudojami kuriant brėžinius, kuriuose yra vaizdiniai objektai, srautų diagramos, UML diagramos, informacijos srautas, organizacinės diagramos, programinės įrangos diagramos, tinklo išdėstymas, duomenų bazių modeliai, objektų žemėlapiai ir kita panaši informacija. Failai, sukurti naudojant Visio, taip pat gali būti eksportuojami į skirtingus failų formatus, tokius kaip PNG, BMP, PDF ir kt.

## Dokumento formatas ##

VSTM failai yra pagrįsti atvirojo pakavimo konvencijomis ir XML, o kūrėjai gali pasinaudoti šiuo formatu, išmokę dirbti su šiais failais programiškai. Formatas paveldi daug tų pačių XML struktūrų kaip ir jo dalys iš Visio XML Drawing failo formato (.vdx). Sąveika su Visio failais labai padidėja, nes trečiosios šalies programinė įranga gali manipuliuoti Visio failais failo formato lygiu.

Kiekvienas Visio failas vadinamas paketu, kuriame yra kiti failai ar dalys. Paketo dalis gali būti XML failas, vaizdas ar net VBA sprendimas. Paketo dalys gali būti suskirstytos į dokumento ir santykių dalis.

### Dokumentas ###

Dokumento dalyse yra tikrasis Visio failo turinys ir metaduomenys, pvz., failo pavadinimas, pirmasis puslapis ir visos jame esančios figūros ir netgi figūrų duomenų ryšiai. Paketo vaizdai ir tekstiniai failai laikomi dokumento dalimis.

### Santykiai ###

Visio failo santykių dalys saugomos aplanke _rels ir aprašoma, kaip paketo dalys yra susijusios su kiekviena. Taip pat pateikiama failo struktūra. Atskiras XML dokumentas naudoja elementų pirminį ir antrinį ryšį, kad nustatytų objektų ryšį vienas su kitu. Tinkamame Visio 2013 failo formate yra tinkamas dalių rinkinys, o pakete yra dalių ryšiai.

Ryšių dalys yra XML dokumentai, apibūdinantys ryšius tarp skirtingų paketo dokumentų dalių. Jie apibrėžia ryšį tarp dviejų elementų: nurodyto šaltinio (apibrėžto pagal ryšio failo pavadinimą ir vietą) ir nurodytos tikslinės dokumento dalies. Pavyzdžiui, ryšių dalys naudojamos apibūdinti, kurios formos šablonai yra susieti su failu, kaip puslapiai yra susiję su failu ir vienas su kitu arba kaip vaizdai ir objektai yra susiję su konkrečiu puslapiu.

## Nuorodos Nr.

* [Įvadas į „Visio“ failo formatą](https://learn.microsoft.com/en-us/office/client-developer/visio/introduction-to-the-visio-file-formatvsdx)


