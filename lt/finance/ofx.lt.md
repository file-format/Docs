{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX – atviras finansų mainų failo formatas",
  "description":"Sužinokite apie OFX failo formatą ir API, kurios gali kurti ir atidaryti OFX failus.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-lt",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Kas yra OFX failas?

OFX (Open Financial Exchange) failas yra finansinio failo formatas, naudojamas finansinei informacijai keistis tarp programinės įrangos programų ir finansų įstaigų. Tobulėjant programinės įrangos sprendimams, skirtiems vidiniam finansinės apskaitos tvarkymui, buvo sukurtos programinės įrangos programos, galinčios prisijungti prie jūsų banko ir importuoti arba eksportuoti finansinius duomenis iš bankų. Tai apima finansinius duomenis, tokius kaip operacijos, sąskaitos informacija ir sąskaitų apmokėjimas. Programinės įrangos programos, tokios kaip QuickBooks, Microsoft Money, Intuit ir Quicken, išsaugo importuotus duomenis kaip OFX failą.

OFX failo formato interneto medijos tipas yra application/x-ofx.

## OFX failo formatas

OFX failai išsaugomi XML (Extensible Markup Language) failo formatu ir naudoja žymas duomenims struktūrizuoti. [XML](/web/xml/) failai saugomi žmonėms suprantamu formatu ir gali būti atidaromi bei redaguojami naudojant bet kurią teksto rengyklę, pvz., Notepad, Notepad++ arba Apple TextEdit. OFX failuose saugomi duomenys yra pagrįsti **SGML (standartinė apibendrinta žymėjimo kalba)** standartu. OFX failuose saugomi duomenys paprastai apima:

* Informacija susijusi su bankais

* Kredito ir debeto kortelių informacija

* Informacija apie sąskaitas ir investicijas

* bet kokios kitos finansinės operacijos


### OFX failo formato pavyzdys

Toliau pateikiama vidinė duomenų struktūra ir pavyzdiniai OFX failo duomenys.

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

Šiame OFX failo pavyzdyje yra ši informacija:

 * Banko sąskaitos informacija, pvz., banko pavadinimas, sąskaitos numeris ir likutis
 * Operacijų sąrašas, įskaitant kiekvienos operacijos datą, tipą ir sumą

Visą šią informaciją galima importuoti į asmeninių finansų programinę įrangą, kad būtų galima stebėti sąskaitos operacijas ir išlaidas.

## Nuorodos Nr.

* [Open Financial Exchange – Vikipedija](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [ISO standartas elektroniniam duomenų mainams](https://en.wikipedia.org/wiki/ISO_20022)


