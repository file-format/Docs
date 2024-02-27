{
  "date": "2021-03-09",
  "keywords": [
"TCR",
"Psion",
"udvidelse",
"format",
"e-bog"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om TCR-filformat til Psion 3-serien og API'er, der kan oprette og åbne tcr-filer.",
  "title": "TCR - Psion Series 3 e-bogsfil",
  "linktitle": "TCR",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-tc-dar"
}
},
  "lastmod": "2021-03-09"
}

## Hvad er en TCR fil?

I begyndelsen af 90'erne blev TCR-filformatet introduceret til de ældgamle **Psion Series 3** palmtop-enheder. Virksomheden brugte sin platformsspecifikke komprimering, og dette format har meget begrænset understøttelse af tekstformatering. Det er et ZVR-baseret filformat og giver en forholdsvis bedre komprimeringshastighed end PalmDOC. Det fungerer også meget godt med FontMachine. Selvom TCR-filformatet tilhører en udgået enhed, kan dette filformat stadig læses ved at bruge nogle e-læsere. Dette filformat kan også ses på et skrivebord med Sumatra PDF og med Caliber-applikationen i Windows og Linux.

## Tekniske detaljer

Da TCR-filformatet er baseret på en ZVR-kompressor, som er i stand til at reducere mange filer med omkring 50% af deres oprindelige størrelse. Kompressionsskemaet brugt af over er en lille smule gammelt. Den komprimerede fil begynder med en ordbog over de 256 mulige symboler, som kan vises i den komprimerede fil. Ordbogen indeholder en fast alternativ streng for hvert af disse symboler. Dekomprimering er blevet meget hurtig selv i OPL, og den kan begynde på et hvilket som helst tidspunkt i den komprimerede fil.

## Problemer med at åbne en TCR-fil ##

Hvis du ikke er i stand til at åbne og køre filen TCR; det betyder ikke, at du ikke har egnet software installeret på din enhed. Der kan være nogle andre problemer, der forhindrer filen i at fungere korrekt. De mulige problemer kan være et af følgende:

- Korruption af en TCR-fil.
- Forkerte links til TCR-filen i registreringsposter.
- Deleted description of the TCR from the Windows registry
- Ødelagt installation af et program, der understøtter TCR-formatet
- En inficeret TCR-fil med uønsket malware.
- Computeren har ikke tilstrækkelige hardwareressourcer til at betjene filen TCR.
- Drivere, der bruges af computeren til at åbne en TCR-fil, er forældede.




## Referencer

* [TCR - Af MobileRead](https://wiki.mobileread.com/wiki/TCR)

* [ZVR Compressed Text File Reader](https://iay.org.uk/zvr/)


