{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL-fil - Lista över återkallade certifikat",
  "description":"Läs mer om CRL-filformat och API:er som kan skapa och öppna CRL-filer.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Vad är en CRL fil?

En CRL-fil (Certificate Revocation List) är en svartlista över X.509 digitala certifikat som en certifikatmyndighet (CA) återkallar före deras tilldelade återkallelsedatum. Den innehåller information om problemet och återkallningsdatumet som gör att säkerhetsadministratörerna kan blockera berörda digitala certifikat. CRL inkluderar inte utgångna certifikat eftersom dess huvudsakliga syfte är att meddela om otillförlitliga och ogiltiga certifikat.

Applikationer som kan **öppna CRL-filer** inkluderar OpenSSL, Microsoft IIS Server och Citrix NetScaler.

## CRL-filformat - Mer information

CRL-filer innehåller information i X.509-standarden som också definierar dess semantik för delning av offentlig nyckelinformation. Annan information som finns i en CRL-fil kan inkludera tidsgränsen för vilken certifikaten har återkallats, orsaken till återkallelsen, serienummer på återkallat certifikat och tidsstämpel.


### De främsta anledningarna till att certifikat läggs till i CRL

Det kan finnas flera anledningar till att få din webbplats certifikat återkallat och läggas till i CRL. Några av dem kan vara;

1. Ditt certifikats privata nyckel har äventyrats
1. Ditt certifikat är inte giltigt eller felaktigt utfärdat av CA
1. Organisationsdetaljer associerade med certifikatet ändras och CA utfärdar ett nytt certifikat
1. Varje annan oundviklig orsak till vilken certifikatet har återkallats

## Referenser

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Certificate Revocation List](https://en.wikipedia.org/wiki/Certificate_revocation_list)

