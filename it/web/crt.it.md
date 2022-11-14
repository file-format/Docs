{
  "date" : "2019-10-11",
  "keywords" :[ "crt","file crt", "formato file crt", "tipo di file crt", "file", "tipo", "che cos'è un file crt"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Formato file certificato di sicurezza",
  "description":"Scopri il formato di file CRT e le API che possono creare e aprire file CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file CRT?

Un file con estensione .crt è un file di certificato di sicurezza utilizzato da siti Web protetti per stabilire connessioni sicure dal server Web a un browser. I siti Web sicuri consentono di proteggere i trasferimenti di dati, gli accessi, le transazioni con carta di pagamento e di fornire una navigazione protetta al sito. Se apri un sito Web protetto, vedrai l'icona di un "lucchetto" nella barra degli indirizzi. Se si fa clic su di esso, è possibile visualizzare i dettagli del certificato installato. Società internazionali come Verisign e Thawte distribuiscono questi certificati SSL.

## Formato file CRT

I file CRT sono in formato ASCII e possono essere aperti in qualsiasi editor di testo per visualizzare il contenuto del file del certificato. Segue lo standard di certificazione X.509 che definisce la struttura del certificato. Definisce i campi di dati che devono essere inclusi nel certificato SSL. CRT appartiene al formato PEM dei certificati che sono file con codifica ASCII Base64.

### Struttura del file PEM

Un file PEM può avere più certificati. In tal caso, ogni certificato nel file PEM segue la struttura seguente.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### Esempio di formato file CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Riferimenti ##

* [Chiavi pubbliche, chiavi private e certificati](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

