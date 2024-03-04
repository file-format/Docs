{
  "date": "2022-09-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRL failas – sertifikatų panaikinimo sąrašas",
  "description": "Sužinokite apie CRL failo formatą ir API, kurios gali kurti ir atidaryti CRL failus.",
  "linktitle": "CRL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-ltl"
}
},
  "lastmod": "2022-09-01"
}

## Kas yra CRL failas?

CRL (Certificate Revocation List) failas yra juodasis X.509 skaitmeninių sertifikatų, kuriuos sertifikatų institucija (CA) atšaukia prieš jiems priskirtą atšaukimo datą, sąrašas. Jame pateikiama informacija apie problemą ir atšaukimo datą, kuri leidžia saugos administratoriams blokuoti paveiktus skaitmeninius sertifikatus. CRL neapima pasibaigusių sertifikatų, nes pagrindinis jo tikslas yra pranešti apie nepatikimus ir negaliojančius sertifikatus.

Programos, kurios gali **atidaryti CRL failus**, apima OpenSSL, Microsoft IIS Server ir Citrix NetScaler.

## CRL failo formatas – daugiau informacijos

CRL failuose yra X.509 standarto informacijos, kuri taip pat apibrėžia jo semantiką, skirtą dalytis viešojo rakto informacija. Kita informacija, esanti CRL faile, gali apimti laikotarpį, kuriam sertifikatai buvo atšaukti, atšaukimo priežastį, atšaukto sertifikato serijos numerį ir laiko žymą.


### Pagrindinės priežastys, dėl kurių sertifikatai pridedami prie CRL

Gali būti keletas priežasčių, kodėl jūsų svetainės sertifikatas buvo atšauktas ir įtrauktas į CRL. Kai kurie iš jų gali būti;

1. Jūsų sertifikato privatus raktas buvo pažeistas
1. Jūsų sertifikatas negalioja arba jį klaidingai išdavė CA
1. Pakeičiami su sertifikatu susiję organizacijos duomenys ir CA išduoda naują sertifikatą
1. Bet kuri kita neišvengiama priežastis, dėl kurios sertifikatas buvo panaikintas

## Nuorodos

* [Nacionalinis standartų ir technologijų institutas (NIST)](https://csrc.nist.gov/glossary/term/CRL)

* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)

* [Sertifikatų panaikinimo sąrašas](https://en.wikipedia.org/wiki/Certificate_revocation_list)


