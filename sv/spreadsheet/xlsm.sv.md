{
  "date" : "2019-12-10",
  "keywords" :[ "XLSM", "fil", "tillägg", "filformat", "Excel-makron", "Öppna" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en XLSM-fil och API:er är som kan skapa och öppna dem.",
  "title" :"Vad är en XLSM-fil?",
  "linktitle" : "XLSM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Vad är en XLSM fil?

Filer med tillägget XLSM är en typ av kalkylbladsfiler som stöder makron. Ur applikationssynpunkt är ett makro en uppsättning instruktioner som används för att automatisera processer. Ett makro används för att registrera de steg som utförs upprepade gånger och underlättar utförandet av åtgärderna genom att köra makrot igen. Makron programmeras med Microsofts Visual Basic for Applications (VBA) från Excel-arbetsboken med hjälp av Visual Basic Editor och kan köras/felsökas direkt därifrån.

XLSM-filer liknar XLM-filformat men är baserade på Open XML-formatet som introducerades i Microsoft Office 2007. Med andra ord, XLSM är [XLSX](/sv/spreadsheet/xlsx/) filer men med stöd för makron. Som standard tillhandahåller Excel själv flera makron för allmänt bruk. Men du kan också spela in dina egna makron med nödvändiga funktioner.

## XLSM - Spela in ett makro ##

Excel ger lättanvända steg för att spela in ett makro. Det kräver att du har utvecklarverktyg installerade för att kunna arbeta med makron. När en makroinspelning är igång, registrerar den varje användaråtgärd för att spelas upp senare. Makroinspelning involverar faktiskt alla steg en användare utför efter att inspelningen startar. Således, om du gör en cells innehåll fetstilt, kursivt och ställer in dess textjustering efter att en makroinspelning har startat, kommer alla dessa kommandon att spelas in. Varje inspelat makro kan också tilldelas en genväg för snabb uppspelning senare. Makroinspelning genererar VBA-kod i form av ett makro som kan redigeras med hjälp av Visual Basic Editor (VBE).

## Referenser ##

* [MS-XLSX filformat](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

