{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "extensie", "bestand", "formaat", "systeem", "configuratie", "instellingen", "programma's", "computer", "toepassing"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Bestandsformaat",
  "description":"Meer informatie over CFG-bestandsindeling en API's die CFG-bestanden kunnen maken en openen.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Wat is een CFG-bestand? ##

Een bestand met de extensie .cfg is een soort "instellingen"-bestand. Het is een veelgebruikt bestandstype en wordt gebruikt om informatie op te slaan met betrekking tot configuratie en instellingen voor computerprogramma's. De meeste typen CFG-bestanden worden opgeslagen in tekstformaat en mogen niet handmatig worden geopend, maar moeten worden geopend met een teksteditor. Er zijn echter verschillende soorten CFG-bestanden, die verschillen in het formaat waarmee de informatie wordt opgeslagen. De functies die CFG-bestanden bieden, variëren van toepassing tot toepassing. Sommige computertoepassingen stellen de gebruikers in staat om de syntaxis van hun configuratiebestanden te wijzigen of te ontwikkelen door het gebruik van grafische interferenties, terwijl andere alleen wijzigingen toestaan met behulp van een teksteditor. Na het wijzigen van deze bestanden kunnen de gebruikers de toepassing opdracht geven om deze bestanden opnieuw te lezen en de wijzigingen op het systeem toe te passen.


## CFG-bestandsindeling ##

CFG-bestanden worden ondersteund door verschillende besturingssystemen, zoals Unix en Unix-achtige besturingssystemen, MS-DOS, macOS, Microsoft Windows en IBM OS/2. De indeling waarin deze bestanden in elk van deze besturingssystemen worden opgeslagen en gebruikt, varieert. De meeste systemen gebruiken en slaan deze bestanden op in een voor mensen leesbare en bewerkbare platte tekstindeling, terwijl andere er een complexere indeling in opslaan, afhankelijk van het bestandsgebruik en de vereisten van het besturingssysteem.

In Unix en Unix-achtige besturingssystemen worden de meeste CFG-bestanden gebruikt in verschillende indelingsstijlen voor CFG-bestanden, maar de meest gebruikelijke indeling is een gemakkelijk leesbare platte tekstindeling en bijna alle indelingen maken het mogelijk om opmerkingen te maken en te bewerken. De meest voorkomende bestandsextensies voor CFG-bestanden in deze besturingssystemen zijn CNF, CONF, CF en INI.

In het MS-DOS-besturingssysteem was er aanvankelijk slechts één configuratiebestandsformaat, namelijk platte tekst, maar MS-DOS 6 bracht de introductie van een INI-configuratiebestandsformaat met zich mee.

macOS gebruikt een standaard configuratiebestand voor de indeling van de eigenschappenlijst.

In Microsoft Windows waren configuratiebestanden in platte tekst INI-stijl een belangrijke bron voor het opslaan en bewerken van informatie, maar in 1993 werd een nieuw databasesysteem geïntroduceerd, wat leidde tot een afname van het gebruik van configuratiebestanden in Microsoft Windows na 1993.


## CFG-voorbeeld ##

Een voorbeeld van een CFG-bestand is hieronder te zien:

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
