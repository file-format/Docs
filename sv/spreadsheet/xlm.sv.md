{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "fil", "tillägg", "filformat", "Microsoft Excel Macro File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en XLM-makronfil och API:er är som kan skapa och öppna XLM-filer.",
  "title" :"Vad är en XLM-fil?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en XLM fil?

XLM, för Excel Macro, är en typ av kalkylbladsfiler som används för att lagra makron. Ur applikationssynpunkt är ett makro en uppsättning instruktioner som används för att automatisera processer. Ett makro används för att registrera stegen som utförs upprepade gånger för filformatet [XLS](/sv/spreadsheet/xls/) och underlättar utförandet av åtgärderna genom att köra makrot igen. Makron programmeras med Microsofts Visual Basic for Applications (VBA) från Excel-arbetsboken med hjälp av Visual Basic Editor och kan köras/felsökas direkt därifrån.

## Kortfattad bakgrund ##

Microsoft Excel stödde programmering av makron sedan den första offentliga lanseringen. Funktionerna i makron förblev desamma genom efterföljande versioner av Excel med tillägg enligt nya funktioner. XLM var standardmakrospråket för Excel till och med Excel 4.0. Excel 5.0 spelade in makron i VBA som standard men med version 5.0 var XLM-inspelning fortfarande tillåten som ett alternativ. Efter version 5.0 avbröts det alternativet. Alla versioner av Excel, inklusive Excel 2010, kan köra ett XLM-makro, även om Microsoft avråder från att använda dem.

## Spela in ett makro i XLM ##

Excel ger lättanvända steg för att spela in ett makro. Det kräver att du har utvecklarverktyg installerade för att kunna arbeta med makron. När en makroinspelning är igång, registrerar den varje användaråtgärd för att spelas upp senare. Makroinspelning involverar faktiskt alla steg en användare utför efter att inspelningen startar. Således, om du gör en cells innehåll fetstilt, kursivt och ställer in dess textjustering efter att en makroinspelning har startat, kommer alla dessa kommandon att spelas in. Varje inspelat makro kan också tilldelas en genväg för snabb uppspelning senare. Makroinspelning genererar VBA-kod i form av ett makro som kan redigeras med hjälp av Visual Basic Editor (VBE).

## Excel-objektmodell ##

Makron använder VBA-rutiner på baksidan och följer [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) för detta ändamål. Denna modell identifierar objekten i ett kalkylblad för interaktion med kalkylarket genom användardefinierade kommandoverktygsfält, kommandofält eller meddelanderutor. Till exempel beviljas åtkomst till arbetsbokens egenskaper med Workbook-objektet. På samma sätt finns det ett kalkylbladsobjekt i modellen för att arbeta med kalkylbladen i arbetsboken programmatiskt.

## Makron och säkerhet ##

VBA ger tillgång till alla applikationsområden såväl som filsystem och kan också vara farligt. Detta väcker oro när du delar arbetsboken med någon som kan köra filen i slutet. Det är Microsoft Excel varnar för att öppna en sådan fil. Makron kan certifieras med en digital signatur för att andra användare ska kunna verifiera att dessa är pålitliga. Således kan makron aktiveras efter verifiering av deras källa.

## Referenser ##

* [[MS-XLS] - Excel Binary File Format Structure](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Makroprogrammering](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

