{
  "date" : "2021-04-22",
  "keywords": [ "appxbundle file", "extension", "format","how to open appxbundle file","appxbundle file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"appxbundle - Vad är en APPXBundle-fil?",
  "description":"Läs mer om APPX-filformat och API:er som kan skapa och öppna APPX-filer.",
  "linktitle" : "APPXBUNDLE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-19"
}

## Vad är en APPXBUNDLE fil?

En APPXBUNDLE-fil är en paketfil skapad med [Microsoft Visual Studio](https://visualstudio.microsoft.com/) och används för distribution av Windows-appar (både Desktop och UWP) på [Microsoft Store](https:// www.microsoft.com/en-us/store/apps/windows). Den innehåller en eller flera versioner av en app, inriktad på specifik processorarkitektur som x86, x64 eller ARM. Detta låter slutanvändaren ta emot och distribuera lämplig version av appen baserat på datorarkitekturen. APPXBUNDLE-filer grupperas tillsammans med standardfilformatet [ZIP](/sv/compression/zip/). Microsoft Visual Studios Publish-metod används för att publicera apparna som ett paket. Enstaka paketappar distribueras som [APPX](/sv/programming/appx/)-filer.

## APPXBUNDLE filformat

APPXBUNDLE-filer publiceras i ZIP-filformat. Om du vill se innehållet i apppaketet kan du extrahera innehållet i det med hjälp av dekompressionsverktyg som [WinZIP](https://www.winzip.com/en/) eller WinRAR.

## Referenser

* [Beroendepaket för .appx- och .appxbundle-paket](https://www.ibm.com/docs/en/maas360?topic=catalog-dependency-packages-appx-appxbundle-packages)
* [Skapa APPX-filer med Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

