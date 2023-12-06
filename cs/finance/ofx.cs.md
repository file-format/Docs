{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Open Financial Exchange File Format",
  "description":"Další informace o formátu souborů OFX a rozhraních API, která mohou vytvářet a otevírat soubory OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Co je soubor OFX?

Soubor OFX (Open Financial Exchange) je formát finančního souboru používaný pro výměnu finančních informací mezi softwarovými programy a finančními institucemi. S vývojem softwarových řešení pro vnitropodnikové vedení finančního účetnictví byly vyvinuty softwarové programy, které se mohou připojit k vaší bance a importovat nebo exportovat finanční data s bankami. To zahrnuje finanční údaje, jako jsou transakce, informace o účtu a platby faktur. Softwarové programy jako QuickBooks, Microsoft Money, Intuit a Quicken ukládají importovaná data jako soubor OFX.

Typ internetového média pro formát souboru OFX je application/x-ofx.

## Formát souboru OFX

Soubory OFX jsou uloženy ve formátu souboru XML (Extensible Markup Language) a ke strukturování dat používají značky. Soubory [XML](/cs/web/xml/) jsou uloženy ve formátu čitelném pro člověka a lze je otevřít a upravit v libovolném textovém editoru, jako je Notepad, Notepad++ nebo Apple TextEdit. Data uložená v souborech OFX jsou založena na standardu **SGML (Standard Generalized Markup Language)**. Data uložená v souborech OFX obvykle zahrnují:

* Informace týkající se bank
* Informace o kreditní a debetní kartě
* Informace o účtech a investicích
* jakékoli další finanční transakce

### Příklad formátu souboru OFX

Následuje vnitřní struktura dat a ukázková data ukázkového souboru OFX.

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

Tento vzorový soubor OFX obsahuje následující informace:

* Informace o bankovním účtu, jako je název banky, číslo účtu a zůstatek
* Seznam transakcí včetně data, typu a částky každé transakce

Všechny tyto informace lze importovat do softwarového programu pro osobní finance, abyste mohli sledovat transakce a výdaje na účtu.

## Reference ##

* [Otevřená finanční burza – podle Wikipedie](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO Standard pro elektronickou výměnu dat] (https://en.wikipedia.org/wiki/ISO_20022)

