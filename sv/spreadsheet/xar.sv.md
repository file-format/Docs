{
  "date" : "2021-06-29",
  "keywords" :[ "XAR", "fil", "tillägg", "filformat", "Excel Auto-återställningsfil", "kalkylblad" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om XAR-filformat och API:er som kan skapa och öppna XAR-filer.",
  "title" :"XAR - Microsoft Excel Auto-Recovery File Format",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
      "identifier": "spreadsheet-xar",
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är en XAR fil?

En fil med filändelsen .xar är en Microsoft Excel Recvoery-fil som genereras tillsammans med de viktigaste Excel-kalkylbladsfilerna. Den används som en återställningsfil om programmet inte fungerar eller stängs oväntat, vilket resulterar i förlust av data från huvudfilen. Dessa återställningsfiler sparas i samma ursprungliga filformat för snabbhet och enkelhet. Excel föreslår det ursprungliga filformatet och namnet vid återöppning av den återställda filen som den lagrar i systemregistret för återställning.

## XAR filformat

XAR-filerna är återställningsfiler som sparats i binärt filformat på skiva vid sidan av excel-huvudfilen. Dessa lagras som dolda filer på skiva med godtyckliga namn, länkar till huvudexelfilen från systemregistret. Alla öppna filer sparas aktivt och periodiskt till standardtillägget som dolda XAR-filer och dessa sparas på skivor med namn som ~ar8EF9.xar.

## Hur återställer man Excel-fil från XAR-fil?

XAR-filer kan spara alla typer av Excel-filformat som XLS, XLSX och andra. Om din Excel-kalkylbladsfil stängs oväntat kan du öppna Excel eller dubbelklicka på filen och den kommer automatiskt att be dig att återställa från den sparade återställningsfilen som du kan spara med samma filnamn som originalet för lateral användning.

## Referenser

* [Atuo återställningsfunktioner i Excel](https://docs.microsoft.com/en-us/office/troubleshoot/excel/autorecover-functions-in-excel)
* [XAR File Community Hjälp](https://answers.microsoft.com/en-us/msoffice/forum/msoffice_excel-mso_win10-mso_365hp/2016-excel-xar-files/5af5e10c-027a-4c24-a403-39e9c590ce8f)

