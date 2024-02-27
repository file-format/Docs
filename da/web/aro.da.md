{
  "date": "2021-12-09",
  "keywords": [
"aro",
".aro-fil",
"aro filformat",
"en filtype",
"fil",
"type",
"hvad er en .aro-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARO-filformat - SteelArrow-webapplikationsfil",
  "description": "Lær om, hvad en ARO-fil og API'er er, der kan oprette og åbne ARO-filer.",
  "linktitle": "ARO",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ar-dao"
}
},
  "lastmod": "2021-12-09"
}

## Hvad er ARO fil?

En ARO-fil er en websidefil på serversiden, der er genereret med SteelArrow Web Application. Den indeholder [HTML](/web/html/) og SteelArrow tags og scripts. Disse udføres på serveren for at generere en komplet svarside, før de sendes til brugerens browser. ARO-filer indeholder næsten 95% af HTML-indhold, mens de resterende består af SteelArrow-kode. For at ARO-filer skal fungere for dig, skal SteelArrow Web Applications-serveren være installeret og køre på webservermaskinen.

## ARO filformat

ARO files are written in HTML markup language file with embedded JavaScript code and Java applets. [SteelArrow tags](http://www.steelarrow.com/docs/basics1.aro) are the basic building blocks for development of web pages. Though these don't change the display of the page, they are used to fill the page with data. In addition, they may also be used to control the output with conditional statements.

### Eksempel på ARO-tag

Det<SAOUTPUT> ARO-tag lader udviklere udskrive dataværdier hvor som helst i et script. For eksempel kan den bruges til at få output fra PARAM-tabellen med<SAOUTPUT VALUE=PARAM[]> som kan vises i HTML<BODY> tag.

## Referencer

* [SteelArrow tags](http://www.steelarrow.com/docs/basics.aro)

