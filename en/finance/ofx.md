{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - Open Financial Exchange File Format",
  "description":"Learn about OFX file format and APIs that can create and open OFX files.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
    }
  },
  "lastmod" : "2023-05-09"
}

## What is an OFX file?

An OFX (Open Financial Exchange) file is a financial file format used for exchange of financial information between software programs and financial institutions. With the evolution of software solutions for in-house financial accounting and [bookkeeping](https://docs.familiarize.com/glossary/bookkeeping/), software programs have been developed that can connect to your bank and import or export financial data with the banks. This includes financial data such as transactions, account information, and bill payments. Software programs such as QuickBooks, Microsoft Money, Intuit, and Quicken save the imported data as OFX file.

The Internet media type	for OFX file format is application/x-ofx.

## OFX File Format

OFX files are saved in XML (Extensible Markup Language) file format and uses tags to structure the data. [XML](/web/xml/) files are stored in human readable format and can be opened and edited in any text editor such as Notepad, Notepad++, or Apple TextEdit. The data stored inside the OFX files is based on the **SGML (Standard Generalized Markup Language)** standard. Data stored inside OFX files typically include:

* Information related to banks
* Credit and Debit Card information
* Accounts and investments information
* any other financial transactions

### OFX File Format Example

Following is the internal data structure and sample data of an example OFX file.

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

This example OFX file contains the following information:

 * Bank account information such as bank name, account number, and balance
 * List of transactions including date, type, and amount of each transaction

All this information can be imported in a personal finance software program to keep track of account transactions and expenses.

## References ##

* [Open Financial Exchange - By Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO Standard for Electronic Data Exchange](https://en.wikipedia.org/wiki/ISO_20022)
