{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Stylesheet Language"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف XSLT" ,
  "description":"تعرف على تنسيق ملف XSLT وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XSLT وفتحها." ,
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-01-20"
}

## ما هو ملف XSLT؟

الملف بامتداد .xslt هو ملف تحويل لغة ورقة الأنماط الموسعة يُستخدم لتحويل ملف XML وتصميمه باستخدام إرشادات XSL. يستخدم التنسيق لتحويل مستندات XML إلى تنسيقات إخراج قياسية مثل مستند نصي أو صفحة ويب .html. يؤدي هذا التحويل إلى إنشاء مستند جديد بناءً على محتوى مستند XML الحالي. XSLT يجعله قادرًا نظريًا على الحسابات التعسفية.

## تنسيق ملف XSLT

يحتوي تنسيق ملف XLST على إرشادات التحويل بتنسيق نص عادي يمكن عرضها في أي محرر نصوص. كانت هناك ثلاث مراجعات للغة.

* "XSLT 1.0" - تم نشر XSLT 1.0 كتوصية W3C في نوفمبر 1999.
* "XSLT 2.0" - يتضمن تعديلات مثل معالجة السلسلة باستخدام التعبيرات العادية والوظائف والمشغلات لمعالجة التواريخ والأوقات والمدد ومستندات الإخراج المتعددة والتجميع ونظام كتابة أكثر ثراءً وفحصًا قويًا للنوع.
* "XSLT 3.0" - أصبح جزءًا من توصية W3C في 8 يونيو 2017 وتشمل الميزات الجديدة الرئيسية تحويل التدفق ، والحزم لتحسين نمطية أوراق الأنماط الكبيرة ، وتحسين معالجة الأخطاء الديناميكية باستخدام ، على سبيل المثال ، xsl: حاول التعليمات ، ودعم الخرائط والمصفوفات ، مما يمكّن XSLT من التعامل مع JSON وكذلك XML.

### مثال XSLT

المثال التالي مأخوذ من [w3schools] (https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## مراجع ##

* [XSLT - بواسطة Wikipedia] (https://en.wikipedia.org/wiki/XSLT)
* [عناصر XSLT] (https://en.wikipedia.org/wiki/XSLT_elements)

