{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WSDL failo formatas – žiniatinklio paslaugų aprašo kalbos failas",
  "description": "Sužinokite, kas yra WSDL failas ir API, kurios gali kurti ir atidaryti WSDL failus.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-ltl"
}
},
  "lastmod": "2022-02-03"
}

## Kas yra WSDL failas?

WSDL failas yra žiniatinklio paslaugų aprašo kalbos failas, parašytas XML kalba, skirtas žiniatinklio paslaugoms apibūdinti. Jame yra informacija apie galutinius taškus arba sąsajas, skirtas prisijungti prie išorinio pasaulio visuotinai priimtu formatu. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (prižiūrima W3C.org) apibrėžia duomenų sklaidos kanalų, skirtų keistis duomenimis, paskelbimo sąlygas, kad būtų galima pasiekti nuotolinę taikomųjų programų prieigą per prievadus ir galinius taškus.

## WSDL failo formatas – daugiau informacijos

WSDL failai išsaugomi kaip XML failai, kuriuos galima skaityti žmonėms ir kuriuos galima atidaryti bet kuriame teksto rengyklėje, kad būtų galima peržiūrėti turinį.

## WSDL paslaugos aprašymas

WSDL 2.0 failo formato specifikacijose WSDL paslauga apibūdinama kaip susidedanti iš dviejų etapų:

- Abstraktus etapas
- Betoninė scena

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### Kokios technologijos gali būti naudojamos sąsajai su WSDL paslaugomis?

Sąsajai su WSDL paslaugomis, įskaitant ASP.NET, C/C++ ir Java programas, gali būti naudojamos kelios skirtingos technologijos.

## WSDL pavyzdys

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

Šiame pavyzdyje portType glossaryTerms apibrėžia vienpusę operaciją, vadinamą setTerm.

## Nuorodos

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [WSDL failo formato specifikacijos](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


