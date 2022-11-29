{
  "date" : "2022-01-12",
  "keywords" :[ "ica-fil", "ica-filformat", "vad är en ica-fil", "fil", "ica-exempel", "ica-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICA - Citrix ICA-fil",
  "description":"Läs mer om ICA-filtillägg och API:er som kan skapa och öppna ICA-filer.",
  "linktitle" : "ICA",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Vad är ICA fil?

En fil med ica-tillägg är en konfigurationsfil som skapas baserat på Independent Computing Architecture. Den används av Citrix applikationsservrar och innehåller konfigurationsinformation om kopplingen mellan olika servrar. ICA-filer kan innehålla länkar till en värdapplikation eller i vissa fall till en stationär server för fjärranslutning. Dessa är textfiler som kan skapas, redigeras och visas med vilken textredigerare som helst som Microsoft Notepad, Notepad++ eller Apple TextEdit.

## ICA Filformat - Mer information

ICA-filer lagras på skiva i vanlig textformat och är lätt att läsa av människor. ICA-filer anger parametrarna som klientapplikationerna för fjärrskrivbordsklienter, som Citrix Receiver, använder för att ansluta till applikationer som finns på virtuella fjärrskrivbord.

ICA-filer bör överensstämma med vissa initialiseringar och format för att lyckas med anslutning. Dessa nämns i [Inställningsreferens för Citrix ICA](http://support.citrix.com/proddocs/topic/ica-settings/ica-settings-wrapper.html) och inkluderar fält som:

* Ingångskodning
* TCP webbläsaradress
* Transparent nyckelpassering
* Versionsinformation
* Programnamn och adress, och flera andra.
 

## Referenser

* [Förstå ICA-filinnehåll](https://docs.eggplantsoftware.com/epp/9.0.0/ePP/cvuunderstanding_ica_file_contents.htm)
* [Inställningsreferens för Citrix ICA](http://support.citrix.com/proddocs/topic/ica-settings/ica-settings-wrapper.html)

