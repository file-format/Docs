{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - Åbn Financial Exchange-filformat",
  "description":"Lær om OFX-filformat og API'er, der kan oprette og åbne OFX-filer.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-da",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Hvad er en OFX fil?

En OFX (Open Financial Exchange) fil er et finansielt filformat, der bruges til udveksling af finansiel information mellem softwareprogrammer og finansielle institutioner. Med udviklingen af softwareløsninger til intern finansiel bogføring er der udviklet softwareprogrammer, der kan oprette forbindelse til din bank og importere eller eksportere finansielle data med bankerne. Dette omfatter finansielle data såsom transaktioner, kontooplysninger og regningsbetalinger. Softwareprogrammer som QuickBooks, Microsoft Money, Intuit og Quicken gemmer de importerede data som OFX-fil.

Internetmedietypen for OFX-filformatet er application/x-ofx.

## OFX filformat

OFX-filer gemmes i XML-filformat (Extensible Markup Language) og bruger tags til at strukturere dataene. [XML](/web/xml/) filer gemmes i et menneskeligt læsbart format og kan åbnes og redigeres i ethvert tekstredigeringsprogram, såsom Notesblok, Notesblok++ eller Apple TextEdit. Dataene gemt i OFX-filerne er baseret på **SGML (Standard Generalized Markup Language)**-standarden. Data gemt i OFX-filer inkluderer typisk:

* Oplysninger relateret til banker

* Kredit- og betalingskortoplysninger

* Konti og investeringsoplysninger

* alle andre finansielle transaktioner


### Eksempel på OFX-filformat

Følgende er den interne datastruktur og eksempeldata for et eksempel på OFX-fil.

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

Dette eksempel på OFX-fil indeholder følgende oplysninger:

 * Bankkontooplysninger såsom banknavn, kontonummer og saldo
 * Liste over transaktioner inklusive dato, type og beløb for hver transaktion

Alle disse oplysninger kan importeres i et personligt finansprogram for at holde styr på kontotransaktioner og -udgifter.

## Referencer ##

* [Open Financial Exchange - Af Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [ISO-standard for elektronisk dataudveksling](https://en.wikipedia.org/wiki/ISO_20022)


