{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM File - Privacy Enhanced Mail Certificate Format",
  "description":"Další informace o formátu souboru PEM a rozhraních API, která mohou vytvářet a otevírat soubory PEM.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## Co je soubor PEM?

Soubor PEM je soubor bezpečnostního certifikátu, který se používá k vytvoření zabezpečeného komunikačního kanálu mezi webovým serverem a prohlížečem. Je kódován Base64 a může obsahovat soukromý klíč, certifikát serveru a/nebo kombinaci jiných certifikátů. Soubory PEM jsou z hlediska použití podobné souborům certifikátů .der, ale jsou uloženy jako text kódovaný Base64, nikoli binární data. Mezi další podobné formáty souborů certifikátů patří soubory [.cer](/cs/web/cer/) a [.crt](/cs/web/crt/).

Aplikace, které mohou **otevřít soubory PEM**, zahrnují textové editory, jako je Microsoft Notepad a Apple TextEdit.

## Formát souboru PEM

PEM je formát kontejnerového souboru, který definuje strukturu a typ kódování souboru použitého k uložení dat. Soubory PEM se ukládají na disk ve formátu souboru zakódovaného v Base64, který není čitelný pro člověka. Standard definuje, že soubor PEM začíná:

```
-----BEGIN <type>-----
```
a končí:
```
-----END <type>-----
```

Veškerý ostatní obsah v nich je kódován base64 (velká a malá písmena, číslice, + a /). Jeden soubor PEM se může skládat z více bloků, které mohou být použity jinými programy. Pokud soubor PEM obsahuje více certifikátů, každý certifikát je oddělen jednotlivými bloky následovně:

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

### Příklad souboru PEM

Soubor PEM s blokem CERTIFICATE obvykle vypadá takto:

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

Soubor PEM s RSA začíná následovně.

```
-----BEGIN RSA PRIVATE KEY-----
```

## Reference ##

* [Public Key Cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [Jak vytvořit soubor P7C?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

