{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Vad är en MSIX-fil?",
  "description":"Läs mer om MSIX-filer och API:er som kan skapa och öppna MSIX-filer.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Vad är en MSIX fil?

En MSIX-fil är ett Windows-apppaketeringsformat som används för att skapa och distribuera applikationer i Windows 10. Detta är det moderna paketfilformatet jämfört med [APPX](/sv/programming/appx/) och MSI som slutligen kommer att fasas ut till detta nya filformat. Den kan användas för distribution av appar för Win32, WPF och Windows Forms. MSIX-filer är tillförlitliga och riktar sig mot nätverks- och diskutrymmesoptimering. Utvecklare använder dessa för att distribuera program till slutanvändare via Microsoft Store (tidigare känt som Windows Store).

## MSIX-filformat - Mer information

MSIX-filer är [ZIP](/sv/compression/zip/)-komprimerade, med alla filer inkluderade i den paketerade filen. Förutom de apprelaterade filerna innehåller MSIX-filen [.xml](/sv/web/xml/) konfigurationsfiler som innehåller information relaterad till appinstallationen.

## Vad finns i ett MSIX-paket?

Ett MSIX-paket består av följande filer.

* `AppxBlockMap.xml` – Känd som kartfilen för paketblock, det är ett XML-dokument som innehåller en lista över appens filer med index och kryptografiska hash för varje datablock som lagras i paketet.
* `AppxManifest.xml` – Ett XML-dokument som innehåller den information som krävs för distribution, visning och uppdatering av en MSIX-app. Denna information inkluderar paketidentitet, paketberoenden, nödvändiga funktioner, visuella element och utökningsmöjligheter.
* `AppxSignature.p7x` - En fil som genereras när paketet signeras. Alla MSIX-paket måste signeras innan installationen. Med AppxBlockmap.xml kan plattformen installera paketet och valideras.

## Referenser

* [MSIX-översikt](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Skapa APPX-filer med Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

