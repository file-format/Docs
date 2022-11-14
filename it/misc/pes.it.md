{
  "date" : "2021-07-29",
  "keywords" :[ "file pes", "formato file pes", "cos'è un file pes", "file", "esempio pes", "estensione file pes", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file PES - Formato ricamo Brother PE",
  "description":"Scopri il formato di file PES e le API che possono creare e aprire file PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Che cos'è un file di ricamo PES?

Il file di ricamo PES è un file di disegno che contiene le istruzioni per le macchine da ricamo/cucire. È stato sviluppato da Brother Industries per le loro macchine da ricamo, ma in seguito è stato formalizzato come formato di file generale. I file PES vengono utilizzati dalle macchine da cucire per leggere le istruzioni per la cucitura di motivi su tessuto. Questi file servono a due scopi; in primo luogo fornendo informazioni sul disegno per l'applicazione PE-Design sviluppata da Brother Industries e in secondo luogo, fornendo il nome del disegno, i colori e i codici della macchina da ricamo come "stop", "salta" e "rifila".

## Formato file PES - Ulteriori informazioni

Un file PES viene salvato su disco in formato binario. Contiene più sezioni che contengono informazioni di cucitura memorizzate utilizzando il metodo predefinito. Il formato del file PES è il seguente.

* Dati versione: fornisce informazioni sulla versione e può essere qualsiasi valore `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* Valore di ricerca PEC - Un intero little-endian di 4 byte che segue immediatamente i dati della versione e rappresenta il valore di ricerca per la sezione PEC che contiene i dettagli di progettazione Informazioni
* Sezione PSE - Contiene informazioni di design rilevanti per Brother PE-Design e potrebbero essere altre applicazioni di cucito
* Sezione PCE - Può essere ovunque nel file PSE ma referenziata dal valore di ricerca PEC.

## Tipo di macchine da cucire che utilizzano file PES

I file PES vengono creati principalmente dal software PE-Design utilizzato con le macchine da cucire Brother. Alcune altre macchine che possono supportare i file PES includono le macchine da ricamo per la casa Babylock e Bernina.

## Come convertire i file PSE?

L'applicazione software PE-Design può [convertire il file PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+file) in altri formati come .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd o .xxx. Può essere fatto utilizzando l'applicazione PE-Design aprendo il file e selezionando il Formato di conversione.

## Riferimenti

* [PE Design - Manuale di istruzioni](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

