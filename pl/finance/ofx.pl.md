{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Otwarty format pliku wymiany finansowej",
  "description":"Dowiedz się o formacie pliku OFX i interfejsach API, które umożliwiają tworzenie i otwieranie plików OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Czym jest plik OFX?

Plik OFX (Open Financial Exchange) to format pliku finansowego używany do wymiany informacji finansowych pomiędzy programami a instytucjami finansowymi. Wraz z ewolucją rozwiązań programowych do wewnętrznego prowadzenia ksiąg rachunkowych opracowano programy, które mogą łączyć się z bankiem i importować lub eksportować dane finansowe z bankami. Obejmuje to dane finansowe, takie jak transakcje, informacje o koncie i płatności za rachunki. Programy takie jak QuickBooks, Microsoft Money, Intuit i Quicken zapisują zaimportowane dane jako plik OFX.

Typ mediów internetowych dla formatu pliku OFX to aplikacja/x-ofx.

## Format pliku OFX

Pliki OFX są zapisywane w formacie pliku XML (Extensible Markup Language) i wykorzystują znaczniki do strukturyzowania danych. Pliki [XML](/pl/web/xml/) są przechowywane w formacie czytelnym dla człowieka i można je otwierać i edytować w dowolnym edytorze tekstu, takim jak Notatnik, Notepad++ lub Apple TextEdit. Dane przechowywane w plikach OFX oparte są na standardzie **SGML (Standard Generalized Markup Language)**. Dane przechowywane w plikach OFX zazwyczaj obejmują:

* Informacje dotyczące banków
* Informacje o karcie kredytowej i debetowej
* Informacje o kontach i inwestycjach
*wszelkie inne transakcje finansowe

### Przykład formatu pliku OFX

Poniżej znajduje się wewnętrzna struktura danych i przykładowe dane przykładowego pliku OFX.

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

Ten przykładowy plik OFX zawiera następujące informacje:

* Informacje o koncie bankowym, takie jak nazwa banku, numer konta i saldo
* Lista transakcji zawierająca datę, rodzaj i kwotę każdej transakcji

Wszystkie te informacje można zaimportować do programu do finansów osobistych, aby śledzić transakcje i wydatki na koncie.

## Bibliografia ##

* [Otwarta giełda finansowa – według Wikipedii](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Norma ISO dotycząca elektronicznej wymiany danych](https://en.wikipedia.org/wiki/ISO_20022)

