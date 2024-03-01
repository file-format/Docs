{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - Open Financial Exchange -tiedostomuoto",
  "description":"Opi OFX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OFX-tiedostoja.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-fi",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Mikä on OFX-tiedosto?

OFX (Open Financial Exchange) -tiedosto on rahoitustiedostomuoto, jota käytetään taloudellisten tietojen vaihtoon ohjelmistojen ja rahoituslaitosten välillä. Oman talouskirjanpidon ohjelmistoratkaisujen kehityksen myötä on kehitetty ohjelmistoja, jotka voivat muodostaa yhteyden pankkiisi ja tuoda tai viedä taloustietoja pankkien kanssa. Tämä sisältää taloustiedot, kuten tapahtumat, tilitiedot ja laskujen maksut. Ohjelmistot, kuten QuickBooks, Microsoft Money, Intuit ja Quicken, tallentavat tuodut tiedot OFX-tiedostona.

OFX-tiedostomuodon Internet-mediatyyppi on application/x-ofx.

## OFX tiedostomuoto

OFX-tiedostot tallennetaan XML-tiedostomuodossa (Extensible Markup Language) ja käyttävät tageja tietojen jäsentämiseen. [XML](/web/xml/)-tiedostot on tallennettu ihmisen luettavassa muodossa, ja niitä voidaan avata ja muokata missä tahansa tekstieditorissa, kuten Notepadissa, Notepad++:ssa tai Apple TextEditissä. OFX-tiedostoihin tallennetut tiedot perustuvat **SGML (Standard Generalized Markup Language)** -standardiin. OFX-tiedostoihin tallennetut tiedot sisältävät yleensä:

* Pankkeja koskevat tiedot

* Luotto- ja pankkikorttitiedot

* Tilit ja sijoitustiedot

* kaikki muut rahoitustapahtumat


### Esimerkki OFX-tiedostomuodosta

Seuraavassa on esimerkki OFX-tiedoston sisäinen tietorakenne ja esimerkkitiedot.

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

Tämä esimerkki OFX-tiedosto sisältää seuraavat tiedot:

 * Pankkitilin tiedot, kuten pankin nimi, tilinumero ja saldo
 * Luettelo tapahtumista, mukaan lukien kunkin tapahtuman päivämäärä, tyyppi ja summa

Kaikki nämä tiedot voidaan tuoda henkilökohtaiseen rahoitusohjelmistoon tilin tapahtumien ja kulujen seuraamiseksi.

## Viitteet ##

* [Avoin rahoituspörssi – Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [ISO-standardi sähköiselle tiedonsiirrolle](https://en.wikipedia.org/wiki/ISO_20022)


