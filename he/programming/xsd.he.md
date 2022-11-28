{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd","מהו קובץ xsd","כיצד לפתוח קובץ xsd", "סיומת", "קובץ", "קובץ xsd","פורמט קובץ xsd", "סיומת .xsd", "דוגמה לקובץ xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ XSD וממשקי API שיכולים ליצור ולפתוח קובץ XSD.",
  "title" :"פורמט קובץ XSD - קובץ הגדרת סכמת XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## מהו קובץ XSD Schema?

קובץ XSD הוא קובץ הגדרה המציין את האלמנטים והתכונות שיכולים להיות חלק ממסמך XML. זה מבטיח שהנתונים מתפרשים כראוי, ושגיאות נתפסות, וכתוצאה מכך לאימות XML מתאים. קובצי XSD מבטיחים שהנתונים שהוזנו עוקבים אחר אותו מבנה כפי שהוגדר בקובץ. קובצי XSD מאוחסנים בפורמט קובץ [XML](/he/web/xml/) וניתן לפתוח או לערוך אותם בכל עורך טקסט כגון Microsoft Notepad, Notepad++ או [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## פורמט קובץ XSD

קובצי XSD מאוחסנים על דיסק בפורמט קובץ טקסט רגיל הניתן לקריאה אנושית. XSD מגדיר את האלמנטים שניתן להשתמש בהם במסמכים, המתייחסים לנתונים בפועל שאיתם יש לקודד אותו.

## דוגמה לקובץ XSD

קובץ XSD פשוט בעל סכימת הזמנת רכש מגדיר את האלמנטים באמצעות תגים כפי שמוצג ב [דוגמה XSD מאת Microsoft](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file) -simple-schema?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

כאן נעשה שימוש בתגים הבאים.

* `xs:element` - מגדיר אלמנט.
* `xs:sequence` - מציין אלמנטים צאצאים מופיעים רק בסדר המוזכר.
* `xs:complexType` - מציין שהוא מכיל אלמנטים אחרים.
* `xs:simpleType` - מציין שהם אינם מכילים אלמנטים אחרים.
* 'סוג' - מחרוזת, עשרוני, מספר שלם, בוליאני, תאריך, שעה,

## הפניות ##

- [פנקס XML של Microsoft](https://microsoft.github.io/XmlNotepad/)
- [דוגמה ל-XSD](https://docs.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

