{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid WSDL - Cur síos ar Sheirbhísí Gréasáin Comhad Teanga",
  "description": "Foghlaim faoi cad is comhad WSDL agus APIs ann ar féidir comhaid WSDL a chruthú agus a oscailt.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-gal"
}
},
  "lastmod": "2022-02-03"
}

## Cad is comhad WSDL ann?

Comhad Teanga Cur Síos ar Sheirbhísí Gréasáin is ea comhad WSDL atá scríofa i dteanga XML chun cur síos a dhéanamh ar sheirbhísí Gréasáin. Tá faisnéis ann faoi na críochphointí nó na comhéadain le haghaidh nascachta leis an domhan lasmuigh i bhformáid a nglactar leis go huilíoch. Sainmhíníonn [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (arna chothabháil ag W3C.org) na téarmaí le fothaí sonraí a fhoilsiú chun sonraí a mhalartú ionas go mbeidh rochtain chianfheidhmchláir ar phoirt agus ar chríochphointí.

## Formáid Chomhaid WSDL - Tuilleadh Eolais

Déantar comhaid WSDL a shábháil mar chomhaid XML atá inléite ag daoine agus is féidir iad a oscailt in aon eagarthóir téacs chun an t-ábhar a fheiceáil.

## Cur síos ar Sheirbhís WSDL

Déanann sonraíochtaí formáid comhaid WSDL 2.0 cur síos ar an tseirbhís WSDL mar dhá chéim:

- Céim teibí
- Céim coincréite

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### Cad iad na teicneolaíochtaí is féidir a úsáid chun comhéadan a dhéanamh le seirbhísí WSDL?

Is féidir roinnt teicneolaíochtaí éagsúla a úsáid chun comhéadan a dhéanamh le seirbhísí WSDL lena n-áirítear ASP.NET, C/C++, agus feidhmchláir Java.

## Sampla WSDL

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

Sa sampla seo, sainmhíníonn an cineál port GluaisTéarmaí oibríocht aontreo ar a dtugtar setTerm.

## Tagairtí

* [WSDL XML]( https://www.w3schools.com/xml/xml_wsdl.asp)

* [Sonraíochtaí formáid comhaid WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


