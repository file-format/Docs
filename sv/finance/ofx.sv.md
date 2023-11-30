{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Open Financial Exchange File Format",
  "description":"Läs mer om OFX-filformat och API:er som kan skapa och öppna OFX-filer.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Vad är OFX fil?

En OFX-fil (Open Financial Exchange) är ett finansiellt filformat som används för utbyte av finansiell information mellan program och finansiella institutioner. Med utvecklingen av mjukvarulösningar för intern finansiell bokföring har program utvecklats som kan ansluta till din bank och importera eller exportera finansiell data med bankerna. Detta inkluderar finansiella data som transaktioner, kontoinformation och betalningar av räkningar. Programvaror som QuickBooks, Microsoft Money, Intuit och Quicken sparar importerade data som OFX-fil.

Internetmedietypen för OFX-filformat är application/x-ofx.

## OFX filformat

OFX-filer sparas i XML-filformat (Extensible Markup Language) och använder taggar för att strukturera data. [XML](/sv/web/xml/)-filer lagras i läsbart format och kan öppnas och redigeras i vilken textredigerare som helst som Notepad, Notepad++ eller Apple TextEdit. Data som lagras i OFX-filerna är baserade på standarden **SGML (Standard Generalized Markup Language)**. Data som lagras i OFX-filer inkluderar vanligtvis:

* Information relaterad till banker
* Kredit- och betalkortsinformation
* Information om konton och investeringar
* alla andra finansiella transaktioner

### Exempel på OFX-filformat

Följande är den interna datastrukturen och exempeldata för ett exempel på OFX-fil.

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

Detta exempel på OFX-fil innehåller följande information:

* Bankkontoinformation som banknamn, kontonummer och saldo
* Lista över transaktioner inklusive datum, typ och belopp för varje transaktion

All denna information kan importeras i ett personligt ekonomiprogram för att hålla reda på kontotransaktioner och utgifter.

## Referenser ##

* [Open Financial Exchange - av Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO-standard för elektroniskt datautbyte](https://en.wikipedia.org/wiki/ISO_20022)

