{
  "date": "2019-10-11",
  "keywords": [
"xoml",
"Fil",
"Udvidelse",
"Filformat",
"Filudvidelse",
"Extensible Object Markup Language"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XOML - Windows Workflow-filformat",
  "description": "Lær om XOML filformat og API'er, der kan oprette og åbne XOML filer.",
  "linktitle": "XOML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xom-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en XOML fil?

XOML er akronym for Extensible Object Markup Language og er et serialiseringsformat for Windows Workflow Foundations workflow-objekter. Baseret på **[XAML](/web/xaml/)**, bruges det mest til at skabe brugergrænseflader i almindelig **[XML](/web/xml/)**. Disse bruges til at erklære arbejdsgangen for brugergrænsefladen og kompileres sammen med den separate fil, der indeholder implementeringslogik. Den indeholder en træbaseret struktur, der definerer en rodarbejdsgangsknude, indlejrede underelementer og indlejrede kodesegmenter. Når en ny arbejdsgang er oprettet med Visual Studio til .NET, har den mulighed for, at du kan vælge, om den skal være i kodeformat eller kodesepareret format. Hvis du vælger den senere, vil IDE'en oprette to filer til dig; en i XOML-format (bestående af workflow-layout og indstillinger), og den anden er i formatet [.CS](/programming/cs/)/[.VB](/programming/vb/), hvor programmeringskoden findes.

