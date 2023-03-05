{
  "date" : "2021-08-10",
  "keywords" :[ "file .ovf", "formato file", "cos'è un file .ovf", "file", "estensione file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri cos'è un formato di file .ovf e le API che possono creare e aprire file OVF.",
  "title" :"Formato file OVF - Apri file di virtualizzazione",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## Che cos'è un file OVF?

Un file OVF è un file di testo che contiene informazioni sulla confezione e sulla distribuzione di un software eseguito su una macchina virtuale. È formattato secondo le [Specifiche dello standard di virtualizzazione aperta](https://www.dmtf.org/standards/ovf) che descrive tutti i requisiti (come sicurezza, portabilità, efficienza ed estensibilità) per l'esecuzione di applicazioni su macchine virtuali. L'Organizzazione internazionale per la standardizzazione (ISO) ha adottato OVF come standard ISO 17203.

## Breve storia del formato di file OVF

Il formato file OVF è stato introdotto da DMTF (Distributed Management Task Force) che crea standard di gestibilità aperti. È indipendente da qualsiasi hypervisor particolare o architettura del set di istruzioni. Il pacchetto OVF contiene uno o più sistemi virtuali, ognuno dei quali può essere distribuito su una macchina virtuale.

## Formato file OVF - Ulteriori informazioni

Un pacchetto OVF è costituito da più file inseriti in un'unica directory. Tra questi, contiene esattamente un file descrittore OVF (con estensione .ovf) che è memorizzato nel formato di file [XML](/it/web/xml/). Descrive le informazioni sulla macchina virtuale in pacchetto e le informazioni sui metadati sul pacchetto OVF come:

* nome
* requisiti hardware
* riferimenti agli altri file nel pacchetto OVF e
* descrizioni leggibili dall'uomo

Altri file che possono essere trovati in un pacchetto OVF includono una o più immagini disco e facoltativamente file di certificato e altri file ausiliari.

## Riferimenti

* [Formato di virtualizzazione aperto - DMTF](https://www.dmtf.org/standards/ovf)
* [Specifiche del formato file OVF](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

