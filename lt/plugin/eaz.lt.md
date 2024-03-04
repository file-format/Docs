{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ failas – kas yra EAZ failas ir kaip jį atidaryti?",
  "description":"Sužinokite apie EAZ failo formatą ir API, kurios gali kurti ir atidaryti EAZ failus.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-ltz"
}
},
  "lastmod" : "2023-12-23"
}

## Kas yra EAZ failas?

EAZ failas yra priedo failas, kurį naudoja ArcGIS Explorer – nemokama ESRI programa, skirta žemėlapių tyrinėjimui, vizualizavimui ir bendrinimui. Jame yra suspaustų failų archyvas, kuriame yra [XML file](/web/xml/), sukompiliuotas kodas ir pagalbiniai failai, reikalingi priedui. Šie failai naudojami norint išplėsti pagrindines programinės įrangos funkcijas, įtraukiant naujus mygtukus, prijungiamus langus ir kitus plėtinius.

## EAZ failo formatas – daugiau informacijos

EAZ failai sukuriami naudojant ArcGIS Explorer SDK – kūrimo rinkinį, skirtą tinkintoms ArcGIS Explorer funkcijoms kurti. Šie failai naudoja [ZIP](/compression/zip/) glaudinimą, kad būtų veiksmingai supakuotas jų turinys. Archyvo centre esantis failas **Addins.xml** yra šakniniame kataloge ir yra esminis komponentas, apibūdinantis įvairius tinkinimus, įterptus į EAZ failą.

Addins.xml failas iš esmės veikia kaip planas, siūlantis įžvalgų apie konkrečius patobulinimus, modifikacijas ir plėtinius, kuriuos EAZ failas pristato ArcGIS Explorer. Naudodami šią išsamią struktūrą kūrėjai gali integruoti ir sklandžiai integruoti naujas funkcijas, mygtukus ir prijungiamus langus, pagerindami bendrą ArcGIS Explorer programos funkcionalumą ir vartotojo patirtį.

## Nuorodos

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
