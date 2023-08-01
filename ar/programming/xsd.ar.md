{
  "date" : "2022-02-06",
  "keywords" :["xsd" , ".xsd" , "ما هو ملف xsd" , "كيفية فتح ملف xsd" , "التمديد" , "الملف" , "ملف xsd" , "تنسيق ملف xsd" , "امتداد xsd" , "مثال ملف xsd"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "description" :"تعرف على تنسيق ملف XSD وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف XSD وفتحه." ,
  "title" :"تنسيق ملف XSD - ملف تعريف مخطط XML" ,
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2022-02-06"
}

## ما هو ملف مخطط XSD؟

ملف XSD هو ملف تعريف يحدد العناصر والسمات التي يمكن أن تكون جزءًا من مستند XML. هذا يضمن أن البيانات يتم تفسيرها بشكل صحيح ، ويتم اكتشاف الأخطاء ، مما يؤدي إلى التحقق من صحة XML بشكل مناسب. تضمن ملفات XSD أن البيانات المدخلة تتبع نفس البنية المحددة في الملف. يتم تخزين ملفات XSD بتنسيق ملف [XML](/ar/web/xml/) ويمكن فتحها أو تحريرها في أي محرر نصوص مثل Microsoft Notepad أو Notepad ++ أو [Microsoft XML Notepad](https://microsoft.github.io / XmlNotepad /).

## تنسيق ملف XSD

يتم تخزين ملفات XSD على قرص بتنسيق ملف نصي عادي يمكن للبشر قراءته. يحدد XSD العناصر التي يمكن استخدامها في المستندات ، فيما يتعلق بالبيانات الفعلية التي سيتم ترميزها بها.

## مثال على ملف XSD

يحدد ملف XSD البسيط الذي يحتوي على مخطط أمر شراء العناصر باستخدام العلامات كما هو موضح في [مثال XSD بواسطة Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

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

هنا ، يتم استخدام العلامات التالية.

* `xs: element` - يحدد عنصرًا.
* `xs: sequence` - تشير إلى ظهور العناصر الفرعية بالترتيب المذكور فقط.
* `xs: complexType` - تشير إلى أنه يحتوي على عناصر أخرى.
* `xs: simpleType` - تشير إلى أنها لا تحتوي على عناصر أخرى.
* `النوع` - سلسلة ، عشري ، عدد صحيح ، منطقي ، تاريخ ، وقت ،

## مراجع ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [مثال نموذج XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

