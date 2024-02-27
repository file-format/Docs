{
  "date": "2019-10-11",
  "keywords": [
"j2k fil",
"j2k filformat",
"hvad er en j2k fil",
"fil",
"j2k eksempel",
"j2k filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2K",
  "description": "Lær om J2K-filformat og API'er, der kan oprette og åbne J2K-filer.",
  "linktitle": "J2K",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-dak"
}
},
  "lastmod": "2020-08-03"
}

## Hvad er en J2K fil?

En **J2K**-fil er et billede, der er komprimeret ved hjælp af wavelet-komprimering i stedet for DCT-komprimering. Dette filformat bruges af Joint Photographic Experts Group (JPEG) 2000-filer. J2K-filer gemmer metadataoplysninger om billedfilen i XML i modsætning til .jpeg eller .jpg, der bruger EXIF-formatet til dette formål. J2K-filer understøtter 15-bit farve, alfa-gennemsigtighed og tabsfri komprimering. Der findes adskillige kommercielle API'er til at afkode JPEG 2000-billeder såsom J2K-Codec. En J2K-fil kan åbnes på Windows OS ved hjælp af standard billedfremvisere.

## J2K filformat ##

J2K-filformatet er det samme som JPEG 2000, som ofte gemmes som .jp2 og .jpc. Dette får J2K-filer til at følge den samme tilgang til kodning af metadata i XML-format, hvor Standard 12234-1 bruges som reference mellem Exif-tags og XML-komponenterne. Den er yderligere forbedret af JPEG 2000 del-2-udvidelsen, der kombinerer animationsmekanismen og kodestrømskonfigurationerne i ét enkelt billede. Sådanne filer i udvidet filformat gemmes som .jpx.

### Layout af en JPEG2000-fil ###

JPEG2000 understøtter en række applikationer baseret på overensstemmelsen for udvidelige filformater. Selvom den enkleste type kan indeholde et enkelt billede, kan mere komplekse typer omfatte en række billeder, stablet oven på hinanden eller er tidsbaseret sekvenseret.

#### JP2 Box ####
Det er byggestenen på øverste niveau i JP2-filformatet og indeholder en type- og længdefelter i overskriften og en datasektion. Den mest bemærkelsesværdige type boks er den sammenhængende kodestrømsboks. Denne boks gemmer i sin datasektion JPEG2000-kodestrømmen.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream er en sekvens af bytes, der kræves for at afkode det komprimerede JPEG2000 billede. Hvis filen ikke har andet end denne kodestrøm, kaldes den en rå kodestrømsfil. Normalt er en JPEG-kodestream anvendelsen af JPEG2000-komprimeringsalgoritmen på et billede, selvom det ikke er den eneste måde.

#### Flisedele ####

Et JPEG2000-kodet billede er en samling af dataenheder kaldet pakker. Disse pakker vedligeholdes i kodestrømmen inde i pakkegrupper kaldet tile-parts. Før indkodning af et billede, opdeler koderen billedet i et rektangulært gitter af blokke, kaldet fliser, hvor hver flise er kodet separat, uanset andre fliser.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 filformat" >}}

## J2K-komprimering ##
JPEG 2000 bruger wavelet-komprimeringsteknologi, hvilket gør det hurtigt baseret på det faktum, at der vises relativt få pixels i det viewport eller vindue, som seeren viser billedet. Dette kan understreges af, at der kun vises nogle få megabyte pixels på skærmen for meget store billeder (i gigabyte). Dette hjælper med hurtigt at hente og gengive kun den del af billeddataene, som er nødvendige for at udfylde skærmpixelerne. Dette kræver også højhastigheds dekompressionsteknologi for at fremskynde billedhentningsmekanismen til at skabe de billeder, der kræves i farten.

J2K udnytter hurtig dekompression og henter kun nødvendige oplysninger til pixeldata for at gengive en del af synlige billeder hurtigt til skærmene. J2K er primært designet til at se data og ikke redigere dem.

## J2K-identifikation ##
JPEG 2000-filer har signaturbytes 6A 50 20 20.

### Mimetyper ###
Registrerede Mime-typer til JPEG 2000-filer inkluderer:
  * billede/jp2
  * billede/jpx
  * billede/jpm
  * video/mj2

## Forbedringer i forhold til JPEG-standarden ##
Forbedringer i forhold til JPEG-standarden omfatter:
  * Overlegen kompressionsydelse
  * Repræsentation i flere opløsninger
  * Progressiv transmission med pixel og opløsningsnøjagtighed
  * Valg af tabsfri eller tabsgivende kompression
  * Fejlmodstandsdygtighed, fleksibelt filformat
  * Understøttelse af højt dynamisk område
  * Sidekanals rumlig information

## Referencer ##
  * [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

