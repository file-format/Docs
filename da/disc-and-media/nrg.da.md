{
  "date": "2021-08-16",
  "keywords": [
"nrg fil",
"nrg filformat",
"hvad er en nrg fil",
"fil",
"nrg eksempel",
"nrg filtypenavn",
"udvidelse",
"format",
"nrg sidefod",
"filformat af nrg",
"Nero Burning Rom",
"Nero AG"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om NRG-filformat og API'er, der kan oprette og åbne NRG-filer.",
  "title": "NRG - Disk Image File Format",
  "linktitle": "NRG",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nr-dag"
}
},
  "lastmod": "2021-08-16"
}

## Hvad er en NRG fil?

Et billedfilformat, der er oprettet ved brug af en optisk disk, betragtes som et NRG-filformat. Dette format er specifikt skabt af Nero til brugen af Nero Burning Rom. Til lagring af diskbilleder anses dette format for at være brugt, da det er passende for disse specifikke filer. Disse filer kan være i form af en nøjagtig kopi af en cd eller dvd eller kan have flere filer, der kan monteres som en disk. Andre mere populære filformater såsom [ISO](/compression/iso/) filformater er dem, som disse filer kan konverteres til nogle grundlæggende hjælpeprogrammer. For det meste bruges NRG-filerne til at lave sikkerhedskopier eller kopier af nogle vigtige data eller diske.

## NRG-filformat ##

Dette filformat blev udviklet af Nero AG som et diskimage-format. Det havde den specifikke egenskab af Nero Burning Rom-værktøjet, da det blev udviklet til at gemme diskbilleder. Dens første version blev specificeret til at gemme værdier som 32-bit heltal. Dens anden version blev dog lanceret og indeholdt understøttelse af 64-bit heltal.

## Teknisk specifikation ##

I begyndelsen af filen gemmer dette format ikke sine data som en header. Som en sidefod er den vedhæftet i slutningen af filen. I form af bidder af IFF gemmes informationen om billedet. Forskydningen af den første del kan opnås ved at læse NRG-foden ved de sidste 8 bytes til 12 bytes af filen. I alle versioner af NRG-filformat er der bidder, DAOI, CD-tekst, sessionsinformationsmedietype, diskinformation, Relo og enden af kæden knyttet til det. Byterækkefølgen er big-endian, og alle heltalsværdier er usignerede på lagringstidspunktet.

### Hovedstykker ###

#### Cue Sheet ####

Dette cue-ark er nemt tilgængeligt i alle NRG-filformatversioner. Klumpen af **CUEX** betyder blokkene med sammenkædning af fast størrelse, og hver af disse repræsenterer cue-punktet.

#### DAO-oplysninger ####

Disse oplysninger findes også i alle NRG-formatversioner. Klumperne af **DAOI** gemmer den relevante specifikke information i 2 dele. Dens første del består kun af sessionsspecifikke data. Dens anden del gentager bare den grå information relateret til sporing, og den er kun én gang for hvert spor.

#### CD-tekst ####

Denne findes i NRGs anden version. Klumpen af **CDTX** består af CD-tekstpakkens rå sammenkædning med 18 bytes for hver.

#### Udvidede sporoplysninger ####

Dette er tilgængeligt i alle versioner af filformatet af NRG. Disse bidder bruges til at gemme sporingsinformationen for sporet med en gang session. Disse data gentages kun én gang for hvert spor.

#### Sessionsoplysninger ####

Dette er også tilgængeligt i alle versioner af filformatet af NRG. Oplysningerne om sessionsstykker skal bruges til at scanne sessionens billede hurtigt og derefter spore antallet.

#### End of chain ####

The chunk of end betyder signalerne om, at nu er der ikke flere chunks, der skal læses og dette findes også i NRGs alle versioner.


## Referencer ##

* [NRG - af Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))



