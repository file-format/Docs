{
  "date": "2022-06-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TPSR-filformat - TeamViewer-pilotsessionsrapportfil",
  "description": "Lær om TPSR filformat og API'er, der kan oprette og åbne TPSR filer.",
  "linktitle": "TPSR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tps-dar"
}
},
  "lastmod": "2022-06-06"
}

## Hvad er en TPSR fil?

En TPSR er en forbindelsesprotokolfil, der bruges af TeamViewer Assist AR (tidligere kendt som TeamViewer Pilot). Oplysninger gemt i en TPSR-fil gemmes i komprimeret [ZIP](/compression/zip/) filformat. TPSR indeholder detaljeret historie om TeamViewer-forbindelse mellem en ekspert og en tekniker til løsning af problem og gennemgangsformål. Oplysninger indeholdt i en TPSR-fil inkluderer enhedstype, navn, Assist AR ID, Expert ID, dato og klokkeslæt og forbindelsens varighed. Disse data er gemt i en [JSON](/web/json/)-fil i det komprimerede TPSR-arkiv.

## TPSR filformat

En TPSR-fil gemmes på disk i ZIP-arkivfilformat, hvor indholdet gemmes i en JSON-fil. Den genereres automatisk efter fuldførelsen af Assist AR-forbindelsen, forudsat at forbindelsesrapporteringsmuligheden er aktiveret i TeamViewer.

TeamViewer Assist AR lader eksperter oprette forbindelse til teknikere for at få LIVE-feed fra den eksterne ende via mobilkameraet. De kan hjælpe teknikerne med at løse problemet over telefonen.

## Åbn TPSR-filer

Du kan åbne TPSR-filer ved hjælp af desktopversionen af TeamViewer-softwaren. Hvis den er installeret på din compture, åbnes den i TeamViewer-softwaren ved at dobbeltklikke på TPSR-filen. TPSR-filer kan også eksporteres til [PDF](/pdf/)-filer eller kan udskrives for at få en udskrevet kopi af protokolfilen.

## Referencer ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)


