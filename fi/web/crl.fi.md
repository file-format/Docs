{
  "date": "2022-09-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CRL-tiedosto - sertifikaattien peruutusluettelo",
  "description": "Lisätietoja CRL-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata CRL-tiedostoja.",
  "linktitle": "CRL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cr-fil"
}
},
  "lastmod": "2022-09-01"
}

## Mikä on CRL-tiedosto?

CRL (Certificate Revocation List) -tiedosto on musta lista digitaalisista X.509-sertifikaateista, jotka varmentaja (CA) peruuttaa ennen niille määritettyä peruutuspäivää. Se sisältää tietoja ongelmasta ja peruutuspäivämäärästä, jonka avulla suojauksen järjestelmänvalvojat voivat estää kyseessä olevat digitaaliset sertifikaatit. CRL ei sisällä vanhentuneita varmenteita, sillä sen päätarkoitus on ilmoittaa epäluotetuista ja virheellisistä varmenteista.

Sovelluksia, jotka voivat **avata CRL-tiedostoja**, ovat OpenSSL, Microsoft IIS Server ja Citrix NetScaler.

## CRL-tiedostomuoto - lisätietoja

CRL-tiedostot sisältävät X.509-standardin tietoja, jotka myös määrittelevät sen semantiikan julkisen avaimen tietojen jakamiseen. Muita CRL-tiedoston sisältämiä tietoja voivat olla aikaraja, jolle varmenteet on peruutettu, peruutuksen syy, peruutetun varmenteen sarjanumero ja aikaleima.


### Yleisimmät syyt sertifikaattien lisäämiseen CRL:ään

Sivustosi varmenteen kumoamiseen ja CRL:ään lisäämiseen voi olla useita syitä. Jotkut heistä voisivat olla;

1. Varmenteesi yksityinen avain on vaarantunut
1. Varmenteesi ei ole kelvollinen tai CA on myöntänyt sen väärin
1. Varmenteeseen liittyvät organisaatiotiedot muuttuvat ja CA myöntää uuden varmenteen
1. Mikä tahansa muu väistämätön syy, jonka vuoksi varmenne on peruutettu

## Viitteet

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)

* [Internet Engineering Task Forcen (IETF) RFC 5280](https://tools.ietf.org/html/rfc5280)

* [Sertifikaatin peruutuslista](https://en.wikipedia.org/wiki/Certificate_revocation_list)


