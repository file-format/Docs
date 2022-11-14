{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL-bestand - Certificaatintrekkingslijst",
  "description":"Meer informatie over CRL-bestandsindelingen en API's die CRL-bestanden kunnen maken en openen.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Wat is een CRL-bestand?

Een CRL-bestand (Certificate Revocation List) is een zwarte lijst van X.509 digitale certificaten die een certificeringsinstantie (CA) vóór hun toegewezen intrekkingsdatum intrekt. Het bevat informatie over het probleem en de intrekkingsdatum waarmee de beveiligingsbeheerders getroffen digitale certificaten kunnen blokkeren. CRL bevat geen verlopen certificaten omdat het belangrijkste doel is om te informeren over de niet-vertrouwde en ongeldige certificaten.

Toepassingen die **CRL-bestanden** kunnen openen, zijn onder meer OpenSSL, Microsoft IIS Server en Citrix NetScaler.

## CRL-bestandsindeling - Meer informatie

CRL-bestanden bevatten informatie in de X.509-standaard die ook de semantiek definieert voor het delen van openbare sleutelinformatie. Andere informatie in een CRL-bestand kan de tijdslimiet zijn waarvoor de certificaten zijn ingetrokken, de reden voor de intrekking, het serienummer van het ingetrokken certificaat en de tijdstempel.


### Belangrijkste redenen waarom certificaten worden toegevoegd aan CRL

Er kunnen verschillende redenen zijn waarom het certificaat van uw website wordt ingetrokken en aan de CRL wordt toegevoegd. Sommigen van hen zouden kunnen zijn;

1. De privésleutel van uw certificaat is gecompromitteerd
1. Uw certificaat is niet geldig of verkeerd uitgegeven door de CA
1. Organisatorische gegevens die aan het certificaat zijn gekoppeld, worden gewijzigd en de CA geeft een nieuw certificaat uit
1. Elke andere onvermijdelijke reden waarom het certificaat is ingetrokken

## Referenties

* [Nationaal Instituut voor Standaarden en Technologie (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [Internet Engineering Task Force (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [Lijst met intrekking van certificaten](https://en.wikipedia.org/wiki/Certificate_revocation_list)

