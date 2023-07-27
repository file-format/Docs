{
  "date" : "2021-01-21",
  "keywords" :[ "ai-fil", "ai-filformat", "vad är en ai-fil", "fil", "ai-exempel", "ai filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Adobe Illustrator Artwork File",
  "description":"Läs mer om AI-filformat och API:er som kan skapa och öppna AI-filer.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## Vad är en AI-fil?

En fil med filtillägget .ai är en Adobe Illustrator Artwork-fil som innehåller vektorgrafik på en enda sida. den använder punkter för att skapa vägar för att visa bilddata, vilket gör det säkert från att förlora bildkvalitet om den förstoras. AI-filformatet är baserat på PGF-filformatet som liknar AI-filer. AI-formatet har sin huvudsakliga användning för logotyper och tryckta medier, och dess ursprungliga versioner ansågs likna den för [EPS](/sv/page-description-language/eps/)-filer. AI-filer kan öppnas med verktygen Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro och CorelDraw Graphics.

## AI filformat

AI är Adobe Illustrators proprietära filformat och använder den dubbla sökvägen som liknar PGF för att spara EPS-kompatibla filer. [Adobe Illustrator filformatsspecifikationer](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) tillhandahåller en detaljerad utvecklarens referens för interna detaljer om detta filformat. Alla dokument (filer) som skapats av Adobe Illustrator är PostScript-språkdokument och har två huvuddelar som överensstämmer med dokumentstruktureringskonventionerna: en "prolog" och ett "script".

### Prolog

Prologsektionen kapslar in information som krävs för tolkning av filen. Ett exempel skulle vara begränsningsrutan som innehåller alla märken på sidan. Den innehåller också resursinformation som typsnitt och procedurdefinitioner. Dessa resurser är logiskt grupperade i uppsättningar som kallas procset och innehåller explicita metoder för att initiera och avsluta deras procedurer.

### Skript

Grafiska element på sidan beskrivs av skriptet. Ett skript innehåller referenser till operatorerna och procedurerna i prologen, tillsammans med operander och data. De tre logiska delarna av ett skript inkluderar:

* Setup Sequence - som initierar och aktiverar de resurser som definieras i prologen
* Sekvens av beskrivande operatorer
* Trailer som inaktiverar resurser

Operatörer i skriptet är sekvenser av grafiska element skrivna på det språk som definieras av procets i prologen. Dessa sekvenser består av samlingar av dataelement, grafiska attributdefinitioner och anrop till de procedurer som definieras i procseten.

### Objekttaggar

Objekttaggar används för att bifoga anpassad information till ett Adobe Illustrator-konstobjekt. Taggar består av en:

* Taggidentifierare
* Taggtyp
* Data

## Referenser
* [Adobe Illustrator filformatspecifikationer](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [AI-filformat av PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

