{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru KEY a rozhraních API, která mohou vytvářet a otevírat soubory KEY.",
  "title" :"KEY File Format - Privacy-Enhanced Mail Private Key File",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Co je soubor KEY?

Soubor KEY je soukromá část bezpečnostního mechanismu, který se ukládá na disk ve formátu souboru PEM (Privacy-Enhanced Mal). Používá se k dešifrování informací vyměňovaných mezi webovým prohlížečem a webovým serverem, který obsluhuje požadavky na prohlížení. Soubor KEY obsahuje zakódované řetězce, které jsou pro lidské oko nepoužitelné, ale jsou podstatou šifrování/dešifrování výměny informací v rámci SSL certifikátu na webových serverech. Soubory KEY se generují automaticky a instalují se na konec klienta.

Soubory **KEY** můžete otevřít pomocí libovolného textového editoru, jako je Microsoft Notepad (Windows), Apple TextEdit (Mac) nebo GitHub Atom (pro více platforem). Soubory KEY jsou podobné formátům souborů [CRT](/cs/web/crt/) a [CER](/cs/web/cer/).

## KEY Formát souboru – Další informace

Soubory KEY se ukládají na disk jako soubory ve formátu prostého textu, ale jsou to zakódované řetězce, jejichž čtení není pro člověka příjemné. Při otevření v textovém editoru nemají uživatelé prakticky žádné porozumění řetězcům. Certifikát soukromého klíče je důvěrný a neměl by být s nikým sdílen. Kompletní proces zabezpečení výměny informací přes internet zahrnuje:

* **Veřejný klíč** – používá se k šifrování informací uživatele pro výměnu dat mezi prohlížečem a webovými servery
* **Soukromý klíč** – používá se k dešifrování informací tak, jak jsou přijímány webovým serverem

Certifikáty SSL, známé také jako certifikáty X.509, jsou jedinečné pro každý web. KEY soubory s následující syntaxí:

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

### Příklad souboru KEY

Následuje příklad souboru soukromého klíče.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## Reference

* [Veřejné klíče, soukromé klíče a certifikáty](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

