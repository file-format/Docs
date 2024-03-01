{
  "date": "2022.01.31",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7S-tiedosto - digitaalisesti allekirjoitettu sähköpostiviesti",
  "description": "Opi P7S-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata P7S-tiedostoja.",
  "linktitle": "P7S",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-p7-fis"
}
},
  "lastmod": "2022.01.31"
}

## Mikä on P7S-tiedosto?

P7S-tiedosto on digitaalinen allekirjoitus, joka vastaanotetaan digitaalisesti allekirjoitetulla sähköpostilla. Tämän tiedoston läsnäolo sähköpostin liitteenä varmistaa, että sähköposti on lähetetty autenttisesta lähteestä. Tämä varmistaa, että lähettäjän tietokoneelle on asennettu sähköpostin allekirjoitusvarmenne. Kun tällainen allekirjoitettu sähköposti lähetetään käyttäjän tietokoneelta, siihen liitetään P7S-tiedosto, joka sisältää lähettäjän nimen. Allekirjoitettuja sähköposteja tukevat sähköpostiohjelmat voivat nähdä lähettäjän tiedot.

## P7S-tiedostomuoto – lisätietoja

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S-tiedostot sisältävät tiedot vain tekstimuodossa, joka on ihmisen luettavissa. Sähköpostiohjelmat, kuten Microsoft Outlook, Apple Mail ja Mozilla Thunderbird, tukevat digitaalisesti allekirjoitettujen tietojen lukemista S/MIME-sähköpostista. Sähköpostin allekirjoittaminen vahvistaa lähettäjän henkilöllisyyden ja kertoo vastaanottajalle, että viesti on aito. Kun sähköpostit ladataan sähköpostiohjelmista (joko nimellä [EML](/email/eml/) tai [MSG](/email/msg/)), nämä P7S-tiedostot löytyvät näiden sähköpostien liitteenä.

P7S-tiedosto sisältää seuraavat tiedot:

 * Sähköpostin lähde
 * Lähetyspäivä ja aika,
 * Onko sitä muutettu lähetyksen aikana

Nämä tiedot on upotettu käyttämällä Public-Key Cryptography Standard #7 (PKCS7) -tekniikkaa salattujen allekirjoitusten digitaaliseen liittämiseen sähköpostiin.

## Viitteet ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)


