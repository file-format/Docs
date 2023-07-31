{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl", "ixbrl fil", "ixbrl filformat", "ixbrl filtyp", "fil", "typ", "vad är en ixbrl fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - Filformat för affärs- och finansiell rapportering",
  "description":"Läs mer om IXBRL-filformat och API:er som kan skapa och öppna IXBRL-filer.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Vad är en iXBRL fil?

iXBRL (ilnine XBRL) filformat låter [XBRL](/sv/finance/xbrl/) data bäddas in i en HTML-fil för att göra den både maskinläsbar och läsbar för människor. Det är faktiskt en [xHTML](/sv/web/xhtml/)-fil som använder XBRL-taggarna och utvecklades av XBRL International för att uppfylla kraven i Storbritanniens HMRC. Med hjälp av iXBRL kan bokslut skapas för att behålla layouten på originaldokumentet intakt. iXBRL-filer kan öppnas i vilken textredigerare som helst som Notepad på Windows operativsystem och TextEdit på MacOS.

## iXBRL filformat

Inne i iXBRL är innehållet i XBRL insvept i xHTML-filformat som använder XML-taggar. Som XBRL,<xbrl> är rotelementet i iXBRL-filer. XHTML-formatet representerar dess innehåll som en samling av olika dokumenttyper och moduler. Alla filer i XHTML är baserade på XML-filformat och överensstämmer med XML-dokumentstandarderna. XHTML är formatet för väsentlig användning för operativt utnyttjande av beroende [HTML](/sv/web/html/) Document Object Model (DOM) eller [XML](/sv/web/xml/) Document Object Model. För omvärlden följer iXBRL filformatspecifikationerna [xHTML](/sv/web/xhtml/).

### iXBRL vs XBRL

XBRL kan jämföras med iXBRL baserat på följande faktorer:

* Komplexitet
* Formateringsalternativ
* Filtyper/tillägg
* Återgivningsalternativ
* Arkiveringsprocessen

Följande tabell illustrerar dessa skillnader.

|Parameter|XBRL|iXBRL|
---|---|---|
|Komplexitet|Mer komplex än iXBRL|Mindre komplex på grund av det befintliga organisationsschemat för XHTML|
|Formateringsalternativ|Begränsad flexibilitet|Hög flexibilitet för innehållsformatering|
|Filtyper/tillägg|Sparat formellt med tillägget .xml|Sparas vanligtvis som tillägget .html eller .xhtml|
|Renderingsalternativ|XBRL-tittare krävs för att se dessa|Människligt läsbart innehåll som kan ses i webbläsare|
|Arkeringsprocess| XBRL (maskinläsbara) och HTML (human readable) instansdokument som ska arkiveras separat.|Både mänskligt läsbara och maskinläsbara format är tillgängliga i ett enda instansdokument|

## Referenser

* [XBRL - av Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

