{
  "date": "2020-08-20",
  "keywords": [
"eot tiedosto",
"eot tiedostomuoto",
"mikä on eot-tiedosto",
"tiedosto",
"eot esimerkki",
"eot tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EOT - TrueType-fonttitiedostomuoto",
  "description": "Opi EOT-tiedostomuodosta ja sovellusliittymistä EOT-tiedostojen luomiseen ja avaamiseen.",
  "linktitle": "EOT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-eo-fit"
}
},
  "lastmod": "2020-10-21"
}

## Mikä on EOT-tiedosto?

Tiedosto, jonka tunniste on .eot, on OpenType-kirjasin, joka on upotettu asiakirjaan. Näitä käytetään enimmäkseen verkkotiedostoissa, kuten Web-sivuilla. Sen on luonut Microsoft, ja sitä tukevat Microsoft-tuotteet, mukaan lukien PowerPoint-esitystiedosto [.pps](/presentation/pps/). Tiedosto ei ole ensisijainen käyttötarkoitus, ja se on eräänlainen pääasiakirjan tai verkkosivun oheisasiakirja. Kuten OTF-fontit, EOT tukee sekä Postscript- että TrueType-ääriviivat kuvioille. EOT-tiedostot ovat kooltaan pienempiä siitä syystä, että ne pakataan LZ-pakkauksella. EOT käyttää Microsoft-työkalua luodakseen fontin olemassa olevista TTF/OTF-fonteista.

## Lyhyt historia

EOT-fontti toimitettiin W3C:lle vuonna 2007 osana CSS3:a, mutta sen vaatimuksen vuoksi olla pysyvästi asennettu etäjärjestelmään, tuli sen hylkäämisen syy. Se lähetettiin uudelleen maaliskuussa 2008, mutta W3C valitsi lopulta [Web Font Format](/font/woff/) (WOFF), joka standardisoitiin silloin.

## EOT-tiedostomuoto

EOT-tiedostomuodon tiedot löytyvät osoitteesta [W3 submission page](https://www.w3.org/Submission/EOT/#FileFormat), ja ne tarkentavat tämän fonttimuodon käyttämää rakennetta. EOT koostuu yhdestä EMBEDDEDFONT-rakenteesta, joka tarjoaa riittävästi perustietoa hte-fontin nimestä ja tuetuista merkeistä. Näiden tietojen pakkaus antaa käyttäjäagenteille mahdollisuuden välttää fontin purkamista, purkamista tai asentamista, jos se on jo koneessa.

### EMBEDDEDFONT Rakenne
EMBEDDEDFONT-rakenteeseen on tehty kolme versiota, ja rakenteen loppuun on lisätty lisätiedot jokaisen version yhteydessä. EMBEDDEDFONT-rakenteen viimeisin versio on kuvattu alla.

|Tietotyyppi|Syötteen nimi|Kuvaus|
---|---|---|
|unsigned long|EOTSize|Rakenteen kokonaispituus tavuina (mukaan lukien merkkijono- ja fonttitiedot)|
|unsigned long|FontDataSize|OpenType-kirjasimen pituus (FontData) tavuina|
|unsigned long|Versio|Tämän muodon versionumero - 0x00020002|
|allekirjoittamaton pitkä|Liput|Lippujen käsittely|
|byte[10]|FontPANOSE|Tämän fontin PANOSE-arvo - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|Windowsissa tämä on johdettu tekstistä TEXTMETRIC.tmCharSet. Tämä arvo määrittää fontin merkistön. DEFAULT_CHARSET (0x01) ilmaisee, ettei asetusta ole. - Katso https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Jos ITALIC-bitti on asetettu OS/2.fsSelectionissa, arvo on 0x01 - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|Tämän fontin painoarvo - katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Typpiliput, jotka antavat tietoa upotusoikeuksista - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|EOT-tiedoston maaginen numero - 0x504C. Käytetään tietojen korruption tarkistamiseen.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bitit 0-31) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bitit 32-63) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bitit 64-95) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bitit 96-127) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bitit 0-31) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bitit 32-63) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|allekirjoittamaton pitkä|Varattu1|Varattu - täytyy olla 0|
|allekirjoittamaton pitkä|Varattu2|Varattu - täytyy olla 0|
|allekirjoittamaton pitkä|Varattu3|Varattu - täytyy olla 0|
|allekirjoittamaton pitkä|Varattu4|Varattu - täytyy olla 0|
|unsigned short|Padding1|Täyte säilyttää pitkän kohdistuksen. Täytearvo on aina asetettava arvoon 0x0000.|
|unsigned short|FamilyNameSize|FamilyName-taulukon käyttämien tavujen määrä|
|byte|FamilyName[FamilyNameSize]|UTF-16-merkkien joukko, jonka pituus on FamilyNameSize-tavua. Tämä on englanninkielinen Font Family -merkkijono, joka löytyy fontin nimitaulukosta (nimi ID = 1) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Täytearvo on aina asetettava arvoon 0x0000.|
|unsigned short|StyleNameSize|StyleNamen käyttämien tavujen määrä|
|byte|StyleName[StyleNameSize]|UTF-16-merkkien joukko, jonka pituus on StyleNameSize-tavua. Tämä on englanninkielinen Font Subfamily -merkkijono, joka löytyy fontin nimitaulukosta (nimi ID = 2) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Täytearvo on aina asetettava arvoon 0x0000.|
|unsigned short|VersionNameSize|VersionName:n käyttämien tavujen määrä|
|bytes|VersionName[VersionNameSize]|UTF-16-merkkien joukko, jonka pituus on VersionNameSize-tavua. Tämä on englanninkielisen version merkkijono, joka löytyy fontin nimitaulukosta (nimi ID = 5) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Täytearvo on aina asetettava arvoon 0x0000.|
|unsigned short|FullNameSize|FullName:n käyttämien tavujen määrä|
|byte|FullName[FullNameSize]|UTF-16-merkkien joukko, jonka pituus on FullNameSize-tavua. Tämä on englanninkielinen koko nimimerkkijono, joka löytyy fontin nimitaulukosta (nimi ID = 4) - Katso https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Täytearvo on aina asetettava arvoon 0x0000.|
|unsigned short|RootStringSize|RootString-taulukon käyttämien tavujen määrä|
|byte|RootString[RootStringSize]|UTF-16-merkkien joukko, jonka pituus on RootStringSize tavua.|
|unsigned long|RootStringCheckSum|RootString CheckSum arvo. Katso rootStringChecksum-prosessointialgoritmi alla.|
|unsigned long|EUDCCodePage|EUDC-fonttitukeen tarvitaan koodisivun arvo.|
|unsigned short|Padding6|Täytearvo on aina asetettava arvoon 0x0000.|
|unsigned short|SignatureSize|Signature-taulukon käyttämien tavujen määrä. Tällä hetkellä varattu ja sen arvoksi tulisi asettaa 0x0000.|
|byte|Allekirjoitus[SignatureSize]|Tällä hetkellä varattu. Jos SignatureSize on 0x0000, tällä taulukolla ei ole pituutta.|
|allekirjoittamaton pitkä|EUDCFlags|Käsittelyssä EUDC-fontin lippuja. Tyypilliset arvot voivat olla TTEMBED_XORENCRYPTDATA ja TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Signature-taulukon käyttämien tavujen määrä.|
|byte|EUDCFontData[EUDCFontSize]|EUDC-fonttidataan käytettyjen tavujen määrä. Jos EUDCFontSize on 0x00000000, tällä taulukolla ei ole pituutta.|
|byte|FontData[FontDataSize]|Tämän EOT-tiedoston fonttitiedot. Tiedot voidaan pakata tai XOR-salata, kuten käsittelyliput osoittavat.|

## Viitteet

 * [EOT-tiedostomuoto](https://www.w3.org/Submission/EOT/)
 * [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
 * [Fontin upottaminen](https://en.wikipedia.org/wiki/Font_embedding)

