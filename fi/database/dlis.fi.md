{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi DLIS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DLIS-tiedostoja.",
  "title" : "DLIS-tiedostomuoto - hyvin lokitietotiedosto",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-fi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Mikä on DLIS-tiedosto?

.dlis-tiedostomuoto on tavallinen tiedostomuoto kaivon lokitietojen tallentamiseen ja vaihtoon öljy- ja kaasuteollisuudessa. Formaa on kehittänyt Logging Industry Data Standard (LIDS) -komitea, ja se tarkoittaa Digital Log Information Standardia. Formaatti on suunniteltu tallentamaan hyvin lokitietoja tavalla, jota on helppo lukea, kirjoittaa ja vaihtaa eri järjestelmien välillä.

DLIS-tiedostot sisältävät joukon loogisia tietueita, jotka kuvaavat kaivon lokitietoa ja sen ominaisuuksia, kuten lokitietojen tyyppiä (esim. ominaisvastus, gammasäde), mittayksiköt ja tietojen sijainnin kaivossa. Varsinaiset lokitiedot tallennetaan erillisiin binääritiedostoihin, ja DLIS-tiedoston loogiset tietueet viittaavat niihin.

## Lyhyt tieto kaivon lokitiedoista

Kaivon lokitiedot ovat kaivon eri syvyyksillä tehdyt mittaukset, tyypillisesti porauksen aikana tai kaivon porauksen jälkeen. Nämä mittaukset voivat sisältää erilaisia kiven ja kaivossa olevien nesteiden fysikaalisia, kemiallisia ja/tai geofysikaalisia ominaisuuksia. Joitakin esimerkkejä kaivon lokitiedoista ovat:

- Sähkövastus: mitta kiven kyvystä vastustaa sähkövirran virtausta
- Gammasäde: kiven luonnollisen radioaktiivisuuden mitta
- Huokoisuus: mitta kivessä olevien avoimien tilojen tai huokosten määrästä
- Sonic: mittaa aikaa, joka kuluu ääniaallon kulkemiseen kiven läpi
- Tiheys: kiven massan mitta tilavuusyksikköä kohti
- Litologia: kivityypin tai muodostuman mitta

Kaivon lokitietoja käytetään eri tarkoituksiin öljy- ja kaasuteollisuudessa, kuten:

- Hiilivetyä sisältävien muodostumien sijainnin ja laadun tunnistaminen
- Kaivon tuotantopotentiaalin arviointi
- Kaivon valmistumisen ja stimuloinnin suunnittelu ja seuranta
- Kaivon käyttäytymisen seuranta ajan mittaan

## Suhde PPDM:ään

PPDM (Professional Petroleum Data Management) on öljy- ja kaasuteollisuuden tiedonhallintastandardi, joka tarjoaa yhteisen tietomallin kaivon- ja tuotantotietojen hallintaan. PPDM-tietomalli määrittää joukon vakiotietoobjekteja ja -suhteita, joita voidaan käyttää kaivon lokitietojen, mukaan lukien DLIS-tietojen, järjestämiseen ja hallintaan.

PPDM-tietomalli sisältää tietoobjekteja kaivo- ja tuotantotiedoille, kuten kaivot, kaivon otsikot, kaivon lokit ja tuotantotiedot. Se sisältää myös näiden tietoobjektien välisiä suhteita, kuten kaivon ja siihen liittyvien kaivon lokien välisen suhteen.

PPDM-tietomalli tarjoaa yhtenäisen, alan standardien mukaisen tavan järjestää ja hallita lokitietoja, mukaan lukien DLIS-tiedot. Sen avulla eri organisaatiot voivat jakaa ja vaihtaa tietoja käyttämällä yhteistä tietomallia, mikä parantaa tietojen yhteentoimivuutta ja vähentää tietojen integrointikustannuksia.

PPDM-tietomallin ja DLIS-tietojen käyttö yhdessä mahdollistaa lokitietojen tallentamisen ja hallinnan tavalla, joka on alan standardien mukainen ja helposti muiden järjestelmien ja sovellusten käytettävissä.


