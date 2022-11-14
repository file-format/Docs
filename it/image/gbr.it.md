{
  "date" : "2019-10-11",
  "keywords" :[ "file gbr", "formato file gbr", "cos'è un file gbr", "file", "esempio gbr", "estensione file gbr", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file GBR - Formato file Gerber per PCB",
  "description":"Scopri il formato di file GBR e le API che possono creare e aprire file GBR.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GBR?

Un file con estensione .gbr è un formato di file immagine Gerber per lo scambio di trasferimento di dati di progettazione di circuiti stampati (PCB). È stato sviluppato da Ucamco. I dati di progettazione PCB sono il componente principale richiesto dall'industria di fabbricazione per la manipolazione. Un file GRB contiene dati PCB come strati di rame, maschera di saldatura, legenda e dati di perforazione e percorso. Può essere utilizzato per trasferire dati come le caratteristiche di fabbricazione dei PCB, inclusi lo spessore o la finitura in un formato standardizzato. Tutti i sistemi di progettazione PCB producono file Gerber che possono essere gestiti dai sistemi di fabbricazione PCB. I file GBR sono ora diventati lo standard de facto per il trasferimento dei dati di progettazione di circuiti stampati (PCB). Ucamco ha fornito un [visualizzatore online gratuito](https://gerber-viewer.ucamco.com/) per aprire e visualizzare i formati di file GBR.

## Formato file GBR

GBR è un formato UTF-8 leggibile dall'uomo che consiste di soli 27 comandi. Grazie a questo breve elenco di comandi e alla sua compattezza, è facile eseguire il debug di GBR. Gerber al suo interno è un formato vettoriale aperto per immagini binarie 2D. Le meta-informazioni vengono trasferite con le immagini tramite Attributi. Un singolo file GRB specifica una singola immagine e non richiede l'interpretazione di file di accompagnamento o parametri esterni. Un'immagine necessita di un solo file. Utilizza caratteri ASCII a 7 bit per tutti i comandi ei nomi definiti nella specifica che sono stampabili. Questo copre completamente la generazione di immagini completa.

### Esempio di file GBR

Di seguito è riportato un esempio di file Gerber che crea un cerchio di 1,5 mm di diametro centrato sull'origine. C'è un comando per riga.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Riferimenti

* [Formato Gerber](https://www.ucamco.com/en/gerber)

