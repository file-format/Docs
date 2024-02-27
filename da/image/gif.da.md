{
  "date": "2019-10-11",
  "keywords": [
"gif-fil",
"gif filformat",
"hvad er en gif-fil",
"fil",
"gif eksempel",
"gif filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GIF - billedfilformat",
  "description": "Lær om GIF-filformat og API'er, der kan oprette og åbne GIF-filer.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gi-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en GIF-fil? ##

Et GIF eller Graphical Interchange Format er en type meget komprimeret billede. Ejet af Unisys, GIF bruger LZW-komprimeringsalgoritmen, der ikke forringer billedkvaliteten. For hvert billede tillader GIF typisk op til 8 bits pr. pixel, og op til 256 farver er tilladt på tværs af billedet. I modsætning til et [JPEG](/image/jpeg/) billede, som kan vise op til 16 millioner farver og nogenlunde rører grænserne for det menneskelige øje. Dengang internettet dukkede op, forblev GIF'er det bedste valg, fordi de krævede lav båndbredde og kompatible med grafikken, der bruger solide farveområder. En animeret GIF kombinerer adskillige billeder eller rammer til en enkelt fil og viser dem i en sekvens for at generere et animeret klip eller en kort video. Farvebegrænsningerne er op til 256 for hver ramme og vil sandsynligvis være de mindst egnede til at gengive andre billeder og fotografier med farvegradient.

## GIF-filformat ##

Begrebsmæssigt har GIF-filer et grafisk område med fast størrelse fyldt med nul eller flere billeder. Nogle GIF-filer opdeler det eller de grafiske blokke i fast størrelse i underbilleder, der er i stand til at fungere som animerede rammer i tilfælde af animeret GIF. GIF-formatet bruger pixeldybderne på 1 til 8 bits til at gemme bitmapdataene. RGB-farvemodel og paletdata bruges altid til at gemme billederne. Afhængigt af versionen definerer en header med fast længde (GIF87a eller GIF89a) starten på en typisk GIF-fil.

I øjeblikket er to versioner af GIF: 87a og 89a tilgængelige. Førstnævnte er det originale GIF-format, mens sidstnævnte er det nye GIF-format. I dette filformat er karakteristikaene for blokkene og pixeldimensionerne nævnt i en logisk skærmbeskrivelse med fast længde. Eksistensen og størrelsen af en global farvetabel kan angives af skærmbeskrivelsen, som sporer yderligere detaljer, hvis de findes. Traileren er den sidste byte af filen, der indeholder en enkelt byte af et ASCII-semikolon. Et typisk GIF87a-fillayout er som følger:

### Header ###

Headeren rummer seks bytes og bruges til at angive filtypen som GIF. Selvom den logiske skærmbeskrivelse er adskilt fra den faktiske overskrift, betragtes den nogle gange som den anden overskrift. Den samme struktur, som bruges til at gemme overskriften, kan gemme den logiske skærmbeskrivelse. Alle GIF-filer starter med 3-byte-signaturen og bruger tegnene GIF som en identifikator. Versionen er også tre bytes stor og erklærer versionen af GIF-filen.

### Logisk skærmbeskrivelse ###

En billedbeskrivelse med fast længde angiver de skærm- og farveoplysninger, der er nødvendige for at skabe GIF-billedet. Felterne Højde og Bredde omslutter den mindste værdi af skærmopløsning, hvilket er obligatorisk for at vise billeddataene. Hvis displayenheden ikke er i stand til at vise den specificerede opløsning, vil det være nødvendigt med skalering for at vise billedet på passende vis. Skærm- og farvekortoplysninger vises af de fire underfelter i tabellen nedenfor (hvorimod bit 0 er den mindst signifikante bit):


|Bits|Underfelter
---|---|
|0-2|Størrelse af den globale farvetabel
|3|Farvebordsorteringsflag
|4-6|Farveopløsning
|7|Globalt farvetabelflag

#### Global farvetabel ####

En valgfri global farvetabel er placeret lige efter den logiske skærmbeskrivelse. Denne tabel er kortlagt for at indeksere pixelfarvedataene i billeddataene. I mangel af en global farvetabel bruger hvert billede i GIF-filen sin lokale farve. Det er bedre at levere en standardfarvetabel, hvis der mangler både global og lokal farvetabel. En serie af tre-byte tripler komponerer elementerne i farvetabellen. Hver byte karakteriserer en RGB-farveværdi. De røde, grønne og blå farver bruges som værdier for hvert farvetabelelement. Indtastningerne i den globale farvetabel rammer maksimalt 256 poster og repræsenterer altid i en potens af to.

#### Billeddata ####

Billeddataene gemmer en byte af ukodede symboler efterfulgt af en linket liste over under- sammen med de LZW-kodede data.

#### Trailer ####

Trailer repræsenterer en enkelt byte af data, der er det sidste tegn i filen. Værdien af denne byte er permanent 3Bh og angiver slutningen af datastrømmen. Hver GIF-fil skal have traileren i den sidste af hver fil.

## Referencer ##

* [GIF-filformat](https://en.wikipedia.org/wiki/GIF)


