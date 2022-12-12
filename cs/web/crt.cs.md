{
  "date" : "2019-10-11",
  "keywords" :[ "crt", "soubor crt", "formát souboru crt", "typ souboru crt", "soubor", "typ", "co je soubor crt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - Formát souboru bezpečnostního certifikátu",
  "description":"Další informace o formátu souborů CRT a rozhraních API, která mohou vytvářet a otevírat soubory CRT.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor CRT?

Soubor s příponou .crt je soubor bezpečnostního certifikátu, který používají zabezpečené webové stránky k navázání zabezpečeného připojení z webového serveru k prohlížeči. Zabezpečené webové stránky umožňují zabezpečit datové přenosy, přihlášení, transakce platebními kartami a poskytují chráněné procházení webu. Pokud otevřete zabezpečený web, uvidíte v adresním řádku ikonu „zámku“. Pokud na něj kliknete, zobrazí se podrobnosti o nainstalovaném certifikátu. Tyto certifikáty SSL distribuují mezinárodní společnosti jako Verisign a Thawte.

## Formát souboru CRT

Soubory CRT jsou ve formátu ASCII a lze je otevřít v libovolném textovém editoru a zobrazit obsah souboru certifikátu. Řídí se certifikačním standardem X.509, který definuje strukturu certifikátu. Definuje datová pole, která by měla být součástí certifikátu SSL. CRT patří do formátu PEM certifikátů, které jsou soubory s kódováním Base64 ASCII.

### Struktura souboru PEM

Soubor PEM může mít více certifikátů. V takovém případě má každý certifikát v souboru PEM následující strukturu.

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

### Příklad formátu souboru CRT

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Reference ##

* [Veřejné klíče, soukromé klíče a certifikáty](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

