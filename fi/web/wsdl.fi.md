{
  "date": "2022-02-03",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WSDL-tiedostomuoto - Web Services -kuvauskielitiedosto",
  "description": "Opi, mikä on WSDL-tiedosto ja API:t, jotka voivat luoda ja avata WSDL-tiedostoja.",
  "linktitle": "WSDL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-wsd-fil"
}
},
  "lastmod": "2022-02-03"
}

## Mikä on WSDL-tiedosto?

WSDL-tiedosto on Web Services Description Language -tiedosto, joka on kirjoitettu XML-kielellä verkkopalvelujen kuvaamista varten. Se sisältää tietoja päätepisteistä tai liitännöistä ulkomaailmaan kytkeytymistä varten yleisesti hyväksytyssä muodossa. [WSDL file format specifications](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (ylläpitää W3C.org) määrittelee ehdot datasyötteiden julkaisemiselle tietojen vaihtoa varten, jotta sovelluksella on etäkäyttö porttien ja päätepisteiden kautta.

## WSDL-tiedostomuoto - lisätietoja

WSDL-tiedostot tallennetaan XML-tiedostoina, jotka ovat ihmisen luettavissa ja jotka voidaan avata missä tahansa tekstieditorissa sisällön tarkastelua varten.

## WSDL-palvelun kuvaus

WSDL 2.0 -tiedostomuotomääritykset kuvaavat WSDL-palvelun muodostuvan kahdesta vaiheesta:

- Abstrakti vaihe
- Betonilava

The reusability of the description and independent concern designs is governed by a Web service. This is achieved using several different type of elements including types (data type definitions), messages (the data communicated), operations (actions), and protocols used by the service. These are all managed at abstract level. The binding of transport and wire format details are specified by the binding, that groups the endpoints together to implement a common interface.

### Mitä teknologioita voidaan käyttää WSDL-palvelujen liittämiseen?

Useita eri tekniikoita voidaan käyttää liitäntään WSDL-palveluihin, mukaan lukien ASP.NET-, C/C++- ja Java-sovellukset.

## WSDL esimerkki

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

Tässä esimerkissä porttityyppi glossaryTerms määrittää yksisuuntaisen toiminnon nimeltä setTerm.

## Viitteet

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)

* [WSDL-tiedostomuodon tiedot](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)


