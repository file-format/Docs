{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Finansal Değişim Dosya Formatını Aç",
  "description":"OFX dosya formatı ve OFX dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## OFX dosyası nedir?

OFX (Açık Finansal Değişim) dosyası, yazılım programları ve finansal kurumlar arasında finansal bilgi alışverişi için kullanılan bir finansal dosya formatıdır. Şirket içi finansal muhasebe defter tutmaya yönelik yazılım çözümlerinin gelişmesiyle birlikte, bankanıza bağlanabilen ve bankalarla finansal verileri içe veya dışa aktarabilen yazılım programları geliştirilmiştir. Buna işlemler, hesap bilgileri ve fatura ödemeleri gibi finansal veriler dahildir. QuickBooks, Microsoft Money, Intuit ve Quicken gibi yazılım programları içe aktarılan verileri OFX dosyası olarak kaydeder.

OFX dosya formatı için İnternet medya türü application/x-ofx'tir.

## OFX Dosya Formatı

OFX dosyaları XML (Genişletilebilir İşaretleme Dili) dosya formatında kaydedilir ve verileri yapılandırmak için etiketleri kullanır. [XML](/tr/web/xml/) dosyaları insanlar tarafından okunabilir biçimde saklanır ve Notepad, Notepad++ veya Apple TextEdit gibi herhangi bir metin düzenleyicide açılabilir ve düzenlenebilir. OFX dosyalarının içinde saklanan veriler **SGML (Standart Genelleştirilmiş İşaretleme Dili)** standardını temel alır. OFX dosyalarında depolanan veriler genellikle şunları içerir:

* Bankalara ilişkin bilgiler
* Kredi ve Banka Kartı bilgileri
* Hesaplar ve yatırım bilgileri
* diğer mali işlemler

### OFX Dosya Formatı Örneği

Aşağıda örnek bir OFX dosyasının dahili veri yapısı ve örnek verileri verilmiştir.

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

Bu örnek OFX dosyası aşağıdaki bilgileri içerir:

* Banka adı, hesap numarası ve bakiye gibi banka hesap bilgileri
* Her işlemin tarihi, türü ve tutarını içeren işlemlerin listesi

Hesap işlemlerini ve harcamalarını takip etmek için tüm bu bilgiler kişisel finans yazılım programına aktarılabilir.

## Referanslar ##

* [Açık Finansal Borsa - Wikipedia'dan](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Elektronik Veri Değişimi için ISO Standardı](https://en.wikipedia.org/wiki/ISO_20022)

