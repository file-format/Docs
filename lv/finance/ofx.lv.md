{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX — atvērts finanšu apmaiņas faila formāts",
  "description":"Uzziniet par OFX failu formātu un API, kas var izveidot un atvērt OFX failus.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-lv",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Kas ir OFX fails?

OFX (Open Financial Exchange) fails ir finanšu faila formāts, ko izmanto finanšu informācijas apmaiņai starp programmatūras programmām un finanšu iestādēm. Attīstoties programmatūras risinājumiem iekšējai finanšu grāmatvedības uzskaitei, ir izstrādātas programmatūras, kas var izveidot savienojumu ar jūsu banku un importēt vai eksportēt finanšu datus no bankām. Tas ietver finanšu datus, piemēram, darījumus, konta informāciju un rēķinu apmaksu. Programmatūras programmas, piemēram, QuickBooks, Microsoft Money, Intuit un Quicken, saglabā importētos datus kā OFX failu.

Interneta multivides veids OFX faila formātam ir application/x-ofx.

## OFX faila formāts

OFX faili tiek saglabāti XML (Extensible Markup Language) faila formātā un izmanto tagus, lai strukturētu datus. [XML](/web/xml/) faili tiek glabāti cilvēkiem lasāmā formātā, un tos var atvērt un rediģēt jebkurā teksta redaktorā, piemēram, Notepad, Notepad++ vai Apple TextEdit. OFX failos saglabātie dati ir balstīti uz **SGML (standarta vispārinātā iezīmēšanas valoda)** standartu. Dati, kas tiek glabāti OFX failos, parasti ietver:

* Informācija, kas saistīta ar bankām

* Kredītkaršu un debetkaršu informācija

* Informācija par kontiem un ieguldījumiem

* jebkuri citi finanšu darījumi


### OFX faila formāta piemērs

Tālāk ir sniegta OFX faila parauga iekšējā datu struktūra un datu paraugi.

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

Šajā OFX faila paraugā ir šāda informācija:

 * Bankas konta informācija, piemēram, bankas nosaukums, konta numurs un atlikums
 * Darījumu saraksts, tostarp katra darījuma datums, veids un summa

Visu šo informāciju var importēt personīgo finanšu programmatūrā, lai sekotu līdzi konta darījumiem un izdevumiem.

## Atsauces Nr.

* [Open Financial Exchange — Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [ISO standarts elektroniskajai datu apmaiņai](https://en.wikipedia.org/wiki/ISO_20022)


