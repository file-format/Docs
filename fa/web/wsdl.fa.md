{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل WSDL - فایل زبان توضیحات خدمات وب",
  "description": "در مورد اینکه فایل WSDL چیست و APIهایی که می‌توانند فایل‌های WSDL را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-fal"
}
}،
  "lastmod": "2022-02-03"
}

## فایل WSDL چیست؟

فایل WSDL یک فایل Web Services Description Language است که به زبان XML برای توصیف خدمات وب نوشته شده است. این شامل اطلاعاتی در مورد نقاط پایانی یا واسط برای اتصال به دنیای خارج در قالب مورد قبول جهانی است. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (نگهداری شده توسط W3C.org) شرایط انتشار فیدهای داده را برای تبادل داده به منظور دسترسی از راه دور برنامه به پورت ها و نقاط پایانی تعریف می کند.

## فرمت فایل WSDL - اطلاعات بیشتر

فایل‌های WSDL به‌عنوان فایل‌های XML ذخیره می‌شوند که قابل خواندن توسط انسان هستند و می‌توانند در هر ویرایشگر متنی برای مشاهده محتویات باز شوند.

## توضیحات سرویس WSDL

مشخصات فرمت فایل WSDL 2.0 سرویس WSDL را شامل دو مرحله توصیف می کند:

- مرحله انتزاعی
- مرحله بتنی

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### چه فناوری هایی را می توان برای ارتباط با سرویس های WSDL استفاده کرد؟

چندین فناوری مختلف را می توان برای رابط با سرویس های WSDL از جمله ASP.NET، C/C++ و برنامه های جاوا استفاده کرد.

## مثال WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

در این مثال، portType glossaryTerms یک عملیات یک طرفه به نام setTerm را تعریف می کند.

## منابع

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [مشخصات فرمت فایل WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


