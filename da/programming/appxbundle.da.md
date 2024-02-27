{
  "date": "2021-04-22",
  "keywords": [
"appxbundle-fil",
"udvidelse",
"format",
"hvordan man åbner en appxbundle fil",
"appxbundle filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "appxbundle - Hvad er en APPXBundle-fil?",
  "description": "Lær om APPX-filformat og API'er, der kan oprette og åbne APPX-filer.",
  "linktitle": "APPXBUNDLE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-appxbundl-dae"
}
},
  "lastmod": "2021-12-19"
}

## Hvad er en APPXBUNDLE fil?

En APPXBUNDLE-fil er en pakkefil oprettet med [Microsoft Visual Studio](https://visualstudio.microsoft.com/) og bruges til distribution af Windows-apps (både Desktop og UWP) på [Microsoft Store](https://apps.microsoft.com/store/apps). Den indeholder en eller flere versioner af en app, målrettet mod specifik processorarkitektur såsom x86, x64 eller ARM. Dette giver slutbrugeren mulighed for at modtage og implementere den relevante version af appen baseret på computerarkitekturen. APPXBUNDLE-filer er grupperet sammen ved hjælp af standardfilformatet [ZIP](/compression/zip/). Microsoft Visual Studios Publish-metode bruges til at udgive apps som en pakke. Enkeltpakkeapps distribueres som [APPX](/programming/appx/) filer.

## APPXBUNDLE filformat

APPXBUNDLE-filer udgives i ZIP-filformat. Hvis du vil se indholdet af apppakken, kan du udtrække indholdet af den ved hjælp af dekomprimeringsværktøjer såsom [WinZIP](https://www.winzip.com/en/) eller WinRAR.

## Referencer

 * [Dependency packages for .appx and .appxbundle packages](https://www.ibm.com/docs/en/maas360?topic=catalog-dependency-packages-appx-appxbundle-packages)
 * [Opret APPX-filer ved hjælp af Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

