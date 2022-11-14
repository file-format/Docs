{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "estensione", "file", "formato", "web", "certificato", "lingua" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Formato file certificato",
  "description":"Scopri il formato di file CER e le API che possono creare e aprire file CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Che cos'è un file CER? ##

Un file con estensione .cer è responsabile della memorizzazione di alcune informazioni sul certificato del proprietario e sulla chiave pubblica specifica. Questo formato di file non può memorizzare le chiavi private e ha la capacità di memorizzare un solo certificato che è x509. Le autorità di certificazione specificamente protette sono quelle che appartengono a HTTPS, un protocollo affidabile e protetto per la navigazione
Il CER è un certificato del tuo server. Di solito viene ricevuto dall'autorità di certificazione per il dominio. CER è per lo più considerato uguale a [CRT](/it/web/crt/), sebbene entrambi abbiano lo stesso formato di certificato SSL ma siano estensioni di nomi di file diverse.
Questi possono essere utilizzati sui sistemi operativi semplicemente aprendo un browser e verificando la sicurezza del browser o del sito web in uso.

## Breve storia ##

Nel 1995 Thawte è diventata la prima autorità di certificazione per la risoluzione del problema dei certificati SSL (Secure Socket Link) pubblici al di fuori degli Stati Uniti. Successivamente, c'è una serie di tali autorità che è stata fondata dal 1995 al 2020.

## Formato file CER ##

Questi file possono essere semplicemente
* Il PKC S#7 comprende la codifica ASCII Base64
* Le sue estensioni di file sono p7b o p7cZ
* Per il contenuto binario, il certificato sarebbe DER o pkcs12/pfx.
Esistono molti tipi di file di certificato con alcune specifiche univoche:
* .pem, Quando un'organizzazione usThawteificate concatena questo formato è ben noto per creare certificati
* .arm, quando è richiesto il metodo per estrarre una certificazione assistita autofirmata, il formato specificato per questo scopo è .arm. È rappresentato nella codifica ASCII base-64.
* .der, Consiste di dati binari. Ciò significa che può essere utilizzato solo per un singolo certificato
* .pfx (PKC512), Consiste in una chiave privata corrispondente a un certificato emesso da CA o un certificato autofirmato. Questo formato è noto per la conversione di un'implementazione SSL nell'altra.


