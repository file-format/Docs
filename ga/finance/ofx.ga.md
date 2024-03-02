{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - Formáid Comhaid Malartaithe Airgeadais Oscailte",
  "description":"Foghlaim faoi fhormáid comhaid OFX agus APIs ar féidir leo comhaid OFX a chruthú agus a oscailt.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-ga",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Cad is comhad OFX ann?

Is formáid comhaid airgeadais é comhad OFX (Malartú Airgeadais Oscailte) a úsáidtear chun faisnéis airgeadais a mhalartú idir cláir bhogearraí agus institiúidí airgeadais. Le teacht chun cinn na réitigh bogearraí le haghaidh coimeád leabhar cuntasaíochta airgeadais intí, forbraíodh cláir bhogearraí ar féidir leo nascadh le do bhanc agus sonraí airgeadais a allmhairiú nó a onnmhairiú leis na bainc. Áirítear leis seo sonraí airgeadais amhail idirbhearta, faisnéis chuntais, agus íocaíochtaí billí. Sábhálann cláir bogearraí ar nós QuickBooks, Microsoft Money, Intuit, agus Quicken na sonraí allmhairithe mar chomhad OFX.

Is é an cineál meán Idirlín le haghaidh formáid comhaid OFX ná application/x-ofx.

## Formáid Comhaid OFX

Sábháltar comhaid OFX i bhformáid comhaid XML (Teanga Mharcála Leathnaithe) agus úsáidtear clibeanna chun na sonraí a struchtúrú. Stóráiltear [XML](/web/xml/) comhad i bhformáid inléite daonna agus is féidir iad a oscailt agus a chur in eagar in aon eagarthóir téacs ar nós Notepad, Notepad++, nó Apple TextEdit. Tá na sonraí atá stóráilte laistigh de na comhaid OFX bunaithe ar an gcaighdeán **SGML (Teanga Mharcála Ghinearálta Chaighdeánach)**. Áirítear go hiondúil ar shonraí a stóráiltear taobh istigh de chomhaid OFX:

* Faisnéis a bhaineann le bainc

* Faisnéis maidir le Cárta Creidmheasa agus Dochair

* Eolas cuntais agus infheistíochtaí

* aon idirbheart airgeadais eile


### Sampla Formáid Comhaid OFX

Seo a leanas an struchtúr inmheánach sonraí agus sonraí samplacha comhad OFX samplach.

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

Tá an fhaisnéis seo a leanas sa chomhad samplach OFX seo:

 * Faisnéis chuntas bainc ar nós ainm bainc, uimhir chuntais, agus iarmhéid
 * Liosta na n-idirbheart lena n-áirítear dáta, cineál, agus méid gach idirbhirt

Is féidir an fhaisnéis seo go léir a allmhairiú i gclár bogearraí airgeadais phearsanta chun cuntas a choinneáil ar idirbhearta agus caiteachais cuntais.

## Tagairtí ##

* [Malartú Airgeadais Oscailte - Le Vicipéid]( https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [Caighdeán ISO do Mhalartú Leictreonach Sonraí]( https://en.wikipedia.org/wiki/ISO_20022)


