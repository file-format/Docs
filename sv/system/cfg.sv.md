{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "tillägg", "fil", "format", "system", "konfiguration", "inställningar", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Filformat",
  "description":"Läs mer om CFG-filformat och API:er som kan skapa och öppna CFG-filer.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är CFG fil? ##

En fil med filtillägget .cfg är en typ av "inställningar"-fil. Det är en populärt använd filtyp och används för att lagra information om konfiguration och inställningar för datorprogram. De flesta typer av CFG-filer lagras i textformat och bör inte öppnas manuellt, istället bör de öppnas med en textredigerare. Det finns dock olika typer av CFG-filer, som skiljer sig åt i formatet som informationen lagras med. Funktionerna som CFG-filer erbjuder varierar från applikation till applikation. Vissa datorapplikationer gör det möjligt för användarna att modifiera eller utveckla sina konfigurationsfilers syntax genom att använda grafiska störningar, medan andra endast tillåter ändringar med hjälp av en textredigerare. Efter att ha modifierat dessa filer kan användarna instruera applikationen att läsa dessa filer igen och tillämpa ändringarna på systemet.


## CFG-filformat ##

CFG-filer stöds av olika operativsystem som Unix och Unix-liknande operativsystem, MS-DOS, macOS, Microsoft Windows och IBM OS/2. Formatet som dessa filer lagras och används i vart och ett av dessa operativsystem varierar. De flesta system använder och lagrar dessa filer i ett läsbart och redigerbart oformaterat textformat, medan andra lagrar ett mer komplext format i det, beroende på filanvändningen och operativsystemets krav.

I Unix och Unix-liknande operativsystem används de flesta CFG-filer flera olika formatstilar för CFG-filer, men det vanligaste formatet är ett lättläst oformaterad text-format, och nästan alla format tillåter att kommentarer görs och redigeras. De vanligaste filtilläggen för CFG-filer i dessa operativsystem är CNF, CONF, CF och INI.

I MS-DOS operativsystem fanns det från början bara ett konfigurationsfilformat, nämligen ren text, men MS-DOS 6 förde med sig introduktionen av ett INI-konfigurationsfilformat.

macOS använder en stilkonfigurationsfil för standardegenskapslistformat.

I Microsoft Windows var konfigurationsfiler i vanlig text INI-stil en viktig källa för att lagra och redigera information, men ett nytt databassystem introducerades 1993, vilket ledde till en minskning av användningen av konfigurationsfiler i Microsoft Windows efter 1993.


## CFG-exempel ##

Ett exempel på CFG-fil kan ses nedan:

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
