{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL-bestandsindeling - Webservices Beschrijving Taalbestand",
  "description":"Meer informatie over wat een WSDL-bestand is en API's die WSDL-bestanden kunnen maken en openen.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Wat is een WSDL-bestand?

Een WSDL-bestand is een Web Services Description Language-bestand dat is geschreven in XML-taal voor het beschrijven van webservices. Het bevat informatie over de eindpunten of interfaces voor connectiviteit met de buitenwereld in een universeel geaccepteerd formaat. [WSDL bestandsformaatspecificaties](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (onderhouden door W3C.org) definiëren de voorwaarden voor het publiceren van datafeeds voor de uitwisseling van data om externe applicatietoegang via poorten en eindpunten.

## WSDL-bestandsindeling - Meer informatie

WSDL-bestanden worden opgeslagen als XML-bestanden die voor mensen leesbaar zijn en die in elke teksteditor kunnen worden geopend om de inhoud te bekijken.

## WSDL-servicebeschrijving

De specificaties van de WSDL 2.0-bestandsindeling beschrijven de WSDL-service als bestaande uit twee fasen:

- Abstracte fase
- Beton podium

De herbruikbaarheid van de beschrijving en onafhankelijke concernontwerpen wordt geregeld door een webservice. Dit wordt bereikt met behulp van verschillende soorten elementen, waaronder typen (definities van gegevenstypes), berichten (de gecommuniceerde gegevens), bewerkingen (acties) en protocollen die door de service worden gebruikt. Deze worden allemaal op abstract niveau beheerd. De binding van transport- en draadformaatdetails worden gespecificeerd door de binding, die de eindpunten groepeert om een gemeenschappelijke interface te implementeren.

### Welke technologieën kunnen worden gebruikt voor interfacing met WSDL-services?

Er kunnen verschillende technologieën worden gebruikt voor interfacing met WSDL-services, waaronder ASP.NET, C/C++ en Java-toepassingen.

## WSDL-voorbeeld

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

In dit voorbeeld definieert het portType "glossaryTerms" een eenrichtingsbewerking met de naam "setTerm".

## Referenties

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [specificaties voor WSDL-bestandsindeling](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

