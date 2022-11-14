{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - Microsoft Outlook e-mailformaat",
  "description":"Meer informatie over MSG-bestandsindeling en API's die MSG-bestanden kunnen maken en openen.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een MSG-bestand?

MSG is een bestandsindeling die wordt gebruikt door [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) en Exchange om e-mailberichten op te slaan , contact, afspraak of andere taken. Dergelijke berichten kunnen een of meer e-mailvelden bevatten, met de afzender, ontvanger, onderwerp, datum en berichttekst, of contactgegevens, afspraakgegevens en een of meer taakspecificaties. De eigenschappen die het Message-object vormen, inclusief, maken ook deel uit van het MSG-bestand. MSG-bestand heeft headers, hoofdtekst van het bericht en hyperlinks als gewone ASCII-tekst. MSG-bestanden zijn ook geschikt voor de programma's die de Messaging Applications Programming Interface (MAPI) van Microsoft nodig hebben.

## MSG-bestandsstructuur

Het CFB_3-formaat is de basis van het MSG-bestand. Het paradigma is gebaseerd op de concepten voor opslag en streams, vrij dicht bij mappen en bestanden. Daarom is een groot verschil met de eerste de hele hiërarchie, verpakt in een afzonderlijk bestand, een samengesteld bestand genoemd. Objecten vormen de berichtbestanden en bestaan uit een enkele eigenschap of zijn verzamelingen. Dankzij deze mogelijkheid kunnen applicaties ingewikkelde, gestructureerde gegevens in één bestand opslaan. Dit formaat specificeert ook meerdere opslagplaatsen, elke opslag vertegenwoordigt het berichtobject als een belangrijk onderdeel. Deze storages bevatten een aantal streams die een eigenschap van die component vertegenwoordigen. Nesten van opslag is ook mogelijk.

## Mapi-eigenschappen

Op het hoogste niveau van het .msg-bestand bevatten opslagruimten streams waarin eigenschappen worden opgeslagen. Eigenschappen kunnen als volgt worden gecategoriseerd:

* Eigenschappen vaste lengte
* Variabele lengte eigenschappen
* Vastgoed met meerdere waarden

Ongeacht de categorie, een eigenschap is ofwel een tagged of benoemde. Er is echter geschikte toewijzingsinformatie vereist voor benoemde eigenschappen zoals gespecificeerd door hun toewijzingsopslag.

## Opslag

Storages vormen de belangrijkste componenten van het Message-object. MSG-bestandsindeling vermeldt de volgende opslagplaatsen:

## Structuur op het hoogste niveau

Berichtobject vertegenwoordigt het volledige hoogste niveau van het MSG-bestandsformaat. Afhankelijk van het type, de eigenschappen, het aantal ontvangers en bijlage-objecten, kan een berichtobject verschillende stroomopslagen hebben in het bijbehorende .MSG-bestand.

### Relatie met andere structuren

Het Msg-bestandsformaat heeft de volgende relaties met andere structuren:

* De basis van .msg is Samengesteld Bestand Binair Bestandsformaat.
* De eigenschappen die worden gebruikt door Message and Attachment Object Protocol worden gebruikt door dit formaat.

## Scenario's om MSG-indelingen te vermijden

Berichtobject kan worden gedeeld tussen clients of berichtenarchieven die het .msg-bestandssysteem gebruiken. Er zijn weinig omstandigheden waarin het opslaan van een berichtobject in het .msg-bestandsformaat niet geschikt zou zijn. Bijvoorbeeld:

* In het geval van een groot op zichzelf staand archief, is het beter om een full-featured formaat te gebruiken waarin weergaven nauwkeuriger kunnen worden weergegeven.
* Als de ontvanger onbekend is, is het mogelijk dat het formaat niet wordt ondersteund door de ontvanger en dat privé of irrelevant kan worden afgeleverd.

## MSG-bestandsvoorbeeld

Om een idee te krijgen van hoe een MSG-bestand eruitziet, kunt u een [voorbeeld MSG-bestand](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) downloaden en openen op uw computer om de inhoud ervan te bekijken.

## Referenties

* [[MS-OXMSG]: Outlook MSG-bestandsindeling](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

