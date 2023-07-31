{
  "date" : "2019-10-11",
  "keywords" :[ "ixbrl","ixbrl-bestand", "ixbrl-bestandsformaat", "ixbrl-bestandstype", "bestand", "type", "wat is een ixbrl-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IXBRL - Bestandsformaat voor zakelijke en financiële rapportage",
  "description":"Meer informatie over IXBRL-bestandsindelingen en API's die IXBRL-bestanden kunnen maken en openen.",
  "linktitle" : "IXBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-ixbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Wat is een iXBRL-bestand?

Met de iXBRL-bestandsindeling (ilnine XBRL) kunnen [XBRL](/nl/finance/xbrl/)-gegevens worden ingesloten in een HTML-bestand om het zowel door machines als door mensen leesbaar te maken. Het is eigenlijk een [xHTML](/nl/web/xhtml/)-bestand dat de XBRL-tags gebruikt en is ontwikkeld door XBRL International om te voldoen aan de eisen van de Britse HMRC. Met iXBRL kunnen financiële overzichten worden gemaakt waarbij de lay-out van het originele document intact blijft. iXBRL-bestanden kunnen worden geopend in elke teksteditor, zoals Kladblok op het Windows-besturingssysteem en Teksteditor op MacOS.

## iXBRL-bestandsindeling

Binnen de iXBRL is de inhoud van XBRL verpakt in xHTML-bestandsindeling die XML-tags gebruikt. Zoals XBRL,<xbrl> is het root-element van iXBRL-bestanden. Het XHTML-formaat vertegenwoordigt de inhoud als een verzameling van verschillende documenttypen en modules. Alle bestanden in XHTML zijn gebaseerd op het XML-bestandsformaat en voldoen aan de XML-documentstandaarden. XHTML is het formaat dat essentieel is voor operationeel gebruik van het afhankelijke [HTML](/nl/web/html/) Document Object Model (DOM) of het [XML](/nl/web/xml/) Document Object Model. Voor de buitenwereld volgt iXBRL de [xHTML](/nl/web/xhtml/) bestandsformaatspecificaties.

### iXBRL versus XBRL

XBRL kan worden vergeleken met iXBRL op basis van de volgende factoren:

* Complexiteit
* Opmaakopties
* Bestandstypen/extensies
* Renderoptie
* Indieningsproces

De volgende tabel illustreert deze verschillen.

|Parameter|XBRL|iXBRL|
---|---|---|
|Complexiteit|Complexer dan iXBRL|Minder complex door het bestaande organisatieschema van XHTML|
|Opmaakopties|Beperkte flexibiliteit|Hoge flexibiliteit voor opmaak van inhoud|
|Bestandstypen/extensie|Formeel opgeslagen met de extensie .xml|Meestal opgeslagen als .html of .xhtml extensie|
|Renderingopties|XBRL-kijkers vereist om deze te bekijken|Menselijk leesbare inhoud die in browsers kan worden bekeken|
|Aangifteproces| XBRL (machineleesbaar) en HTML (mensleesbaar) instantiedocumenten moeten afzonderlijk worden ingediend.|Zowel door mensen leesbare als machineleesbare formaten zijn beschikbaar in een enkelvoudig document|

## Referenties

* [XBRL - Door Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [iXBRL](https://www.xbrl.org/the-standard/what/ixbrl/)

