{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - Açıq Maliyyə Mübadiləsi Fayl Formatı",
  "description":"OFX faylları yarada və aça bilən OFX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-az",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## OFX faylı nədir?

OFX (Açıq Maliyyə Mübadiləsi) faylı proqram proqramları və maliyyə institutları arasında maliyyə məlumatlarının mübadiləsi üçün istifadə edilən maliyyə fayl formatıdır. Daxili maliyyə uçotunun aparılması üçün proqram həllərinin təkamülü ilə bankınıza qoşula və banklarla maliyyə məlumatlarını idxal və ya ixrac edə bilən proqram proqramları hazırlanmışdır. Buraya əməliyyatlar, hesab məlumatları və faktura ödənişləri kimi maliyyə məlumatları daxildir. QuickBooks, Microsoft Money, Intuit və Quicken kimi proqram proqramları idxal olunan məlumatları OFX faylı kimi saxlayır.

OFX fayl formatı üçün İnternet media növü proqram/x-ofx-dir.

## OFX fayl formatı

OFX faylları XML (Extensible Markup Language) fayl formatında saxlanılır və məlumatları strukturlaşdırmaq üçün etiketlərdən istifadə edir. [XML](/web/xml/) faylları insanların oxuna biləcəyi formatda saxlanılır və Notepad, Notepad++ və ya Apple TextEdit kimi istənilən mətn redaktorunda açıla və redaktə edilə bilər. OFX faylları içərisində saxlanılan məlumatlar **SGML (Standard Generalized Markup Language)** standartına əsaslanır. OFX fayllarında saxlanılan məlumatlara adətən aşağıdakılar daxildir:

* Banklarla bağlı məlumatlar

* Kredit və debet kartı məlumatı

* Hesablar və investisiyalar haqqında məlumat

* hər hansı digər maliyyə əməliyyatları


### OFX fayl formatı nümunəsi

Aşağıda bir nümunə OFX faylının daxili məlumat strukturu və nümunə məlumatları verilmişdir.

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

Bu nümunə OFX faylı aşağıdakı məlumatları ehtiva edir:

 * Bank adı, hesab nömrəsi və balans kimi bank hesabı məlumatları
 * Hər bir əməliyyatın tarixi, növü və məbləği daxil olmaqla əməliyyatların siyahısı

Bütün bu məlumatlar hesab əməliyyatları və xərcləri izləmək üçün şəxsi maliyyə proqram proqramına idxal edilə bilər.

## İstinadlar ##

* [Açıq Maliyyə Birjası - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [Elektron Məlumat Mübadiləsi üçün ISO Standartı](https://en.wikipedia.org/wiki/ISO_20022)


