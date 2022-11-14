{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File PEM - Formato file certificato di posta ottimizzato per la privacy",
  "description":"Scopri il formato di file PEM e le API che possono creare e aprire file PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Che cos'è un file PEM?

Un file PEM è un file di certificato di sicurezza utilizzato per stabilire un canale di comunicazione sicuro tra un server Web e un browser. È codificato in Base64 e può contenere una chiave privata, un certificato del server e/o una combinazione di altri certificati. I file PEM sono simili ai file di certificato .der in termini di utilizzo, ma vengono archiviati come testo con codifica Base64 anziché come dati binari. Altri formati di file di certificato simili includono i file [.cer](/it/web/cer/) e [.crt](/it/web/crt/).

Le applicazioni che possono **aprire file PEM** includono editor di testo come Microsoft Notepad e Apple TextEdit.

## Formato file PEM

PEM è un formato di file contenitore che definisce la struttura e il tipo di codifica del file utilizzato per archiviare i dati. I file PEM vengono archiviati su disco come formato di file con codifica Base64 che non è leggibile dall'uomo. Lo standard definisce che un file PEM inizia con:

```
-----BEGIN <type>-----
```
e termina con:
```
-----END <type>-----
```

Tutti gli altri contenuti all'interno di questi sono codificati in base64 (lettere maiuscole e minuscole, cifre, + e /). Un singolo file PEM può comprendere più blocchi che possono essere utilizzati da altri programmi. Se un file PEM contiene più certificati, ogni certificato è separato da singoli blocchi come segue:

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### Esempio di file PEM

Un file PEM con blocco CERTIFICATE di solito ha il seguente aspetto:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Un file PEM con RSA inizia come segue.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Riferimenti ##

* [Crittografia a chiave pubblica](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Come creare il file P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

