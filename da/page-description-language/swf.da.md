{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "keywords": [
"SWF",
"fil",
"udvidelse",
"format",
"videoformat",
"Hvad er en SWF-fil",
"swf filformat",
"swf fil afspiller",
"hvordan man åbner en swf fil"
],
  "title": "SWF-fil - Shockwave Flash-filmfilformat",
  "description": "Lær om, hvad en SWF-fil og API'er er, der kan oprette og vise, hvordan du åbner SWF-filen.",
  "linktitle": "SWF",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sw-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en SWF fil?

En SWF-fil er en animationsfil, der er oprettet med Adobe Flash. Det kan indeholde forskellige typer elementer såsom tekst, vektorbilleder, rasterbilleder, actionscripts, objekter såsom cirkler, linjer, firkanter og rektangel for at skabe animationen. SWF-filer arrangerer disse multimedieelementer i rammer, der kan afspilles på forskellige billeder pr. sekund (fps). SWF betyder Short Web File, men er også kendt for Shockwave Format.

Programmer, der kunne *åbne SWF-filer**, inkluderede Adobe Flash Player (nu udgået) og Eltima Elmedia Player.

## SWF-filformat - flere oplysninger

SWF-filer blev brugt til at blive gemt som binære filer på disk. SWF-filformatet blev brugt til at udvikle animationer og spil, der kunne indlejres på websteder og spilles selvstændigt. Det understøttede også videoer og lyde, der gav udviklere en masse valgmuligheder for at skabe interaktive multimedieapplikationer. SWF-filer kan afspilles i webbrowsere, der har Adobe Shockwave installeret. Adobe Flash blev udgået i december 2020 på grund af dets mangler og sikkerhedsproblemer.

## Kort historie om SWF-filformat

SWF-filformatet blev oprindeligt designet af FutureWave Software til at vise animationer med den hensigt at køre på en afspillersoftware på ethvert system med langsommere netværksforbindelser, mens filstørrelsen holdes lille. I december 1996 ejede Macromedia FutureWave og konverterede til Macromedia Flash 1.0.

In 2005, Macromedia was acquired by Adobe, who announced the SWF as a part of its open source project in 2008. I løbet af samme år udgav Adobe kode til verdens populære webmotorer for at give dem mulighed for at crawle og indeksere SWF-filer. Men da SWF-filer ser ud til at blive et standardformat til udgivelse af Flash-indhold på internettet, er SWF'en blevet revideret til at betyde Small Web Format.

## SWF-filstruktur

Sti er det grundlæggende grafiske element i SWF, som er en sekvens af segmenter af grundlæggende elementer, der spænder fra simple linjer til Bezier-kurver. Disse enkle elementer hjælper også med at lave andre ekstra primitiver som terninger, ellipser og endda tekster. De grafiske primitiver i SWF har lighed med de grafiske elementer i andre formater som SVG og MPEG-4 BIFS.

Visningslister og genbrug/omdøbning af allerede definerede elementer er også tilladt af formatet. Det binære stream-format af SWF kan sammenlignes med QuickTime-atomer, som er ens med hensyn til tag, størrelse og nyttelast. Det binære stream-format gør det muligt for ældre spillere at springe over ikke-understøttet indhold. Selvom originale versioner af SWF var begrænset til at tilbyde vektorgrafik og billeder, tillader nye versioner også lyd- og videoindhold.

A new, low-level 3D API of the Flash Player named “Stage3D” was introduced in version 11. Denne API blev tænkt som modstykke til OpenGL eller Direct3D. Stage3D definerer farver i et lavniveausprog kaldet Adobe Graphics Assembly Language (AGAL). Følgende er nogle få grundlæggende datatyper af SWF-filformat.

### Koordinater

XY-koordinater i SWF-filformat gemmes som heltal og måles i en enhed kaldet twip. En twip består af 1/20 af en logisk pixel. Logisk pixel og skærmpixel er den samme, når filen afspilles uden skalering til 100 %.

### Heltalstyper og byterækkefølge

De signerede og usignerede heltalstyper på 8, 16, 32 og 64 bit er tilladt i SWF-filformat. Little-endian byte-rækkefølge bruges til at gemme heltalsværdier. Selvom bitrækkefølgen er inden for bytes, gemmes den i big-endian. Alle heltalsværdier skal være byte-justeret. Signerede heltal er repræsenteret ved at bruge traditionelle 2'er-komplement bitmønstre.

### Fastpunktsnumre

To typer fastpunktsnumre understøttes af SWF-filformatet, dvs. 32 og 16 bit.

### Floating-Point-tal

SWF 8 og nyere versioner bruger tre typer flydende-komma-tal (FLOAT, FLOAT 16, DOUBLE), der er kompatible med IEEE Standard 754 for flydende-komma-typer.

### Kodede heltal

Én type kodet heltal understøttes af SWF 9 og senere med variabelt antal bytes.

## Referencer

* [SWF-filformat](https://en.wikipedia.org/wiki/Swf)


