{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - File certificato PKCS 7",
  "description":"Scopri il formato di file P7C e le API che possono creare e aprire file P7C.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file P7B?

Un file P7B è un file di certificato di sicurezza che contiene un certificato digitale sicuro per l'autenticazione di una persona o di un dispositivo. Simile a un file di certificato [.cer](/it/web/cer/), è possibile installare un file P7B utilizzando l'opzione "Installa certificato" utilizzando l'opzione del tasto destro del mouse sul file. P7B utilizza un'opzione di formattazione diversa rispetto al formato file CER. Contiene uno o più file di certificati digitali X.509 che utilizzano la codifica base64 (ASCII). I file P7B vengono ricevuti come file [ZIP](/it/compression/zip/) o ricevuti dall'autorità di certificazione.

## Formato file P7B

I file P7B sono archiviati come semplici file ASCII che possono essere aperti in qualsiasi editor di testo. Contiene la chiave pubblica che è una stringa codificata che non ha significato dal punto di vista della leggibilità.

### Esempio di formato file P7B

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Riferimenti ##

* [Crittografia a chiave pubblica](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Come creare il file P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

