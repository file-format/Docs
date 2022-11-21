{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "extensão", "arquivo", "formato", "sistema", "configuração", "configurações", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Formato de arquivo",
  "description":"Saiba mais sobre o formato de arquivo CFG e APIs que podem criar e abrir arquivos CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo CFG? ##

Um arquivo com extensão .cfg é um tipo de arquivo de "configurações". É um tipo de arquivo popularmente usado e usado para armazenar informações sobre configuração e configurações de programas de computador. A maioria dos tipos de arquivos CFG são armazenados em formato de texto e não devem ser abertos manualmente, em vez disso, eles devem ser abertos usando um editor de texto. No entanto, existem diferentes tipos de arquivos CFG, que diferem no formato com o qual as informações são armazenadas. Os recursos que os arquivos CFG oferecem variam de aplicativo para aplicativo. Alguns aplicativos de computador permitem que os usuários modifiquem ou desenvolvam a sintaxe de seus arquivos de configuração pelo uso de interferências gráficas, enquanto outros permitem apenas modificações usando um editor de texto. Após modificar esses arquivos, os usuários podem instruir o aplicativo a ler esses arquivos novamente e aplicar as modificações no sistema.


## Formato de arquivo CFG ##

Os arquivos CFG são suportados por vários sistemas operacionais, como sistemas operacionais Unix e semelhantes a Unix, MS-DOS, macOS, Microsoft Windows e IBM OS/2. O formato em que esses arquivos são armazenados e usados em cada um desses sistemas operacionais varia. A maioria dos sistemas usa e armazena esses arquivos em um formato de texto simples editável e legível por humanos, enquanto outros armazenam nele um formato mais complexo, dependendo do uso dos arquivos e dos requisitos do sistema operacional.

Nos sistemas operacionais Unix e do tipo Unix, a maioria dos arquivos CFG são usados vários estilos de formato diferentes para arquivos CFG, no entanto, o formato mais comum é um formato de texto simples de fácil leitura e quase todos os formatos permitem que comentários sejam feitos e editados. As extensões de arquivo mais comuns para arquivos CFG nesses sistemas operacionais são CNF, CONF, CF e INI.

No sistema operacional MS-DOS havia inicialmente apenas um formato de arquivo de configuração, ou seja, texto simples, no entanto, o MS-DOS 6, trouxe consigo a introdução de um formato de arquivo de configuração INI.

O macOS usa um arquivo de configuração de estilo de formato de lista de propriedades padrão.

No Microsoft Windows, os arquivos de configuração estilo INI de texto simples eram uma importante fonte de armazenamento e edição de informações, no entanto, um novo sistema de banco de dados foi introduzido em 1993, levando a uma diminuição no uso de arquivos de configuração no Microsoft Windows após 1993.


## Exemplo CFG ##

Um exemplo de arquivo CFG pode ser visto abaixo:

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
