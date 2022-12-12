{
  "date" : "2021-06-29",
  "keywords" :[ "XAR", "file", "extension", "file format", "Excel Auto-Recovery File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az XAR fájlformátumról és az API-król, amelyek XAR fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"XAR - Microsoft Excel automatikus helyreállítási fájlformátum",
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
      "identifier": "spreadsheet-xar",
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a XAR fájl?

A .xar kiterjesztésű fájl egy Microsoft Excel Recvoery fájl, amely a fő Excel-táblázatfájlok mellett jön létre. Helyreállítási fájlként használatos, ha az alkalmazás hibásan működik vagy váratlanul bezárul, ami a főfájl adatainak elvesztését eredményezi. Ezeket a helyreállítási fájlokat ugyanabban az eredeti fájlformátumban menti a rendszer a gyorsaság és az egyszerűség érdekében. Az Excel az eredeti fájlformátumot és nevet javasolja a helyreállított fájl újranyitásakor, amelyet a rendszerleíró adatbázisban tárol helyreállítás céljából.

## XAR fájlformátum

Az XAR fájlok bináris fájlformátumban mentett helyreállítási fájlok a fő Excel fájl mellett. Ezeket rejtett fájlokként tárolják a lemezen tetszőleges néven, a rendszerleíró adatbázis fő Excel fájljára hivatkozva. Az összes megnyitott fájl aktívan és időszakonként az alapértelmezett kiterjesztésre menti rejtett XAR-fájlként, és ezeket olyan lemezekre menti, mint például ~ar8EF9.xar.

## Hogyan lehet visszaállítani az Excel fájlt XAR fájlból?

Az XAR fájlok minden típusú Excel fájlformátumot menthetnek, például XLS, XLSX és mások. Ha az Excel-táblázatfájl váratlanul bezárul, megnyithatja az Excelt, vagy kattintson duplán a fájlra, és a rendszer automatikusan kéri, hogy állítsa helyre a mentett helyreállítási fájlt, amelyet az eredetivel azonos néven menthet el oldalirányú használatra.

## Hivatkozások

* [Atuo Recover Functions in Excel](https://docs.microsoft.com/en-us/office/troubleshoot/excel/autorecover-functions-in-excel)
* [XAR File Community Help](https://answers.microsoft.com/en-us/msoffice/forum/msoffice_excel-mso_win10-mso_365hp/2016-excel-xar-files/5af5e10c-027a-4c24-a403-309e8f5909e8f)

