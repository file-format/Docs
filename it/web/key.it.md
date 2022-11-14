{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file KEY e le API che possono creare e aprire file KEY.",
  "title" :"Formato file KEY - File chiave privata della posta ottimizzata per la privacy",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Che cos'è un file KEY?

Un file KEY è la parte privata di un meccanismo di sicurezza che viene salvato su disco nel formato di file Privacy-Enhanced Mal (PEM). Viene utilizzato per decrittografare le informazioni scambiate tra un browser Web e il server Web che serve le richieste di navigazione. Un file KEY contiene stringhe codificate che sono inutili per l'occhio umano ma sono l'essenza della crittografia/decrittografia dello scambio di informazioni come parte del certificato SSL sui server web. I file KEY vengono generati automaticamente e installati sul lato client.

Puoi aprire file **KEY** con qualsiasi editor di testo come Microsoft Notepad (Windows), Apple TextEdit (Mac) o GitHub Atom (multipiattaforma). I file KEY sono simili ai formati di file [CRT](/it/web/crt/) e [CER](/it/web/cer/).

## Formato file KEY - Ulteriori informazioni

I file KEY vengono archiviati su disco come file di testo normale ma sono stringhe codificate che non sono leggibili dall'uomo. In pratica, gli utenti non hanno alcuna comprensione delle stringhe quando vengono aperte in un editor di testo. Il certificato della chiave privata è riservato e non deve essere condiviso con nessuno. Il processo completo per garantire lo scambio di informazioni su Internet prevede:

* **Chiave pubblica** - utilizzata per crittografare le informazioni dell'utente per lo scambio di dati tra il browser e i server web
* **Chiave privata** - utilizzata per decrittografare le informazioni così come vengono ricevute dal server web

I certificati SSL, noti anche come certificati X.509, sono univoci per ogni sito web. KEY file utilizzando la seguente sintassi:

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

### Esempio di file KEY

Di seguito è riportato un esempio di file chiave privata.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Riferimenti

* [Chiavi pubbliche, chiavi private e certificati](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

