{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WSDL-filformat - Webtjenester Beskrivelse Sprogfil",
  "description": "Lær om, hvad en WSDL-fil og API'er er, der kan oprette og åbne WSDL-filer.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-dal"
}
},
  "lastmod": "2022-02-03"
}

## Hvad er en WSDL fil?

En WSDL-fil er en Web Services Description Language-fil, der er skrevet i XML-sprog til at beskrive webtjenester. Den indeholder information om endepunkter eller grænseflader for tilslutning til omverdenen i et universelt accepteret format. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (vedligeholdt af W3C.org) definerer vilkårene for udgivelse af datafeeds til udveksling af data for at få fjernadgang til applikationer via porte og slutpunkter.

## WSDL-filformat - flere oplysninger

WSDL-filer gemmes som XML-filer, der kan læses af mennesker og kan åbnes i en hvilken som helst teksteditor for at se indholdet.

## WSDL Servicebeskrivelse

WSDL 2.0-filformatspecifikationerne beskriver WSDL-tjenesten som bestående af to trin:

- Abstrakt scene
- Beton scene

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### Hvilke teknologier kan bruges til grænseflader med WSDL-tjenester?

Flere forskellige teknologier kan bruges til grænseflader med WSDL-tjenester, herunder ASP.NET, C/C++ og Java-applikationer.

## WSDL eksempel

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

I dette eksempel definerer portTypen glossaryTerms en envejsoperation kaldet setTerm.

## Referencer

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [WSDL filformatspecifikationer](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


