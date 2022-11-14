{
  "date" : "2021-03-11",
  "keywords" :[ "APNX", "Indice numero pagina Amazon", "estensione", "file", "formato", "eBook", "Amazon Kindle" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file Amazon APNX e le API che possono creare e aprire file APNX.",
  "title" :"APNX - Indice del numero di pagina Amazon",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## Che cos'è un file APNX? ##

Il file Amazon Page Number Index che utilizza l'estensione .apnx è un tipo di file eBook; utilizzato da Amazon Kindle. Questi file sono in realtà noti come file di impaginazione utilizzati dai dispositivi Kindle. Quindi i file APNX vengono in genere creati per contrassegnare le pagine degli eBook Kindle. La funzione di impaginazione è stata avviata sui dispositivi Amazon Kindle dal suo firmware 3.1. Cerca nel file APNX gli indici di pagina e quindi lo mappa con i numeri di pagina nel libro di stampa originale. Questi file vengono salvati nei dispositivi Kindle insieme ai file Amazon eBooks. Non è possibile aprire o modificare i file APNX.

## Specifiche del formato file APNX ##

### Disposizione

|byte| contenuto| commenti|
---|---|---|
|4 |00010001 | Identificatore di formato. Valore di 65537 little-endian.|
|4 |inizio del prossimo | L'offset dopo la posizione finale della prima intestazione. Avvia una nuova sequenza di header info|
|4 |lunghezza| Lunghezza della prima intestazione|
|N |prima intestazione | Stringa contenente l'intestazione del contenuto. Inizia la sequenza successiva|
|2 |sconosciuto | Sempre 1|
|2 |lunghezza | Lunghezza della seconda intestazione|
|2 |conteggio pagine | Numero totale di byte dopo la seconda intestazione che rappresentano le pagine. Questo totale include i byte ignorati da pageMap.|
|2 |sconosciuto | Sempre 32|
|N |seconda intestazione | Stringa contenente l'intestazione di mappatura della pagina|
|4*N |imbottitura | Il primo numero fornito nell'intestazione della mappatura della pagina indica il numero di 0 byte.|
|4*N |elenco delle pagine ||

### Intestazione del contenuto

L'intestazione del contenuto è costituita da una stringa racchiusa tra {} contenente coppie chiave e valore:

|contenuto| commenti|
---|---|
|contentGuid| guida.|
|asino | Identificatore Amazon per la versione Kindle del libro.|
|cdeType | MOBI cdeType. Dovrebbe essere sempre EBOK per gli ebook.|
|ID revisione file | Revisione di questo file.|

#### Esempio
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Intestazione di mappatura della pagina
L'intestazione di mappatura della pagina è costituita da una stringa racchiusa tra {} contenente coppie chiave e valore.

|contenuto | commenti|
---|---|
|asino | L'ISBN 10 per il libro cartaceo a cui corrispondono le pagine|
|Mappa pagina| Tupla a tre valori. Si presenta come: "(N,N,N)\
1) Numero di byte dopo l'intestazione che avvia la sequenza di numerazione delle pagine\
2) sconosciuto\
3) sconosciuto\|
#### Esempio
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Elenco pagine

L'elenco delle pagine è una sequenza di offset nell'HTML grezzo. A testa
value è l'inizio di una nuova pagina. Ogni voce è un big endian di 4 byte
int.



## Riferimenti

* [Formato file Amazon APNX](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - di MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)

