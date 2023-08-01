{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - File di riferimento macro di Microsoft Office",
  "description":"Ulteriori informazioni sul file MSO e sulle API che possono creare e aprire file MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Che cos'è un file MSO?

Un file MSO è un formato di file contenitore di dati che viene creato quando un messaggio HTML viene inviato utilizzando Microsoft Outlook. Ciò accade principalmente con le applicazioni di Microsoft Office 2000. Nella maggior parte dei casi, il messaggio di posta elettronica è allegato con il nome del file **Oledata.mso**. Il destinatario dell'e-mail, quando apre tale e-mail, può visualizzare il file correttamente anche se non ha installato lo stesso software. I file MSO fanno riferimento a [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Formato file Microsoft MSO

I file MSO vengono salvati in Microsoft Compound Document File Format (MCDF), noto anche come formato di file binario di implementazione di file compositi di archiviazione strutturata OLE (Object Linking and Embedding) o COM (Component Object Model).

### Struttura del formato file MSO

La struttura del formato file interno del formato file MSO è ben definita in [Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) sezione della documentazione MCDF. La File Allocation Table (FAT) gestisce l'allocazione settoriale e le catene settoriali. Contiene una matrice di numeri di settore a 32 bit. Ogni indice nell'array rappresenta un numero di settore mentre il suo valore rappresenta il settore successivo nella catena o un valore speciale.

## Riferimenti

* [Archiviazione strutturata COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

