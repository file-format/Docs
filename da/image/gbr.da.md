{
  "date": "2019-10-11",
  "keywords": [
"gbr fil",
"gbr filformat",
"hvad er en gbr-fil",
"fil",
"gbr eksempel",
"gbr filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GBR-filformat - Gerber-filformat til PCB",
  "description": "Lær om GBR-filformat og API'er, der kan oprette og åbne GBR-filer.",
  "linktitle": "GBR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gb-dar"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er GBR fil?

En fil med filtypenavnet .gbr er et Gerber-billedfilformat til udveksling af designdataoverførsel af printkort (PCB). Det er udviklet af Ucamco. PCB-designdata er den vigtigste komponent, der kræves af fremstillingsindustrien til håndtering. En GRB-fil indeholder PCB-data såsom kobberlag, loddemaske, forklaring og bore- og rutedata. Det kan bruges til at overføre data såsom PCB-fremstillingskarakteristika, herunder tykkelse eller finish i et standardiseret format. Alle PCB-designsystemer udsender Gerber-filer, der kan håndteres af PCB-fremstillingssystemer. GBR-filer er nu blevet de facto-standarden for printet kredsløb (PCB) design dataoverførsel. Ucamco har leveret en [free online viewer](https://gerber-viewer.ucamco.com/) til at åbne og se GBR-filformater.

## GBR filformat

GBR er et UTF-8-format, der kan læses af mennesker, og som kun består af 27 kommandoer. På grund af denne korte liste over kommandoer og dens kompakthed er GBR let at fejlfinde. Gerbers kerne er et åbent vektorformat til 2D binære billeder. Meta-information overføres med billederne via Attributter. En enkelt GRB-fil specificerer et enkelt billede og kræver ikke, at nogen medfølgende filer eller eksterne parametre fortolkes. Et billede behøver kun én fil. Den bruger 7-bit ASCII-tegn til alle kommandoer og navne defineret i specifikationen, som kan udskrives. Dette dækker fuldt ud fuldstændig billedgenerering.

### Eksempel GBR-fil

Følgende er et eksempel på en Gerber-fil, der skaber en cirkel med en diameter på 1,5 mm centreret om oprindelsen. Der er én kommando pr. linje.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referencer

 * [Gerber-format](https://www.ucamco.com/en/gerber)

