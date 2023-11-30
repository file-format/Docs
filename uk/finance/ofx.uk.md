{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - відкритий формат файлу фінансового обміну",
  "description":"Дізнайтеся про формат файлу OFX та API, які можуть створювати та відкривати файли OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Що таке файл OFX?

Файл OFX (Open Financial Exchange) — це формат фінансового файлу, який використовується для обміну фінансовою інформацією між програмним забезпеченням і фінансовими установами. З розвитком програмних рішень для внутрішнього фінансового обліку було розроблено програмне забезпечення, яке може підключатися до вашого банку та імпортувати або експортувати фінансові дані з банками. Сюди входять такі фінансові дані, як транзакції, інформація про обліковий запис і оплата рахунків. Такі програми, як QuickBooks, Microsoft Money, Intuit і Quicken, зберігають імпортовані дані як файл OFX.

Тип Інтернет-медіа для формату файлу OFX – application/x-ofx.

## Формат файлу OFX

Файли OFX зберігаються у форматі XML (розширювана мова розмітки) і використовують теги для структурування даних. Файли [XML](/uk/web/xml/) зберігаються у форматі, зрозумілому людині, і їх можна відкривати та редагувати в будь-якому текстовому редакторі, наприклад Notepad, Notepad++ або Apple TextEdit. Дані, що зберігаються у файлах OFX, базуються на стандарті **SGML (Standard Generalized Markup Language)**. Дані, що зберігаються у файлах OFX, зазвичай включають:

* Інформація про банки
* Інформація про кредитну та дебетову картку
* Інформація про рахунки та інвестиції
* будь-які інші фінансові операції

### Приклад формату файлу OFX

Нижче наведено внутрішню структуру даних і зразки даних прикладу файлу OFX.

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

Цей приклад файлу OFX містить таку інформацію:

* Інформація про банківський рахунок, як-от назва банку, номер рахунку та баланс
* Список операцій, включаючи дату, тип і суму кожної операції

Усю цю інформацію можна імпортувати в програмне забезпечення для персональних фінансів, щоб відстежувати операції та витрати на рахунку.

## Посилання ##

* [Відкрита фінансова біржа – Вікіпедія](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Стандарт ISO для електронного обміну даними](https://en.wikipedia.org/wiki/ISO_20022)

