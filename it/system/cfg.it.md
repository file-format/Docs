{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "estensione", "file", "formato", "sistema", "configurazione", "impostazioni", "programmi", "computer", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Formato file",
  "description":"Scopri il formato di file CFG e le API che possono creare e aprire file CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file CFG? ##

Un file con estensione .cfg è un tipo di file "impostazioni". È un tipo di file comunemente usato e utilizzato per memorizzare informazioni relative alla configurazione e alle impostazioni per i programmi per computer. La maggior parte dei tipi di file CFG sono archiviati in formato testo e non devono essere aperti manualmente, ma devono essere aperti utilizzando un editor di testo. Tuttavia, esistono diversi tipi di file CFG, che differiscono per il formato con cui vengono archiviate le informazioni. Le funzionalità offerte dai file CFG variano da applicazione a applicazione. Alcune applicazioni per computer consentono agli utenti di modificare o sviluppare la sintassi dei file di configurazione mediante l'uso di interferenze grafiche, mentre altre consentono solo modifiche utilizzando un editor di testo. Dopo aver modificato questi file, gli utenti possono istruire l'applicazione a leggere nuovamente questi file e ad applicare le modifiche al sistema.


## Formato file CFG ##

I file CFG sono supportati da vari sistemi operativi come Unix e sistemi operativi simili a Unix, MS-DOS, macOS, Microsoft Windows e IBM OS/2. Il formato in cui questi file vengono archiviati e utilizzati in ciascuno di questi sistemi operativi varia. La maggior parte dei sistemi utilizzava e archiviava questi file in un formato di testo semplice leggibile e modificabile, mentre altri archiviavano in un formato più complesso, a seconda dell'utilizzo dei file e dei requisiti del sistema operativo.

Nei sistemi operativi Unix e simili a Unix, la maggior parte dei file CFG vengono utilizzati diversi stili di formato per i file CFG, tuttavia, il formato più comune è un formato di testo normale facilmente leggibile e quasi tutti i formati consentono di creare e modificare commenti. Le estensioni di file più comuni per i file CFG in questi sistemi operativi sono CNF, CONF, CF e INI.

Nel sistema operativo MS-DOS inizialmente esisteva un solo formato di file di configurazione, vale a dire, testo normale, tuttavia, MS-DOS 6, ha portato con sé l'introduzione di un formato di file di configurazione INI.

macOS utilizza un file di configurazione dello stile del formato dell'elenco delle proprietà standard.

In Microsoft Windows, i file di configurazione in stile INI in testo normale erano un'importante fonte di archiviazione e modifica delle informazioni, tuttavia, nel 1993 è stato introdotto un nuovo sistema di database, che ha portato a una diminuzione dell'uso dei file di configurazione in Microsoft Windows dopo il 1993.


## Esempio CFG ##

Di seguito è possibile visualizzare un file CFG di esempio:

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
