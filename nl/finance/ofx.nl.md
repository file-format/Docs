{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Open Financial Exchange-bestandsformaat",
  "description":"Leer meer over OFX-bestandsindeling en API's die OFX-bestanden kunnen maken en openen.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Wat is een OFX-bestand?

Een OFX-bestand (Open Financial Exchange) is een financieel bestandsformaat dat wordt gebruikt voor de uitwisseling van financiële informatie tussen softwareprogramma's en financiële instellingen. Met de evolutie van softwareoplossingen voor het intern bijhouden van de financiële boekhouding zijn er softwareprogramma's ontwikkeld die verbinding kunnen maken met uw bank en financiële gegevens van de banken kunnen importeren of exporteren. Dit omvat financiële gegevens zoals transacties, accountinformatie en factuurbetalingen. Softwareprogramma's zoals QuickBooks, Microsoft Money, Intuit en Quicken slaan de geïmporteerde gegevens op als OFX-bestand.

Het internetmediatype voor OFX-bestandsindeling is application/x-ofx.

## OFX-bestandsindeling

OFX-bestanden worden opgeslagen in XML-bestandsformaat (Extensible Markup Language) en gebruiken tags om de gegevens te structureren. [XML](/nl/web/xml/)-bestanden worden opgeslagen in een voor mensen leesbaar formaat en kunnen worden geopend en bewerkt in elke teksteditor zoals Kladblok, Notepad++ of Apple TextEdit. De gegevens die in de OFX-bestanden zijn opgeslagen, zijn gebaseerd op de **SGML-standaard (Standard Generalized Markup Language)**. Gegevens die in OFX-bestanden zijn opgeslagen, omvatten doorgaans:

* Informatie met betrekking tot banken
* Credit- en debetkaartinformatie
* Rekeningen en beleggingsinformatie
* eventuele andere financiële transacties

### Voorbeeld van OFX-bestandsindeling

Hieronder volgen de interne datastructuur en voorbeeldgegevens van een voorbeeld van een OFX-bestand.

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

Dit voorbeeld OFX-bestand bevat de volgende informatie:

* Bankrekeninggegevens zoals banknaam, rekeningnummer en saldo
* Lijst met transacties, inclusief datum, type en bedrag van elke transactie

Al deze informatie kan worden geïmporteerd in een softwareprogramma voor persoonlijke financiën om accounttransacties en uitgaven bij te houden.

## Referenties ##

* [Open financiële uitwisseling - door Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO-standaard voor elektronische gegevensuitwisseling](https://en.wikipedia.org/wiki/ISO_20022)

