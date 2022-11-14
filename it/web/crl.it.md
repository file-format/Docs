{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File CRL - Elenco revoche certificati",
  "description":"Scopri il formato di file CRL e le API che possono creare e aprire file CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Che cos'è un file CRL?

Un file CRL (Certificate Revocation List) è una lista nera di certificati digitali X.509 che un'autorità di certificazione (CA) revoca prima della data di revoca assegnata. Contiene informazioni sul problema e sulla data di revoca che consentono agli amministratori della sicurezza di bloccare i certificati digitali interessati. CRL non include i certificati scaduti poiché il suo scopo principale è notificare i certificati non attendibili e non validi.

Le applicazioni che possono **aprire file CRL** includono OpenSSL, Microsoft IIS Server e Citrix NetScaler.

## Formato file CRL - Ulteriori informazioni

I file CRL contengono informazioni nello standard X.509 che ne definisce anche la semantica per la condivisione delle informazioni sulla chiave pubblica. Altre informazioni contenute in un file CRL possono includere il limite di tempo per il quale i certificati sono stati revocati, il motivo della revoca, il numero di serie del certificato revocato e il timestamp.


### Principali motivi per cui i certificati vengono aggiunti a CRL

Potrebbero esserci diversi motivi per cui il certificato del tuo sito web viene revocato e aggiunto a CRL. Alcuni di loro potrebbero essere;

1. La chiave privata del tuo certificato è stata compromessa
1. Il tuo certificato non è valido o è stato emesso erroneamente dalla CA
1. I dettagli organizzativi associati al certificato vengono modificati e la CA emette un nuovo certificato
1. Ogni altro motivo ineludibile per il quale il certificato è stato revocato

## Riferimenti

* [Istituto nazionale di standard e tecnologia (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [RFC 5280 di Internet Engineering Task Force (IETF)](https://tools.ietf.org/html/rfc5280)
* [Elenco di revoca delle certificazioni](https://en.wikipedia.org/wiki/Certificate_revocation_list)

