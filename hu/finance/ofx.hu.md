{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Open Financial Exchange File Format",
  "description":"További információ az OFX fájlformátumról és az API-król, amelyek OFX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Mi az OFX fájl?

Az OFX (Open Financial Exchange) fájl egy pénzügyi fájlformátum, amelyet a szoftverprogramok és a pénzintézetek közötti pénzügyi információk cseréjére használnak. A házon belüli pénzügyi számviteli könyvvezetéshez szükséges szoftvermegoldások fejlődésével olyan szoftvereket fejlesztettek ki, amelyek képesek kapcsolódni az Ön bankjához, és pénzügyi adatokat importálni vagy exportálni a bankokkal. Ez magában foglalja a pénzügyi adatokat, például a tranzakciókat, a számlainformációkat és a számlafizetéseket. Az olyan szoftverek, mint a QuickBooks, a Microsoft Money, az Intuit és a Quicken, OFX fájlként mentik az importált adatokat.

Az OFX fájlformátum internetes médiatípusa: application/x-ofx.

## OFX fájlformátum

Az OFX fájlok XML (Extensible Markup Language) fájlformátumban kerülnek mentésre, és címkéket használnak az adatok strukturálására. Az [XML](/hu/web/xml/) fájlok ember által olvasható formátumban vannak tárolva, és bármely szövegszerkesztőben megnyithatók és szerkeszthetők, például a Notepad, Notepad++ vagy Apple TextEdit segítségével. Az OFX-fájlokban tárolt adatok az **SGML (Standard Generalized Markup Language)** szabványon alapulnak. Az OFX-fájlokban tárolt adatok általában a következőket tartalmazzák:

* Bankokkal kapcsolatos információk
* Hitel- és betéti kártya adatai
* Számlák és befektetési információk
* minden egyéb pénzügyi tranzakció

### OFX fájlformátum példa

Az alábbiakban egy példa OFX fájl belső adatstruktúrája és mintaadatai láthatók.

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

Ez a példa OFX fájl a következő információkat tartalmazza:

* Bankszámlaadatok, például banknév, számlaszám és egyenleg
* A tranzakciók listája, beleértve az egyes tranzakciók dátumát, típusát és összegét

Mindezek az információk importálhatók egy személyes pénzügyi szoftverbe a számlatranzakciók és -kiadások nyomon követése érdekében.

## Hivatkozások ##

* [Open Financial Exchange – Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [ISO szabvány az elektronikus adatcseréhez](https://en.wikipedia.org/wiki/ISO_20022)

