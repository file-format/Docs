{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX – Open Financial Exchange-Dateiformat",
  "description":"Erfahren Sie mehr über das OFX-Dateiformat und APIs, mit denen OFX-Dateien erstellt und geöffnet werden können.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Was ist eine OFX-Datei?

Eine OFX-Datei (Open Financial Exchange) ist ein Finanzdateiformat, das für den Austausch von Finanzinformationen zwischen Softwareprogrammen und Finanzinstituten verwendet wird. Mit der Entwicklung von Softwarelösungen für die interne Finanzbuchhaltung wurden Softwareprogramme entwickelt, die eine Verbindung zu Ihrer Bank herstellen und Finanzdaten mit den Banken importieren oder exportieren können. Dazu gehören Finanzdaten wie Transaktionen, Kontoinformationen und Rechnungszahlungen. Softwareprogramme wie QuickBooks, Microsoft Money, Intuit und Quicken speichern die importierten Daten als OFX-Datei.

Der Internet-Medientyp für das OFX-Dateiformat ist application/x-ofx.

## OFX-Dateiformat

OFX-Dateien werden im XML-Dateiformat (Extensible Markup Language) gespeichert und verwenden Tags zur Strukturierung der Daten. [XML](/web/xml/)-Dateien werden in einem für Menschen lesbaren Format gespeichert und können in jedem Texteditor wie Notepad, Notepad++ oder Apple TextEdit geöffnet und bearbeitet werden. Die in den OFX-Dateien gespeicherten Daten basieren auf dem Standard **SGML (Standard Generalized Markup Language)**. Zu den in OFX-Dateien gespeicherten Daten gehören normalerweise:

* Informationen zu Banken
* Kredit- und Debitkarteninformationen
* Informationen zu Konten und Investitionen
* alle anderen Finanztransaktionen

### Beispiel für ein OFX-Dateiformat

Im Folgenden finden Sie die interne Datenstruktur und Beispieldaten einer Beispiel-OFX-Datei.

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

Diese Beispiel-OFX-Datei enthält die folgenden Informationen:

* Bankkontoinformationen wie Bankname, Kontonummer und Kontostand
* Liste der Transaktionen einschließlich Datum, Art und Betrag jeder Transaktion

Alle diese Informationen können in ein persönliches Finanzsoftwareprogramm importiert werden, um den Überblick über Kontotransaktionen und Ausgaben zu behalten.

## Verweise ##

* [Open Financial Exchange – Von Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO-Standard für elektronischen Datenaustausch](https://en.wikipedia.org/wiki/ISO_20022)

