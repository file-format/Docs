{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WSDL faila formāts — tīmekļa pakalpojumu apraksta valodas fails",
  "description": "Uzziniet, kas ir WSDL fails un API, kas var izveidot un atvērt WSDL failus.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-lvl"
}
},
  "lastmod": "2022-02-03"
}

## Kas ir WSDL fails?

WSDL fails ir tīmekļa pakalpojumu apraksta valodas fails, kas ir rakstīts XML valodā, lai aprakstītu tīmekļa pakalpojumus. Tā satur informāciju par galapunktiem vai saskarnēm savienojumam ar ārpasauli vispārpieņemtā formātā. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (uztur W3C.org) definē noteikumus datu plūsmu publicēšanai datu apmaiņai, lai nodrošinātu attālo lietojumprogrammu piekļuvi, izmantojot portus un galapunktus.

## WSDL faila formāts — vairāk informācijas

WSDL faili tiek saglabāti kā XML faili, kas ir lasāmi cilvēkiem un kurus var atvērt jebkurā teksta redaktorā, lai skatītu saturu.

## WSDL pakalpojuma apraksts

WSDL 2.0 faila formāta specifikācijas apraksta WSDL pakalpojumu kā divus posmus:

- Abstrakts posms
- Betona skatuve

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### Kādas tehnoloģijas var izmantot saskarnei ar WSDL pakalpojumiem?

Saskarsmei ar WSDL pakalpojumiem, tostarp ASP.NET, C/C++ un Java lietojumprogrammām, var izmantot vairākas dažādas tehnoloģijas.

## WSDL piemērs

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

Šajā piemērā portType glossaryTerms definē vienvirziena darbību, ko sauc par setTerm.

## Atsauces

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [WSDL faila formāta specifikācijas](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


