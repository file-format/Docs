{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Format de fișier de schimb financiar deschis",
  "description":"Aflați despre formatul de fișier OFX și despre API-urile care pot crea și deschide fișiere OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Ce este un fișier OFX?

Un fișier OFX (Open Financial Exchange) este un format de fișier financiar utilizat pentru schimbul de informații financiare între programele software și instituțiile financiare. Odată cu evoluția soluțiilor software pentru evidența contabilă financiară internă, au fost dezvoltate programe software care se pot conecta la banca dumneavoastră și pot importa sau exporta date financiare cu băncile. Acestea includ date financiare, cum ar fi tranzacții, informații despre cont și plăți ale facturilor. Programele software precum QuickBooks, Microsoft Money, Intuit și Quicken salvează datele importate ca fișier OFX.

Tipul media de internet pentru formatul de fișier OFX este application/x-ofx.

## Format de fișier OFX

Fișierele OFX sunt salvate în format de fișier XML (Extensible Markup Language) și utilizează etichete pentru a structura datele. Fișierele [XML](/ro/web/xml/) sunt stocate în format ușor de citit și pot fi deschise și editate în orice editor de text, cum ar fi Notepad, Notepad++ sau Apple TextEdit. Datele stocate în fișierele OFX se bazează pe standardul **SGML (Standard Generalized Markup Language)**. Datele stocate în fișierele OFX includ de obicei:

* Informații legate de bănci
* Informații despre cardul de credit și debit
* Informații despre conturi și investiții
* orice alte tranzactii financiare

### Exemplu de format de fișier OFX

Mai jos este structura internă a datelor și datele eșantion ale unui exemplu de fișier OFX.

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

Acest exemplu de fișier OFX conține următoarele informații:

* Informații despre contul bancar, cum ar fi numele băncii, numărul contului și soldul
* Lista tranzacțiilor, inclusiv data, tipul și suma fiecărei tranzacții

Toate aceste informații pot fi importate într-un program software de finanțe personale pentru a ține evidența tranzacțiilor și cheltuielilor contului.

## Referințe ##

* [Open Financial Exchange - Prin Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Standard ISO pentru schimbul electronic de date](https://en.wikipedia.org/wiki/ISO_20022)

