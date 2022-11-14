{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File CSR - Formato del file di richiesta di firma del certificato",
  "description" :"Scopri cos'è un file CSR e le API che possono creare e aprire file CSR.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## Che cos'è un file CSR?

Un file CSR è un file **Richiesta di firma del certificato** utilizzato per richiedere il certificato SSL/TLS. Quando devi avere il tuo certificato SSL/TLS, generi il CSR sullo stesso server dove verrà finalmente installato. Questo file CSR è condiviso con l'Autorità di certificazione (CA) per la creazione del certificato. Contiene informazioni come nome comune, organizzazione, paese e, soprattutto, la **chiave pubblica** integrata nel file del certificato e firmata con la chiave privata corrispondente.

Le applicazioni che possono **aprire file CSR** includono OpenSSL e Microsoft IIS.

## Formato del file di richiesta di firma del certificato

Un file CSR viene creato in un formato PEM Base-64 che può essere aperto e visualizzato in un semplice editor di testo come Microsoft Notepad. Include un'intestazione **-----INIZIO NUOVA RICHIESTA DI CERTIFICATO-----** all'inizio del file e un piè di pagina **-----FINE NUOVA RICHIESTA DI CERTIFICATO-----** a la fine del file.

### Come appare un file CSR?

Un semplice esempio di file CSR è il seguente.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## Quali informazioni sono incluse in una CSR?

Un file CSR contiene le seguenti informazioni.

1. "Informazioni sull'attività e sul sito Web": include informazioni come nome comune, organizzazione, unità organizzativa, città/località, stato/contea/regione (S), paese e indirizzo e-mail
1. `Chiave pubblica` - È inclusa nel certificato e viene utilizzata per crittografare i dati trasmessi che vengono decrittati utilizzando la chiave privata corrispondente
1. "Informazioni sul tipo e sulla lunghezza della chiave" - Di solito si tratta di RSA 2048, ma può anche essere disponibile in dimensioni maggiori come RSA 4096+

## Riferimenti

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

