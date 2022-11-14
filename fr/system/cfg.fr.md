{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "extension", "fichier", "format", "système", "configuration", "paramètres", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Format de fichier",
  "description":"En savoir plus sur le format de fichier CFG et les API qui peuvent créer et ouvrir des fichiers CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier CFG ? ##

Un fichier avec une extension .cfg est un type de fichier "paramètres". Il s'agit d'un type de fichier couramment utilisé et utilisé pour stocker des informations concernant la configuration et les paramètres des programmes informatiques. La plupart des types de fichiers CFG sont stockés au format texte et ne doivent pas être ouverts manuellement, mais plutôt à l'aide d'un éditeur de texte. Cependant, il existe différents types de fichiers CFG, qui diffèrent par le format avec lequel les informations sont stockées. Les fonctionnalités offertes par les fichiers CFG varient d'une application à l'autre. Certaines applications informatiques permettent aux utilisateurs de modifier, ou de faire évoluer la syntaxe de leurs fichiers de configuration par l'utilisation d'interférences graphiques, tandis que d'autres n'autorisent les modifications qu'à l'aide d'un éditeur de texte. Après avoir modifié ces fichiers, les utilisateurs peuvent demander à l'application de relire ces fichiers et d'appliquer les modifications au système.


## Format de fichier CFG ##

Les fichiers CFG sont pris en charge par divers systèmes d'exploitation tels que les systèmes d'exploitation Unix et de type Unix, MS-DOS, macOS, Microsoft Windows et IBM OS/2. Le format dans lequel ces fichiers sont stockés et utilisés dans chacun de ces systèmes d'exploitation varie. La plupart des systèmes utilisent et stockent ces fichiers dans un format de texte brut lisible et modifiable par l'homme, tandis que d'autres y stockent un format plus complexe, en fonction de l'utilisation des fichiers et des exigences du système d'exploitation.

Dans les systèmes d'exploitation Unix et de type Unix, la plupart des fichiers CFG utilisent plusieurs styles de format différents pour les fichiers CFG, cependant, le format le plus courant est un format de texte brut facilement lisible, et presque tous les formats permettent de faire et de modifier des commentaires. Les extensions de fichier les plus courantes pour les fichiers CFG dans ces systèmes d'exploitation sont CNF, CONF, CF et INI.

Dans le système d'exploitation MS-DOS, il n'y avait initialement qu'un seul format de fichier de configuration, à savoir le texte brut, cependant, MS-DOS 6 a entraîné l'introduction d'un format de fichier de configuration INI.

macOS utilise un fichier de configuration de style de format de liste de propriétés standard.

Dans Microsoft Windows, les fichiers de configuration de style INI en texte brut étaient une source importante de stockage et d'édition d'informations, cependant, un nouveau système de base de données a été introduit en 1993, entraînant une diminution de l'utilisation des fichiers de configuration dans Microsoft Windows après 1993.


## Exemple CFG ##

Un exemple de fichier CFG peut être vu ci-dessous :

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
