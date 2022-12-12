{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor CRL - Seznam zneplatněných certifikátů",
  "description":"Další informace o formátu souboru CRL a rozhraních API, která mohou vytvářet a otevírat soubory CRL.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Co je soubor CRL?

Soubor CRL (Certificate Revocation List) je černou listinou digitálních certifikátů X.509, které certifikační autorita (CA) zruší před přiděleným datem odvolání. Obsahuje informace o problému a datu odvolání, které správcům zabezpečení umožňuje blokovat dotčené digitální certifikáty. CRL nezahrnuje certifikáty s prošlou platností, protože jeho hlavním účelem je informovat o nedůvěryhodných a neplatných certifikátech.

Mezi aplikace, které mohou **otevřít soubory CRL**, patří OpenSSL, Microsoft IIS Server a Citrix NetScaler.

## Formát souboru CRL – Další informace

Soubory CRL obsahují informace ve standardu X.509, který také definuje jeho sémantiku pro sdílení informací o veřejném klíči. Další informace obsažené v souboru CRL mohou zahrnovat časový limit, po který byly certifikáty zneplatněny, důvod revokace, sériové číslo revokovaného certifikátu a časové razítko.


### Hlavní důvody pro přidání certifikátů do CRL

Důvodů pro odvolání certifikátu vašeho webu a jeho přidání do CRL může být několik. Některé z nich by mohly být;

1. Soukromý klíč vašeho certifikátu byl prolomen
1. Váš certifikát není platný nebo jej certifikační úřad vydal nesprávně
1. Organizační podrobnosti spojené s certifikátem se změní a CA vydá nový certifikát
1. Jakýkoli jiný nevyhnutelný důvod, pro který byl certifikát zneplatněn

## Reference

* [Národní institut pro standardy a technologie (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Seznam odvolání certifikace](https://en.wikipedia.org/wiki/Certificate_revocation_list)

