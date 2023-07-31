{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES - C++ gecompileerd bronscript",
  "description":"Meer informatie over RES-bestandsindeling met RES-voorbeeld en API's die RES-bestanden kunnen maken en openen.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Wat is een RES-bestand?
Het bestand met het achtervoegsel of de extensie .res kan tot veel bestandsindelingscategorieën behoren. Hier bespreken we het RES-bestandsformaat dat een C++ Compiled Resource Script is; een binair bestand gemaakt door de Microsoft Resource Compiler (rc) dat brongegevens bevat; gebaseerd op de inhoud van het brondefinitiebestand; relevant zijn voor het moedersoftwareproject. Het .res-bestand wordt meestal opnieuw geformatteerd in een bronobjectbestand om het te koppelen aan het uitvoerbare bestand van een toepassing.

## RES-bestandsindeling
Het RES-bestandsformaat behoort tot de Microsoft Resource Compiler (rc). De broncompiler is een hulpmiddel dat bronnen zoals cursors, pictogrammen, menu's en dialoogvensters compileert die door uw toepassing worden gebruikt. De bronbestanden hebben meestal de extensie .res; bevat bronnen, zoals cursors, afbeeldingen en versie-informatie. Een RES-bestand kan een 16- of 32-bits bronbestand zijn.
## Structuur van bronbestand
Een bronbestand bevat een reeks verschillende bronvermeldingen. Elk item bevat een resourceheader en relevante gegevens. Een bronheader is meestal DWORD-uitgelijnd in het bestand en bevat het volgende:

- Een **DWORD** om de grootte van de resourceheader op te geven
- Een **DWORD** om de grootte van de brongegevens op te geven
- Het brontype
- De naam van de bron
- Aanvullende informatie over bronnen

De structuur van de resourceheader definieert het formaat van het RES-bestand. De gegevens voor de resource volgen de resourceheader. Sommige bronnen voegen ook een bronspecifiek groepskoppatroon toe om informatie te geven over een groep bronnen. Hieronder volgen enkele typen resource-items en hun beschrijving:

### Versnellingstabelbronnen
Een acceleratortabel is een bronvermelding in een RES-bestand zonder een groepskoptekst. Het patroon **ACCELTABLEENTRY** definieert elk item in de acceleratortabel. Een RES-bestand kan meerdere acceleratortabellen hebben.

### Cursor- en pictogrambronnen
Hoewel, het systeem beschouwt elk pictogram en elke cursor als een enkel bestand, maar deze worden opgeslagen in RES-bestanden als een groep pictogrambronnen of een groep cursorbronnen. De bestandsindelingen van pictogram- en cursorbronnen zijn hetzelfde. Een resourcegroepkop volgt alle afzonderlijke pictogram- of cursorgroepcomponenten in het .res-bestand.

### Dialoogvensterbronnen
Een dialoogvenster wordt ook gerealiseerd als een resource-item in het RES-bestand. Het bevat één **DLGTEMPLATE**-dialoogvensterkoppatroon en één **DLGITEMTEMPLATE**-patroon voor elk specifiek besturingselement in het dialoogvenster. De **DLGTEMPLATEEX** en de **DLGITEMTEMPLATEEX** patronen verklaren het formaat van uitgebreide dialoogvensterbronnen.

### Bronnen voor lettertypen
Een menubron bevat een **MENUHEADER** patroon en vervolgens een of meer **NORMALMENUITEM** of **POPUPMENUITEM** patronen, één voor elk menu-item in de menusjabloon. De **MENUEX_TEMPLATE_HEADER** en de **MENUEX_TEMPLATE_ITEM** patronen verklaren het formaat van uitgebreide menubronnen.

### Bronnen voor berichtentabel
Een berichtentabel bestaat uit opgemaakte tekst voor weergave als foutbericht of in een berichtvenster. Het belangrijkste patroon in een berichtentabelbron is de **MESSAGE_RESOURCE_DATA**-structuur.

### Versiebronnen
Het hoofdpatroon in een versiebron is de **VS_FIXEDFILEINFO**. Aanvullende patronen zijn onder meer de **VarFileInfo** om taalgerelateerde gegevens op te slaan, en **StringFileInfo** voor aangepaste tekenreeksinformatie.




## Referenties

* [Bronbestandsindelingen](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 



