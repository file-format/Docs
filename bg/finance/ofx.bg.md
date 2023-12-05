{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX – отворен файлов формат за финансов обмен",
  "description":"Научете за OFX файловия формат и API, които могат да създават и отварят OFX файлове.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Какво е OFX файл?

OFX (Open Financial Exchange) файл е формат на финансов файл, използван за обмен на финансова информация между софтуерни програми и финансови институции. С еволюцията на софтуерните решения за водене на вътрешни финансови счетоводни книги бяха разработени софтуерни програми, които могат да се свържат с вашата банка и да импортират или експортират финансови данни с банките. Това включва финансови данни като транзакции, информация за сметката и плащания на сметки. Софтуерни програми като QuickBooks, Microsoft Money, Intuit и Quicken записват импортираните данни като OFX файл.

Типът интернет медия за файлов формат OFX е application/x-ofx.

## Файлов формат OFX

OFX файловете се записват във файлов формат XML (Extensible Markup Language) и използват тагове за структуриране на данните. [XML](/bg/web/xml/) файловете се съхраняват в четим от човека формат и могат да се отварят и редактират във всеки текстов редактор като Notepad, Notepad++ или Apple TextEdit. Данните, съхранявани във файловете OFX, се основават на стандарта **SGML (Standard Generalized Markup Language)**. Данните, съхранявани в OFX файлове, обикновено включват:

* Информация, свързана с банките
* Информация за кредитна и дебитна карта
* Информация за сметки и инвестиции
* всякакви други финансови транзакции

### Пример за файлов формат OFX

Следва вътрешната структура на данните и примерни данни на примерен OFX файл.

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

Този примерен OFX файл съдържа следната информация:

* Информация за банковата сметка, като име на банката, номер на сметка и баланс
* Списък с транзакции, включително дата, вид и сума на всяка транзакция

Цялата тази информация може да бъде импортирана в софтуерна програма за лични финанси, за да следите транзакциите и разходите по сметката.

## Препратки ##

* [Отворен финансов обмен - от Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO стандарт за електронен обмен на данни](https://en.wikipedia.org/wiki/ISO_20022)

