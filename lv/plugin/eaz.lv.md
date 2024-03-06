{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ fails — kas ir EAZ fails un kā to atvērt?",
  "description":"Uzziniet par EAZ faila formātu un API, kas var izveidot un atvērt EAZ failus.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-lvz"
}
},
  "lastmod" : "2023-12-23"
}

## Kas ir EAZ fails?

EAZ fails ir pievienojumprogrammas fails, ko izmanto ArcGIS Explorer — ESRI izstrādāta bezmaksas lietojumprogramma karšu izpētei, vizualizācijai un kopīgošanai. Tajā ir saspiests failu arhīvs, kas ietver [XML file](/web/xml/), kompilētu kodu un atbalsta failus, kas nepieciešami pievienojumprogrammai. Šie faili tiek izmantoti, lai paplašinātu programmatūras pamata funkcionalitāti, iekļaujot jaunas pogas, dokojamus logus un citus paplašinājumus.

## EAZ faila formāts — vairāk informācijas

EAZ faili tiek izveidoti, izmantojot ArcGIS Explorer SDK — izstrādes komplektu, kas paredzēts pielāgotu funkciju izveidei programmā ArcGIS Explorer. Šie faili izmanto [ZIP](/compression/zip/) saspiešanu, lai efektīvi iesaiņotu to saturu. Arhīva pamatā **Addins.xml** fails atrodas saknes direktorijā, kalpojot kā būtiska sastāvdaļa, kas izklāsta un apraksta dažādus EAZ failā iegultos pielāgojumus.

Fails Addins.xml būtībā darbojas kā ceļvedis, piedāvājot ieskatu konkrētajos uzlabojumos, modifikācijās un paplašinājumos, ko EAZ fails ievieš ArcGIS Explorer. Izmantojot šo visaptverošo struktūru, izstrādātāji var iekapsulēt un nemanāmi integrēt jaunas funkcijas, pogas un dokojamus logus, uzlabojot lietojumprogrammas ArcGIS Explorer vispārējo funkcionalitāti un lietotāja pieredzi.

## Atsauces

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
