{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "rozšíření", "soubor", "formát", "systém", "konfigurace", "nastavení", "programy", "počítač", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Formát souboru",
  "description":"Další informace o formátu souboru CFG a rozhraních API, která mohou vytvářet a otevírat soubory CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor CFG? ##

Soubor s příponou .cfg je typem souboru „settings“. Je to populárně používaný typ souboru a používá se k ukládání informací týkajících se konfigurace a nastavení počítačových programů. Většina typů souborů CFG je uložena v textovém formátu a neměly by být otevírány ručně, místo toho by měly být otevřeny pomocí textového editoru. Existují však různé typy souborů CFG, které se liší formátem, ve kterém jsou informace uloženy. Funkce, které soubory CFG nabízejí, se liší od aplikace k aplikaci. Některé počítačové aplikace umožňují uživatelům upravovat nebo vyvíjet syntaxi konfiguračních souborů pomocí grafických interferencí, jiné umožňují úpravy pouze pomocí textového editoru. Po úpravě těchto souborů mohou uživatelé přikázat aplikaci, aby tyto soubory znovu načetla a použila úpravy na systém.


## Formát souboru CFG ##

Soubory CFG jsou podporovány různými operačními systémy, jako jsou Unix a operační systémy podobné Unixu, MS-DOS, macOS, Microsoft Windows a IBM OS/2. Formát, ve kterém jsou tyto soubory uloženy a používány v každém z těchto operačních systémů, se liší. Většina systémů používá a ukládá tyto soubory ve formátu prostého textu čitelného a upravitelného pro člověka, zatímco jiné v něm ukládají složitější formát v závislosti na použití souborů a požadavcích operačního systému.

V Unixu a Unixu podobných operačních systémech se u většiny souborů CFG používá několik různých formátů souborů CFG, nejběžnějším formátem je však snadno čitelný formát prostého textu a téměř všechny formáty umožňují vytvářet a upravovat komentáře. Nejběžnější přípony souborů pro soubory CFG v těchto operačních systémech jsou CNF, CONF, CF a INI.

V operačním systému MS-DOS byl zpočátku pouze jeden formát konfiguračního souboru, a to prostý text, avšak MS-DOS 6 s sebou přinesl zavedení formátu konfiguračního souboru INI.

macOS používá standardní konfigurační soubor formátu seznamu vlastností.

V Microsoft Windows byly konfigurační soubory ve stylu Plain text INI důležitým zdrojem pro ukládání a úpravy informací, nicméně v roce 1993 byl představen nový databázový systém, který po roce 1993 vedl k poklesu používání konfiguračních souborů v Microsoft Windows.


## Příklad CFG ##

Ukázkový soubor CFG si můžete prohlédnout níže:

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
