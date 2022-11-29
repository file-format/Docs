{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL File Format - Web Services Description Language File",
  "description":"Läs mer om vad som är en WSDL-fil och API:er som kan skapa och öppna WSDL-filer.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Vad är en WSDL fil?

En WSDL-fil är en Web Services Description Language-fil som är skriven på XML-språk för att beskriva webbtjänster. Den innehåller information om ändpunkter eller gränssnitt för anslutning till omvärlden i ett universellt accepterat format. [WSDL filformatspecifikationer](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (underhålls av W3C.org) definierar villkoren för publicering av dataflöden för utbyte av data för att ha fjärråtkomst till applikationer över portar och slutpunkter.

## WSDL-filformat - Mer information

WSDL-filer sparas som XML-filer som är läsbara för människor och kan öppnas i vilken textredigerare som helst för att se innehållet.

## WSDL Servicebeskrivning

WSDL 2.0-filformatspecifikationerna beskriver WSDL-tjänsten som består av två steg:

- Abstrakt scen
- Betongscen

Återanvändbarheten av beskrivningen och oberoende orodesigner styrs av en webbtjänst. Detta uppnås genom att använda flera olika typer av element, inklusive typer (definitioner av datatyp), meddelanden (data som kommuniceras), operationer (åtgärder) och protokoll som används av tjänsten. Dessa hanteras alla på abstrakt nivå. Bindningen av transport- och trådformatsdetaljer specificeras av bindningen, som grupperar ändpunkterna för att implementera ett gemensamt gränssnitt.

### Vilka tekniker kan användas för gränssnitt med WSDL-tjänster?

Flera olika teknologier kan användas för gränssnitt med WSDL-tjänster inklusive ASP.NET, C/C++ och Java-applikationer.

## WSDL-exempel

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

I det här exemplet definierar portTypen "glossaryTerms" en enkelriktad operation som kallas "setTerm".

## Referenser

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [WSDL filformatspecifikationer](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

