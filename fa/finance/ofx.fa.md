{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OFX - فرمت فایل تبادل مالی باز کنید",
  "description":"درباره فرمت فایل OFX و API هایی که می توانند فایل های OFX را ایجاد و باز کنند، بیاموزید.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx-fa",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## فایل OFX چیست؟

فایل OFX (Open Financial Exchange) یک فرمت فایل مالی است که برای تبادل اطلاعات مالی بین برنامه های نرم افزاری و موسسات مالی استفاده می شود. با تکامل راه حل های نرم افزاری برای نگهداری دفاتر حسابداری مالی داخلی، برنامه های نرم افزاری ایجاد شده است که می تواند به بانک شما متصل شود و داده های مالی را با بانک ها وارد یا صادر کند. این شامل داده های مالی مانند تراکنش ها، اطلاعات حساب و پرداخت قبض می شود. برنامه های نرم افزاری مانند QuickBooks، Microsoft Money، Intuit و Quicken داده های وارد شده را به عنوان فایل OFX ذخیره می کنند.

نوع رسانه اینترنتی برای فرمت فایل OFX application/x-ofx است.

## فرمت فایل OFX

فایل‌های OFX در قالب فایل XML (Extensible Markup Language) ذخیره می‌شوند و از برچسب‌ها برای ساختار داده‌ها استفاده می‌کنند. فایل‌های [XML](/web/xml/) در قالب قابل خواندن توسط انسان ذخیره می‌شوند و می‌توانند در هر ویرایشگر متنی مانند Notepad، Notepad++ یا Apple TextEdit باز و ویرایش شوند. داده های ذخیره شده در فایل های OFX بر اساس استاندارد **SGML (Standard Generalized Markup Language)** است. داده های ذخیره شده در فایل های OFX معمولاً عبارتند از:

* اطلاعات مربوط به بانک ها

* اطلاعات کارت اعتباری و بدهی

* اطلاعات حساب ها و سرمایه گذاری ها

* هرگونه تراکنش مالی دیگر


### نمونه فرمت فایل OFX

در زیر ساختار داده داخلی و داده های نمونه یک نمونه فایل OFX آمده است.

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

این نمونه فایل OFX حاوی اطلاعات زیر است:

 * اطلاعات حساب بانکی مانند نام بانک، شماره حساب و موجودی
 * فهرست معاملات شامل تاریخ، نوع و مبلغ هر تراکنش

تمام این اطلاعات را می توان در یک برنامه نرم افزاری مالی شخصی برای پیگیری تراکنش ها و هزینه های حساب وارد کرد.

## منابع ##

* [Open Financial Exchange - By Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)

* [استاندارد ISO برای تبادل الکترونیکی داده] (https://en.wikipedia.org/wiki/ISO_20022)


