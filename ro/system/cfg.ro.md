{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "extensie", "fișier", "format", "sistem", "configurare", "setări", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Format de fișier",
  "description":"Aflați despre formatul de fișier CFG și despre API-urile care pot crea și deschide fișiere CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier CFG? ##

Un fișier cu o extensie .cfg este un tip de fișier „settings”. Este un tip de fișier folosit în mod obișnuit și folosit pentru a stoca informații privind configurarea și setările pentru programele de calculator. Majoritatea tipurilor de fișiere CFG sunt stocate în format text și nu ar trebui deschise manual, ci ar trebui să fie deschise folosind un editor de text. Cu toate acestea, există diferite tipuri de fișiere CFG, care diferă în formatul în care sunt stocate informațiile. Caracteristicile pe care le oferă fișierele CFG variază de la aplicație la aplicație. Unele aplicații de calculator permit utilizatorilor să modifice sau să dezvolte sintaxa fișierelor de configurare prin utilizarea interferențelor grafice, în timp ce altele permit modificări doar folosind un editor de text. După modificarea acestor fișiere, utilizatorii pot instrui aplicația să citească din nou aceste fișiere și să aplice modificările sistemului.


## Format de fișier CFG ##

Fișierele CFG sunt acceptate de diverse sisteme de operare, cum ar fi sistemele de operare Unix și similare Unix, MS-DOS, macOS, Microsoft Windows și IBM OS/2. Formatul în care aceste fișiere sunt stocate și utilizate în fiecare dintre aceste sisteme de operare variază. Majoritatea sistemelor au folosit și stochează aceste fișiere într-un format de text simplu care poate fi citit și editabil de om, în timp ce altele stochează în el un format mai complex, în funcție de utilizarea fișierelor și de cerințele sistemului de operare.

În sistemele de operare Unix și Unix-like, cele mai multe fișiere CFG sunt folosite mai multe stiluri de formate diferite pentru fișierele CFG, cu toate acestea, cel mai comun format este un format de text simplu ușor de citit și aproape toate formatele permit efectuarea și editarea comentariilor. Cele mai comune extensii de fișiere pentru fișierele CFG din aceste sisteme de operare sunt CNF, CONF, CF și INI.

În sistemul de operare MS-DOS a existat inițial un singur format de fișier de configurare și anume textul simplu, totuși, MS-DOS 6 a adus cu sine introducerea unui format de fișier de configurare INI.

macOS folosește un fișier standard de configurare a stilului de listă de proprietăți.

În Microsoft Windows, fișierele de configurare în stil INI text simplu au fost o sursă importantă de stocare și editare a informațiilor, cu toate acestea, un nou sistem de baze de date a fost introdus în 1993, ceea ce a condus la o scădere a utilizării fișierelor de configurare în Microsoft Windows după 1993.


## Exemplu CFG ##

Un exemplu de fișier CFG poate fi văzut mai jos:

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
