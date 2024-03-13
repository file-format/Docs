{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WSDL Fayl Format - Veb Xidmətlərinin Təsviri Dil Faylı",
  "description": "WSDL faylı və WSDL faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-azl"
}
},
  "lastmod": "2022-02-03"
}

## WSDL faylı nədir?

WSDL faylı Veb xidmətlərini təsvir etmək üçün XML dilində yazılmış Veb Xidmətlərinin Təsviri Dil faylıdır. Bu, hamı tərəfindən qəbul edilmiş formatda xarici dünyaya qoşulma üçün son nöqtələr və ya interfeyslər haqqında məlumatları ehtiva edir. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (W3C.org tərəfindən saxlanılır) portlar və son nöqtələr üzərindən proqrama uzaqdan giriş əldə etmək üçün məlumat mübadiləsi üçün məlumat lentlərinin dərc edilməsi şərtlərini müəyyən edir.

## WSDL Fayl Format - Ətraflı Məlumat

WSDL faylları insanlar tərəfindən oxuna bilən və məzmuna baxmaq üçün istənilən mətn redaktorunda açıla bilən XML faylları kimi saxlanılır.

## WSDL Xidmətinin Təsviri

WSDL 2.0 fayl formatının spesifikasiyası WSDL xidmətini iki mərhələdən ibarət olaraq təsvir edir:

- Abstrakt mərhələ
- Beton mərhələ

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### WSDL xidmətləri ilə əlaqə qurmaq üçün hansı texnologiyalardan istifadə edilə bilər?

ASP.NET, C/C++ və Java proqramları da daxil olmaqla WSDL xidmətləri ilə əlaqə yaratmaq üçün bir neçə fərqli texnologiyadan istifadə edilə bilər.

## WSDL nümunəsi

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

Bu nümunədə portType glossaryTerms setTerm adlı birtərəfli əməliyyatı müəyyən edir.

## İstinadlar

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [WSDL fayl formatının spesifikasiyası](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


