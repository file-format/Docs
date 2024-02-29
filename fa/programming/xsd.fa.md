{
  "date": "2022-02-06",
  "keywords": [
"xsd",
"xsd",
"فایل xsd چیست",
"نحوه باز کردن فایل xsd",
"افزونه",
"فایل",
"فایل xsd",
"فرمت فایل xsd",
"پسوند xsd",
"نمونه فایل xsd"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": " با فرمت فایل XSD و API هایی که می توانند یک فایل XSD ایجاد و باز کنند آشنا شوید.",
  "title": "فرمت فایل XSD - فایل تعریف طرحواره XML",
  "linktitle": "XSD",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-xs-fad"
}
}،
  "lastmod": "2022-02-06"
}

## فایل XSD Schema چیست؟

یک فایل XSD یک فایل تعریف است که عناصر و ویژگی هایی را که می توانند بخشی از یک سند XML باشند را مشخص می کند. این تضمین می کند که داده ها به درستی تفسیر می شوند و خطاها کشف می شوند و در نتیجه اعتبار XML مناسب می شود. فایل های XSD اطمینان حاصل می کنند که داده های وارد شده از همان ساختار تعریف شده در فایل پیروی می کنند. فایل‌های XSD در قالب فایل [XML](/web/xml/) ذخیره می‌شوند و می‌توانند در هر ویرایشگر متنی مانند Microsoft Notepad، Notepad++ یا [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/) باز یا ویرایش شوند.

## فرمت فایل XSD

فایل‌های XSD روی دیسک در قالب فایل متنی ساده که قابل خواندن توسط انسان است ذخیره می‌شوند. یک XSD عناصری را که می‌توان در اسناد استفاده کرد، مرتبط با داده‌های واقعی که قرار است با آن کدگذاری شود، تعریف می‌کند.

## نمونه ای از فایل XSD

یک فایل XSD ساده که یک طرح سفارش خرید دارد، عناصر را با استفاده از برچسب‌ها همانطور که در [XSD example by Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022) زیر نشان داده شده است، تعریف می‌کند.

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

در اینجا از تگ های زیر استفاده می شود.

 * `xs:element` - یک عنصر را تعریف می کند.
 * `xs:sequence` - نشان می دهد که عناصر فرزند فقط به ترتیب ذکر شده ظاهر می شوند.
 * `xs:complexType` - نشان می دهد که حاوی عناصر دیگری است.
 * `xs:simpleType` - نشان می دهد که آنها حاوی عناصر دیگری نیستند.
 * نوع - رشته، اعشار، عدد صحیح، بولی، تاریخ، زمان،

## منابع ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [XSD Sample Example](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

