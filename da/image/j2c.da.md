{
  "date": "2019-10-11",
  "keywords": [
"j2c fil",
"j2c filformat",
"hvad er en j2c fil",
"fil",
"j2c eksempel",
"j2c filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2C",
  "description": "Lær om J2C-filformat og API'er, der kan oprette og åbne J2C-filer.",
  "linktitle": "J2C",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-dac"
}
},
  "lastmod": "2021-02-14"
}

## Hvad er J2C fil?

En fil med filtypenavnet .j2c er en variant af JPEG-filformatet og komprimeres med wavelet-komprimeringen. Det har næsten identisk system af markører og segmenter til JPEG 2000 filformat. J2C-filformatet er som defineret i del 1 af JPEG 2000-standen, der understøtter både tabs- og tabsfri komprimering. JPEG 2000-kodestrømmen er designet til at blive indlejret i [JP2](/image/jp2/) eller et andet filformat, selvom det kan forekomme i en fil for sig selv. En J2C-fil kan åbnes ved hjælp af Adobe Photoshop 2020, Adobe Illustrator 2020 og Corel Paintshop Pro.

## J2C filformat

J2C-filformatet er det samme som JPEG 2000, som ofte gemmes som .jp2 og .jpc. Dette får J2C-filer til at følge den samme tilgang til kodning af metadata i XML-format, hvor Standard 12234-1 bruges som reference mellem Exif-tags og XML-komponenterne. Den er yderligere forbedret af JPEG 2000 del-2-udvidelsen, der kombinerer animationsmekanismen og kodestrømskonfigurationerne i ét enkelt billede. Sådanne filer i udvidet filformat gemmes som [.jpx](/image/jpx/).

### Layout af en JPEG2000-fil

JPEG2000 understøtter en række applikationer baseret på overensstemmelsen for udvidelige filformater. Selvom den enkleste type kan indeholde et enkelt billede, kan mere komplekse typer omfatte en række billeder, stablet oven på hinanden eller er tidsbaserede sekvenserede.

#### JP2 Box
Det er byggestenen på øverste niveau i JP2-filformatet og indeholder en type- og længdefelter i overskriften og en datasektion. Den mest bemærkelsesværdige type boks er den sammenhængende kodestrømsboks. Denne boks gemmer i sin datasektion JPEG2000-kodestrømmen.

#### JPEG2000 CodeStream

JPEG2000 CodeStream er en sekvens af bytes, der kræves for at afkode det komprimerede JPEG2000 billede. Hvis filen ikke har andet end denne kodestrøm, kaldes den en rå kodestrømsfil. Normalt er en JPEG-kodestream anvendelsen af JPEG2000-komprimeringsalgoritmen på et billede, selvom det ikke er den eneste måde.

#### Flisedele ####

Et JPEG2000-kodet billede er en samling af dataenheder kaldet pakker. Disse pakker vedligeholdes i kodestrømmen inde i pakkegrupper kaldet tile-parts. Før indkodning af et billede, opdeler koderen billedet i et rektangulært gitter af blokke, kaldet fliser, hvor hver flise er kodet separat, uanset andre fliser.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 filformat" >}}

## J2C kompression
JPEG 2000 bruger wavelet-komprimeringsteknologi, hvilket gør det hurtigt baseret på det faktum, at der vises relativt få pixels i det viewport eller vindue, som seeren viser billedet. Dette kan understreges af, at der kun vises nogle få megabyte pixels på skærmen for meget store billeder (i gigabyte). Dette hjælper med hurtigt at hente og gengive kun den del af billeddataene, som er nødvendige for at udfylde skærmpixelerne. Dette kræver også højhastigheds dekompressionsteknologi for at fremskynde billedhentningsmekanismen til at skabe de billeder, der kræves i farten.

J2C drager fordel af hurtig dekompression og henter kun nødvendige oplysninger til pixeldata for at gengive en del af synlige billeder hurtigt til skærmene. J2C er primært designet til at se data og ikke redigere dem.

## J2C identifikation
JPEG 2000-filer har signaturbytes `FF 4F FF 51`.

### Mimetyper
Registrerede Mime-typer til JPEG 2000-filer inkluderer:
  * billede/j2c
  * billede/jpx
  * billede/jpm
  * video/mj2

## Forbedringer i forhold til JPEG-standarden
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

