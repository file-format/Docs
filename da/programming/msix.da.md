{
  "date": "2021-04-22",
  "keywords": [
"msix fil",
"udvidelse",
"format",
"hvordan man åbner filen msix",
"msix filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX - Hvad er en MSIX fil?",
  "description": "Lær om MSIX-filer og API'er, der kan oprette og åbne MSIX-filer.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-dax"
}
},
  "lastmod": "2021-12-16"
}

## Hvad er en MSIX fil?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. Dette er det moderne pakkefilformat sammenlignet med [APPX](/programming/appx/) og MSI, der endeligt vil blive udfaset til dette nye filformat. Det kan bruges til implementering af Win32, WPF og Windows Forms apps. MSIX-filer er pålidelige og målretter netværks- og diskpladsoptimering. Udviklere bruger disse til at distribuere programmer til slutbrugere gennem Microsoft Store (tidligere kendt som Windows Store).

## MSIX-filformat - flere oplysninger

MSIX-filer er [ZIP](/compression/zip/)-komprimerede, med alle filerne inkluderet i den pakkede fil. Ud over de app-relaterede filer indeholder MSIX-filen [.xml](/web/xml/)-konfigurationsfiler, der indeholder oplysninger relateret til app-installationen.

## Hvad er inde i en MSIX-pakke?

En MSIX-pakke består af følgende filer.

 * `AppxBlockMap.xml` - Kendt som pakkeblokkortfilen, er det et XML-dokument, der indeholder en liste over app's filer med indekser og kryptografiske hashes for hver blok af data, der er gemt i pakken.
 * `AppxManifest.xml` - Et XML-dokument, der indeholder de oplysninger, der kræves til implementering, visning og opdatering af en MSIX-app. Disse oplysninger inkluderer pakkeidentitet, pakkeafhængigheder, nødvendige funktioner, visuelle elementer og udvidelsespunkter.
 * `AppxSignature.p7x` - En fil, der genereres, når pakken er signeret. Alle MSIX-pakker skal være underskrevet før installation. Med AppxBlockmap.xml er platformen i stand til at installere pakken og blive valideret.

## Referencer

 * [MSIX-oversigt](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Opret APPX-filer ved hjælp af Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

