{
  "date": "2023-05-09",
  "keywords": [
"pc3 fil",
"hvad er en pc3-fil",
"hvordan man opretter pc3-fil i AutoCAD",
"hvad er formatet på pc3-filen",
"hvad indeholder pc3-filen",
"fil",
"pc3 filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "PC3-filformat - AutoCAD Plotter-konfigurationsfil",
  "description": "Lær om PC3-format og API'er, der kan oprette og åbne PC3-filer.",
  "linktitle": "PC3",
  "menu": {
    "docs": {
      "identifier": "cad-pc3-da",
      "parent": "cad"
}
},
  "lastmod": "2023-05-09"
}

## Hvad er en PC3 fil?

En PC3-fil i AutoCAD er en plotterkonfigurationsfil, der indeholder printer- eller plotterindstillinger til brug i software.

Når du opretter en ny plotterkonfiguration, gemmer AutoCAD alle nødvendige oplysninger om printer eller plotter i PC3-fil. Dette inkluderer ting som papirstørrelser, margener, opløsning og andre indstillinger, der er specifikke for den printer eller plotter, du bruger.

Du kan bruge PC3-filen til nemt at opsætte og konfigurere en printer eller plotter i AutoCAD. For at bruge PC3-fil skal du blot vælge den fra listen over tilgængelige plotterkonfigurationer i Plot-dialogboksen.

Du kan også oprette brugerdefinerede PC3-filer ved at ændre indstillingerne for eksisterende PC3-fil eller ved at oprette en ny PC3-fil fra bunden ved hjælp af Plotter Manager i AutoCAD.

## Hvordan opretter man PC3-fil i AutoCAD?

Følg disse trin for at oprette plotterkonfigurationsfil (PC3) i AutoCAD:

1. **Åbn Plotter Manager:** Skriv PLOTTERMANAGER i kommandolinjen eller gå til fanen Output på båndet og vælg Plotter Manager fra Plot panelet.
2. **Klik på Add-A-Plotter Wizard:** Dette vil starte en guide, der vil guide dig gennem processen med at oprette en ny plotter-konfigurationsfil.
3. **Vælg plotterproducent og -model:** Guiden vil bede dig om at vælge producent og model af din printer eller plotter fra listen. Hvis din printer eller plotter ikke er på listen, kan du vælge Denne computer og søge efter driverfilen.
4. **Vælg en port:** Vælg den port, som din printer eller plotter er tilsluttet. Hvis du er usikker, så tjek dokumentationen, der fulgte med din printer eller plotter.
5. **Specificer plotterkonfiguration:** Guiden vil bede dig om at angive forskellige indstillinger for din plotter, såsom papirstørrelse, opløsning og farvedybde. Sørg for at indstille disse indstillinger korrekt til din specifikke printer eller plotter.
6. **Gem plotterkonfiguration:** Når du har angivet alle indstillinger, vil guiden bede dig om at give din nye plotterkonfiguration et navn. Dette vil oprette en ny PC3-fil i den mappe, der er angivet af guiden.
7. **Brug den nye plotterkonfiguration:** For at bruge den nye plotterkonfiguration i AutoCAD skal du gå til Plot-dialogboksen, vælge din nye plotterkonfiguration fra listen over tilgængelige plotterkonfigurationer og derefter indstille dit plot som normalt.

Det er det! Du har nu oprettet en ny plotter-konfigurationsfil (PC3) i AutoCAD, som du kan bruge til at printe eller plotte dine tegninger.

## Hvad er formatet på PC3-filen?

PC3-filformatet er et proprietært filformat, der bruges af Autodesks AutoCAD-software. Den indeholder konfigurationsindstillinger for specifik plotter eller printer, herunder papirstørrelse, farvedybde, opløsning og andre muligheder.

PC3-filen er typisk gemt i mappen Plotter Configuration i AutoCAD installationsmappe, og den kan nemt deles mellem brugere eller computere for at sikre ensartede udskrivnings- og plotindstillinger.

PC3-filen er i det væsentlige en tekstfil, der indeholder XML-data, som er et maskinlæsbart format til lagring og udveksling af data. Du kan se og redigere indholdet af PC3-filen ved hjælp af teksteditor eller XML-editor, men det anbefales, at du bruger Plotter Manager i AutoCAD til at foretage ændringer i plotterkonfigurationen, da dette vil sikre, at indstillingerne er korrekt formateret og kompatible med software.

## Hvad indeholder PC3-filen?

En PC3-fil i AutoCAD indeholder printer- eller plotterkonfigurationsindstillinger, der er specifikke for en bestemt enhed eller driver. Disse indstillinger bruges af AutoCAD til at printe eller plotte dine tegninger nøjagtigt og for at sikre, at de ser ud, som du havde tænkt dig.

Her er nogle af de indstillinger, der kan gemmes i en PC3-fil:

- **Papirstørrelse:** Dette angiver papirstørrelsen, der skal bruges til udskrivning eller plotning, såsom A4, Letter eller Custom.
- **Plotområde:** Dette angiver den del af tegningen, der vil blive plottet, såsom hele layoutet eller blot et bestemt vindue.
- **Plotskala:** Dette angiver skalaen, hvormed tegningen vil blive udskrevet eller plottet, såsom 1:100 eller 1/4=1'-0.
- **Linjevægt:** Dette angiver tykkelsen af linjer i tegningen, hvilket påvirker, hvordan de vil se ud, når de udskrives eller plottes.
- **Farvedybde:** Dette angiver antallet af farver, der vil blive brugt til udskrivning eller plotning, såsom sort og hvid eller fuld farve.
- **Opløsning:** Dette angiver den opløsning, ved hvilken tegningen vil blive udskrevet eller plottet, hvilket påvirker, hvor skarp og detaljeret den vil se ud.
- **Andre muligheder:** Der er mange andre muligheder, der kan indstilles i PC3-fil, såsom udskriftskvalitet, orientering, margener, skygge og mere.

Ved at oprette og bruge PC3-fil, der indeholder korrekte indstillinger til din specifikke printer eller plotter, kan du sikre, at dine tegninger bliver printet eller plottet præcist og med ensartet kvalitet.

## Referencer
* [PC3 i AutoCAD](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Creating-plotter-configuration-files-PC3.html)


