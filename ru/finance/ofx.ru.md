{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX — формат файла открытой финансовой биржи",
  "description":"Узнайте о формате файлов OFX и API, с помощью которых можно создавать и открывать файлы OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## . OFX вариант №

Файл OFX (Open Financial Exchange) — это формат финансового файла, используемый для обмена финансовой информацией между программами и финансовыми учреждениями. С развитием программных решений для внутреннего финансового учета были разработаны программы, которые могут подключаться к вашему банку и импортировать или экспортировать финансовые данные из банков. Сюда входят финансовые данные, такие как транзакции, информация о счете и оплата счетов. Программное обеспечение, такое как QuickBooks, Microsoft Money, Intuit и Quicken, сохраняет импортированные данные в виде файла OFX.

Тип интернет-носителя для формата файла OFX — application/x-ofx.

## Формат файла OFX

Файлы OFX сохраняются в формате XML (расширяемый язык разметки) и используют теги для структурирования данных. Файлы [XML](/ru/web/xml/) хранятся в удобочитаемом формате и могут открываться и редактироваться в любом текстовом редакторе, например Notepad, Notepad++ или Apple TextEdit. Данные, хранящиеся в файлах OFX, основаны на стандарте **SGML (стандартный обобщенный язык разметки)**. Данные, хранящиеся в файлах OFX, обычно включают:

* Информация, связанная с банками
* Информация о кредитной и дебетовой карте
* Информация о счетах и инвестициях
* любые другие финансовые операции

### Пример формата файла OFX

Ниже приведена внутренняя структура данных и примеры данных примера файла OFX.

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

Этот пример файла OFX содержит следующую информацию:

* Информация о банковском счете, такая как название банка, номер счета и баланс.
* Список транзакций, включая дату, тип и сумму каждой транзакции.

Всю эту информацию можно импортировать в программу для управления личными финансами, чтобы отслеживать операции по счету и расходы.

## Использованная литература ##

* [Открытая финансовая биржа – Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Стандарт ISO для электронного обмена данными] (https://en.wikipedia.org/wiki/ISO_20022)

