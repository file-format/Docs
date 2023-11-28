{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - تنسيق ملف البورصة المالية المفتوحة",
  "description":"تعرف على تنسيق ملف OFX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات OFX وفتحها.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## ما هو ملف OFX؟

ملف OFX (التبادل المالي المفتوح) هو تنسيق ملف مالي يستخدم لتبادل المعلومات المالية بين البرامج والمؤسسات المالية. مع تطور الحلول البرمجية لحفظ دفاتر المحاسبة المالية الداخلية, تم تطوير برامج يمكنها الاتصال بالبنك الذي تتعامل معه واستيراد أو تصدير البيانات المالية مع البنوك. يتضمن ذلك البيانات المالية مثل المعاملات ومعلومات الحساب ودفع الفواتير. تقوم البرامج مثل QuickBooks وMicrosoft Money وIntuit وQuicken بحفظ البيانات المستوردة كملف OFX.

نوع وسائط الإنترنت لتنسيق ملف OFX هو application/x-ofx.

## تنسيق ملف أوفكس

يتم حفظ ملفات OFX بتنسيق ملف XML (لغة التوصيف القابلة للتوسيع) وتستخدم العلامات لتنظيم البيانات. يتم تخزين ملفات [XML](/ar/web/xml/) بتنسيق يمكن قراءته بواسطة الإنسان ويمكن فتحها وتحريرها في أي محرر نصوص مثل Notepad أو Notepad++ أو Apple TextEdit. تعتمد البيانات المخزنة داخل ملفات OFX على معيار **SGML (لغة التوصيف المعممة القياسية)**. تتضمن البيانات المخزنة داخل ملفات OFX عادةً ما يلي:

* المعلومات المتعلقة بالبنوك
* معلومات بطاقة الائتمان والخصم
* معلومات الحسابات والاستثمارات
* أية معاملات مالية أخرى

### مثال على تنسيق ملف OFX

فيما يلي بنية البيانات الداخلية ونموذج البيانات لملف OFX كمثال.

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

يحتوي هذا المثال لملف OFX على المعلومات التالية:

* معلومات الحساب البنكي مثل اسم البنك ورقم الحساب والرصيد
* قائمة المعاملات بما في ذلك تاريخ ونوع ومبلغ كل معاملة

يمكن استيراد كل هذه المعلومات في برنامج التمويل الشخصي لتتبع معاملات الحساب والنفقات.

## مراجع ##

* [البورصة المالية المفتوحة - بواسطة ويكيبيديا](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [معيار ISO لتبادل البيانات الإلكترونية](https://en.wikipedia.org/wiki/ISO_20022)

