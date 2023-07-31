{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","vad är en cd-fil","hur man öppnar cd-fil", "tillägg", "fil", "cd-fil","cd-filformat", "cd-filtillägg" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio Class Diagram File",
  "description":"Läs mer om CD-filformat och API:er som kan skapa och öppna CD-filer.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Vad är en CD-fil?

En fil med filändelsen .cd är en Visual Studio-klassdiagramfil som ger information om strukturen och förhållandet mellan alla klasser i den aktuella lösningen. En Visual Studio-lösning (representerad av [.sln](/sv/programming/sln/)) kan innehålla ett eller flera projekt, som vart och ett har flera olika klasser. Klassdiagramfilen kan genereras genom att högerklicka på projektet och välja alternativet klassdiagram.

## Klassdiagram (.cd) Filformat - Mer information

En klassdiagramfil sparas i standard XML-filformat som representerar klasser i ett projekt som XML-noder. Om Visual Studio inte är tillgängligt kan dessa klassdiagramfiler öppnas i alla applikationsprogram som stöder öppning av XML-filer.

### Hur man lägger till klassdiagram till Visual Studio Project

I Visual Studio öppnar du lösningen/projektet som du vill lägga till klassdiagrammet för. Högerklicka sedan på projektnoden och välj sedan Lägg till > Nytt objekt. Eller tryck på Ctrl+Skift+A.

* Dialogrutan Lägg till nytt objekt öppnas.

* Expandera Gemensamma objekt > Allmänt och välj sedan Klassdiagram från malllistan. För Visual C++-projekt, leta i kategorin Utility för att hitta klassdiagrammallen.

### Exportera klassdiagram (CD) till bilder

Visual Studio gör det möjligt att konvertera/exportera klassdiagram till bilder som [PNG](/sv/image/png/), [JPEG](/sv/image/jpeg/) och [BMP](/sv/image/bmp/). Dessa exporterade klassdiagramfiler kan användas för dokumentation och teknisk datapaket (TDP) journalföring. För att konvertera ett klassdiagram till bild kan följande steg användas från Microsoft Visual Studio.

1. Öppna din klassdiagram (.cd)-fil.
1. Från menyn Klassdiagram eller genvägsmenyn för diagramytan, välj Exportera diagram som bild.
1. Välj ett diagram.
1. Välj det format du vill ha.
1. Välj Exportera för att avsluta exporten.

## Referenser

* [Designklasser i Visual Studio](https://learn.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

