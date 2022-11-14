{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file WSDL - File del linguaggio di descrizione dei servizi Web",
  "description":"Scopri cos'è un file WSDL e le API che possono creare e aprire file WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Che cos'è un file WSDL?

Un file WSDL è un file del linguaggio di descrizione dei servizi Web scritto in linguaggio XML per la descrizione dei servizi Web. Contiene informazioni sugli endpoint o sulle interfacce per la connettività al mondo esterno in un formato universalmente accettato. [Specifiche del formato file WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (mantenuto da W3C.org) definisce i termini per la pubblicazione di feed di dati per lo scambio di dati al fine di avere accesso remoto alle applicazioni su porte ed endpoint.

## Formato file WSDL - Ulteriori informazioni

I file WSDL vengono salvati come file XML leggibili dall'uomo e possono essere aperti in qualsiasi editor di testo per visualizzare i contenuti.

## Descrizione del servizio WSDL

Le specifiche del formato file WSDL 2.0 descrivono il servizio WSDL come composto da due fasi:

- Fase astratta
- Palcoscenico in cemento

La riutilizzabilità della descrizione e dei progetti indipendenti è regolata da un servizio Web. Ciò si ottiene utilizzando diversi tipi di elementi, inclusi tipi (definizioni del tipo di dati), messaggi (i dati comunicati), operazioni (azioni) e protocolli utilizzati dal servizio. Questi sono tutti gestiti a livello astratto. L'associazione del trasporto e i dettagli del formato del cavo sono specificati dall'associazione, che raggruppa gli endpoint insieme per implementare un'interfaccia comune.

### Quali tecnologie possono essere utilizzate per interfacciarsi con i servizi WSDL?

È possibile utilizzare diverse tecnologie per l'interfacciamento con i servizi WSDL, tra cui ASP.NET, C/C++ e applicazioni Java.

## Esempio WSDL

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

In questo esempio, portType "glossaryTerms" definisce un'operazione unidirezionale denominata "setTerm".

## Riferimenti

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [Specifiche del formato file WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

