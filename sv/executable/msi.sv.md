{
  "date" : "2021-06-30",
  "keywords" :[ "msi-fil", "MSI-filformat", "vad är en msi-fil", "fil", "msi-exempel", "msi-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om MSI-filformat och API:er som kan skapa och öppna MSI-filer.",
  "title" :"MSI - Windows Installer Package File",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Vad är en MSI fil?
En MSI-fil som används för att installera och starta Windows-program; ett komplett paket för Microsoft Windows som innehåller installationsinformation för ett typiskt program, inklusive viktiga filer som ska installeras och information om installationsplatsen. MSI-filerna kan också innehålla paketet för programuppdateringar. MSI-filer liknar [EXE](/sv/körbar/exe/), men EXE inkluderar ibland inte installationsinformationen och programvaran kan köras direkt när EXE-filen körs.

## MSI filformat
Windows Installer är faktiskt ett API (Application Programming Interface) och mjukvarukomponent i Microsoft Windows som används för installation, borttagning och underhåll av ett program. Installationsinformationen och de valfria filerna är paketerade som installationspaket och löst relationsdatabaser strukturerade som COM Structured Storages; välkända som **MSI-filer**, med filtillägget .msi. Paketen med filtillägget **.mst** innehåller **Transformation Scripts** av Windows Installer, filer med tillägget **.msm** innehåller **Merge Modules** och filtillägget **.pcp** används för **Patch Creation Properties**. Windows Installer blir mer avancerat efter att ha gjort betydande ändringar från dess tidigare versioner, Setup API. Ett GUI-ramverk och automatisk generering av avinstallationssekvensen är de nya funktionerna i Windows Installer. Det har nu betraktats som ett alternativ till fristående körbara installationsramverk.

### Logisk struktur för MSI-paket
Ett paket betecknar installationen av en eller flera kompletta produkter och identifieras vanligtvis av en **GUID**. En produkt är uppbyggd av en eller flera komponenter och grupperad i olika funktioner. Windows Installer hanterar inte beroenden mellan olika produkter samtidigt. Den logiska strukturen för paket består av följande element:

- **Produkter**: Ett enda, installerat, fungerande program eller uppsättning av flera program kombinerade tillsammans är en produkt. En produkt identifieras av en unik GUID.
- **Funktioner**: Kan innehålla valfritt antal komponenter och andra underfunktioner. Mindre paket kan bestå av en enda funktion.
- **Komponenter**: Komponent behandlas av Windows Installer som en enhet; kan innehålla programfiler, mappar, registernycklar, COM-komponenter och genvägar.
- **Nyckelsökvägar**: En nyckelsökväg är en specifik fil, ODBC-datakälla eller registernyckel som paketförfattaren anger som kritisk för en given komponent.

## Referenser

* [Windows Installer - av Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


