{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MBOX - sähköpostin postilaatikkotiedosto",
  "description": "Opi MBOX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MBOX-tiedostoja.",
  "linktitle": "MBOX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-mbo-fix"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on MBOX-tiedosto?

MBox-tiedostomuoto on yleinen termi, joka edustaa säilöä sähköpostiviestien keräämiseen. Viestit tallennetaan säilöön liitteineen. Koko kansion viestit tallennetaan yhteen tietokantatiedostoon ja uudet viestit liitetään tiedoston loppuun. Lukuisat sovellukset ja API tukevat MBox-tiedostomuotoja, kuten Apple Mail ja Mozilla Thunderbird.

## MBOX-tiedostomuoto ##

The MBox file format remained non-standardized for quite long time until 2005 when the application/mbox  was standardized as [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) Messages, in RFC 2822 format, are concatenated inside MBox file format one after another. Each message begins with a separator line that identifies the message sender, and also identifies the date and time at which the message was received by the final recipient (either the last-hop system in the transfer path, or the system which serves as the recipient's mailstore). Each message is typically terminated by an empty line. The end of the database is usually recognized by either the absence of any additional data, or by the presence of an explicit end-of-file marker.

## Viestin lukeminen MBox-tiedostosta ##

Lukija skannaa mbox-tiedoston ja etsii From_ rivejä. Mikä tahansa Lähettäjä_-rivi merkitsee viestin alun. Lukijan ei tule yrittää käyttää hyväkseen sitä, että jokainen From_-rivi (tiedoston alun jälkeen) on tyhjä. Kun lukija löytää viestin, se poimii (mahdollisesti vioittuneen) kirjekuoren lähettäjän ja toimituspäivämäärän From_-riviltä. Sen jälkeen se lukee seuraavaan From_-riville tai tiedoston loppuun asti sen mukaan, kumpi tulee ensin. Se poistaa viimeisen tyhjän rivin ja poistaa lainaukset riviltä >Riveiltä ja >>Riveiltä ja niin edelleen. Tuloksena on RFC 822 -sanoma.

## Koodausta koskevia huomioita ##

MBox-tiedoston sisältö voi sekoittua peruuttamattomasti, kun vastaanotettu sähköposti sisältää Mbox-tiedoston liitteenä ja tallennetaan toiseen Mbox-tiedostoon. Tämän välttämiseksi viestijärjestelmien on koodattava mbox-tietokanta läpinäkymättömällä siirtokoodauksella (kuten BASE64 tai Quoted-Printable), kun tällainen objekti siirretään viestinvälitysprotokollien kautta. Toteuttajien tulee myös olla valmiita koodaamaan mbox-tiedot paikallisesti, jos vastaanotetaan ei-yhteensopivia tietoja.

## Viitteet ##

* [MBox - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)

* [Mbox - Wikipedia](https://en.wikipedia.org/wiki/Mbox)


