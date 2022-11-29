{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "fil", "tillägg", "filformat", "Excel", "kalkylblad" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en XLS-fil och API:er är som kan skapa och öppna dem.",
  "title" :"Vad är XLS-filformat? Lär dig av filformatsexperter!",
  "linktitle" : "XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Vad är en XLS fil?

Filer med XLS-tillägg representerar Excel Binary File Format. Sådana filer kan skapas av Microsoft Excel såväl som andra liknande kalkylprogram som OpenOffice Calc eller Apple Numbers. Fil som sparas av Excel kallas arbetsbok där varje arbetsbok kan ha ett eller flera kalkylblad. Data lagras och visas för användare i tabellformat i kalkylblad och kan sträcka sig över numeriska värden, textdata, formler, externa dataanslutningar, bilder och diagram. Applikationer som Microsoft Excel låter dig exportera arbetsboksdata till flera olika format inklusive [PDF](/sv/pdf/), [CSV](/sv/spreadsheet/csv/), [XLSX](/sv/spreadsheet/xlsx/), [TXT](/sv/ ordbehandling/txt/), [HTML](/sv/web/html/), [XPS](/sv/page-description-language/xps/) och flera andra. XLS-filformatet ersattes med ett mer öppet och strukturerat format, XLSX, med lanseringen av Microsoft Excel 2007. De senaste versionerna ger fortfarande stöd för att skapa och läsa XLS-filer, även om XLSX är förstahandsvalet för användning nu.

## Kortfattad bakgrund

XLS skapades av Microsoft för användning med Microsoft Excel och är även känt som Binary Interchange File Format (BIFF). Denna filtyp introducerades för första gången genom att göra den till en del av Excel för Windows 1987. XLS-filformatsspecifikationer offentliggjordes för den första i juni 2008 som Revision 1. Därefter uppdaterades specifikationerna kontinuerligt och den senaste versionen tillgänglig är från och med augusti 2018 som är markerad som Revision 8.0. En kort historik över olika versioner av XLS-filformat är som följer:

* Version 7.0 (släppt med office 95): Denna version av excel var den mest robusta och snabbare av alla versioner och interna strömomskrivningar uppdaterades till 32 bitar.
* Version 8 (släppt med office 97): VBA introducerades som ett standardspråk och borttagna naturliga språketiketter införlivades i denna version för första gången. Det introducerade också en kontorsassistent för gem för första gången.
* Version 9 (släppt med office 2000): Det fanns bara mindre ändringar i version 9 där gem kontorsassistent samtidigt kunde hålla flera föremål som tidigare inte var möjliga.
* Version 10 (släppt med office XP): Denna version innehöll inga märkbara förbättringar.
* Version 11 (släppt med office 2003): Stor uppdatering i version 11, excel 2003 var introduktionen av nya tabeller.

## XLS-filformatspecifikationer ##

Data arrangeras i en XLS-fil som binära strömmar i form av en sammansatt fil som beskrivs i [MS-CFB]. Data lagras i den sammansatta filen genom att använda lagringar, strömmar och underströmmar som innehåller information om innehållet och strukturen i en arbetsbok, inklusive arbetsboksdata som kalkylbladsdefinitioner. Varje ström eller underström innehåller en serie binära poster. Varje binär post innehåller noll eller fler strukturerade fält som innehåller arbetsboksdata. Det här avsnittet ger en kort översikt över XLS-filstrukturen, men för detaljerade filformatspecifikationer måste man konsultera [XLS-filformateringsspecifikationerna](https://msdn.microsoft.com/en-us/library/cc313154(v#office) .12).aspx) dokument från Microsoft.

#### Stream och Substream ####

En arbetsbok representeras av arbetsboksströmmen. Varje kalkylblad i en arbetsbok representeras av underströmmar. Dessutom har den Chart Sheet Substream, Macro Sheet Substream eller Dialog Sheet Substream som följer den globala underströmmen. Varje binär ström eller underström som innehåller arbetsboksdata MÅSTE skrivas som en serie binära poster.

#### Spela in ####

Information om funktioner i en arbetsbok lagras som en post som är en sekvens av byte med variabel längd. En binär post består av följande tre komponenter:

**Record Type:** Posttypen är ett tvåbyte osignerat heltal som anger vilken typ av information som specificeras av posten och hur strukturen för postdata som är specifik för denna post är ordnad och strukturerad. Posttypvärden MÅSTE vara ett värde från postuppräkningen (avsnitt 2.3) eller så MÅSTE posten använda den framtida postarkitekturen (avsnitt 2.1.6).

**Record Size**: Poststorleken är ett två-byte osignerat heltal som anger antalet byte som anger den totala storleken på postdata. Poststorleken MÅSTE vara större än eller lika med 0 och MÅSTE vara mindre än eller lika med 8224.

**Record Data:** Postdatakomponenten innehåller fält som motsvarar en viss posttyp och utgör resten av posten. Ordningen och strukturen för fälten för en given posttyp anges i motsvarande avsnitt för den posttypen. Storleken på postdatakomponenten MÅSTE vara lika med poststorleken. Fält i postdatakomponenten kan innehålla enkla värden, matriser av värden, strukturer av flera fält, matriser av fält och matriser av strukturer.

#### Celltabell ####

Celler är de grundläggande blocken i en arbetsbok som lagrar arbetsbokens innehåll som text, formler och numeriska data. Celler upprätthåller register över lagrade data via en datastruktur som kallas celltabellen. Celltabellen i sig lagras i den sekvens av poster som överensstämmer med CELLTABLE-reglerna som definieras i specifikationsdokumentet. Den består av en serie radblock där raderna är ordnade i radblock. Varje radblock innehåller rader från den första raden som innehåller data till den sista raden som innehåller data.

Data eller radformatering sparas i en radpost för varje radblock. Varje cell som innehåller data eller individuell cellformatering representeras av en post. Formatering associerad med en cell kan härledas från individuell cellformatering, radformatering, kolumnformatering eller standardcellformatet. Prioritetsordningen för formatering är individuell cellformatering med högsta prioritet, följt av radformatering och sedan kolumnformatering och sedan standardcellformatet. Celler som inte innehåller data och som inte innehåller individuell formatering sparas inte.

#### Formler ####

En formel är en sekvens av värden, cellreferenser, namn, funktioner eller operatorer i en cell som tillsammans producerar ett nytt värde. Formler lagras i en tokeniserad representation som kallas "parsed expressions". Ett analyserat uttryck konverteras till en textformel vid körning för visning och användarredigering. Cellformler anges av formelposten. Arrayformler specificeras av Array-posten. Delade formler specificeras av ShrFmla-posten.

#### Diagram ####

Diagramarket anger ett diagram, en grafik som visar data eller relationerna mellan datauppsättningar i visuell form, och en diagramdatacache, en lokal kopia av data som används i sjökortsdata saknas eller om länkar till externa datakällor är trasiga. Diagrammet anger grupper med en eller två axlar, en uppsättning axlar som diagramdata plottas mot, och uppsättningen serier, trendlinjer och felstapel som anges i diagrammet. Varje axelgrupp anger en till fyra diagramgrupper som anger vilken typ av visualisering som används för att visa data. Varje serie, trendlinje och felstapel anger en diagramgrupp som den är associerad med.

#### Metadata ####

Metadata är ytterligare data som är associerade med en viss cell eller dess innehåll. Metadata registreras i BIFF8 endast för framtida utökningssyften.

#### Pivottabeller ####

En pivottabell är en mekanism för att sammanfatta källdata för att få en överblick över distributionen av dessa data. I en pivottabell blir tillämpliga kolumner i källdata fält som kan användas för att sammanfatta data. När källdata för pivottabellen är OLAP-källdata, blir OLAP-hierarkier och vissa andra OLAP-enheter fält i pivottabellen.
En pivottabell har två huvuddelar, en pivotcache och en pivottabellvy. Det kan finnas flera pivottabellvyer baserat på en enda icke-OLAP PivotCache.

#### Stilar ####

Den här översikten beskriver hur formaterings- och skyddsinformation för celler i ett ark (1) specificeras. Cellformatering består av flera uppsättningar egenskaper:

* Teckensnittsegenskaper (fet, kursiv, teckensnittsfärg, teckenstorlek, etc...)
* Fyllningsegenskaper (förgrundsfärg, bakgrundsfärg, mönster, gradient, etc...)
* Justeringsegenskaper (vänster-, mitt-, högerjustering, etc...)
* Kantegenskaper (vänster, höger, topp, botten, tjock eller tunn, färg, etc...)
* Egenskaper för nummerformatering (datum, tid, antal decimaler, etc...)
* Skyddsegenskaper (låsta, dolda, etc...)

Dessa egenskaper beskriver som helhet hur en viss cell visas och skrivs ut.

## Referenser ##

* [[MS-XLS] - Excel Binary File Format Structure](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Binärt filformat för sammansatt fil](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

