{
  "date": "2021-06-29",
  "keywords": [
"CFG",
"udvidelse",
"fil",
"format",
"system",
"konfiguration",
"indstillinger",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFG - Filformat",
  "description": "Lær om CFG filformat og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cf-dag"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er CFG fil? ##

En fil med filtypen .cfg er en type indstillingsfil. Det er en populært brugt filtype og bruges til at gemme information om konfiguration og indstillinger for computerprogrammer. De fleste typer CFG-filer er gemt i tekstformat og bør ikke åbnes manuelt, i stedet skal de åbnes ved hjælp af en teksteditor. Der er dog forskellige typer CFG-filer, der adskiller sig i det format, som oplysningerne er gemt med. De funktioner, som CFG-filer tilbyder, varierer fra applikation til applikation. Nogle computerapplikationer gør det muligt for brugerne at ændre eller udvikle deres konfigurationsfilers syntaks ved brug af grafiske interferenser, mens andre kun tillader ændringer ved hjælp af en teksteditor. Efter at have ændret disse filer, kan brugerne instruere applikationen til at læse disse filer igen og anvende ændringerne på systemet.


## CFG-filformat ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. Formatet, som disse filer gemmes og bruges i hvert af disse operativsystemer, varierer. De fleste systemer brugte og gemmer disse filer i et menneskeligt læsbart og redigerbart almindeligt tekstformat, mens andre gemmer et mere komplekst format i det, afhængigt af filbrugen og operativsystemets krav.

I Unix- og Unix-lignende operativsystemer bruges de fleste CFG-filer flere forskellige formatstile til CFG-filer, dog er det mest almindelige format et letlæsbart almindeligt tekstformat, og næsten alle formaterne tillader, at kommentarer kan laves og redigeres. De mest almindelige filtypenavne til CFG filer i disse operativsystemer er CNF, CONF, CF og INI.

I MS-DOS-operativsystemet var der oprindeligt kun ét konfigurationsfilformat, nemlig almindelig tekst, men MS-DOS 6 medførte introduktionen af et INI-konfigurationsfilformat.

macOS bruger en standard konfigurationsfil for egenskabslisteformat.

I Microsoft Windows var konfigurationsfiler i almindelig tekst INI-stil en vigtig kilde til lagring og redigering af information, men et nyt databasesystem blev introduceret i 1993, hvilket førte til et fald i brugen af konfigurationsfiler i Microsoft Windows efter 1993.


## CFG-eksempel ##

Et eksempel på CFG-fil kan ses nedenfor:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

## Andre CFG-filer

Her er andre filtyper, der bruger filtypen **.cfg**.

**Indstillinger**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spil**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System og diverse**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

