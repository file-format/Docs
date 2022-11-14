{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "extensie", "bestand", "formaat", "web", "certificaat", "taal"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Certificaatbestandsformaat",
  "description":"Meer informatie over CER-bestandsindeling en API's die CER-bestanden kunnen maken en openen.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Wat is een CER-bestand? ##

Een bestand met de extensie .cer is verantwoordelijk voor het opslaan van wat informatie over het eigenaarscertificaat en de specifieke openbare sleutel. Dit bestandsformaat kan de privésleutels niet opslaan en heeft de capaciteit om slechts één certificaat op te slaan, namelijk x509. De specifiek beveiligde certificeringsinstanties zijn die welke behoren tot HTTPS, een vertrouwd en beveiligd protocol voor browsen
De CER is een certificaat van uw server. Het wordt meestal ontvangen door de certificeringsinstantie voor het domein. CER wordt meestal als hetzelfde beschouwd als [CRT](/nl/web/crt/), hoewel beide hetzelfde SSL-certificaat hebben, maar verschillende bestandsnaamextensies hebben.
Deze kunnen op besturingssystemen worden gebruikt door simpelweg een browser te openen en de beveiliging van de gebruikte browser of website te controleren.

## Korte geschiedenis ##

In 1995 werd Thawte de eerste certificeringsinstantie voor het oplossen van de kwestie van openbare SSL-certificaten (secured socket link) uit de VS. Daarna is er een reeks van dergelijke autoriteiten die werd opgericht van 1995 tot 2020.

## CER-bestandsindeling ##

Deze bestanden kunnen eenvoudig worden
* De PKC S#7 omvat Base64 ASCII-codering
* De bestandsextensies zijn p7b of p7cZ
* Voor binaire inhoud is het certificaat DER of pkcs12/pfx.
Er zijn veel soorten certificaatbestanden met enkele unieke specificaties:
* .pem, wanneer een organisatie onsOnthawteificate chaining dit formaat staat bekend om het maken van certificaten
* .arm, wanneer de methode voor het verkrijgen van een certificering door zelfondertekend wordt ondersteund, is vereist, het gespecificeerde formaat voor dit doel is .arm. Het wordt weergegeven in base-64 ASCII-codering.
* .der, Het bestaat uit binaire gegevens. Dit betekent dat het slechts voor één certificaat kan worden gebruikt
* .pfx (PKC512), Het bestaat uit een privésleutel die overeenkomt met een certificaat uitgegeven door CA of een zelfondertekend certificaat. Dit formaat staat bekend om de conversie van de ene SSL-implementatie naar de andere.


