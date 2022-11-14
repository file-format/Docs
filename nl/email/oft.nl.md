{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Microsoft Outlook e-mailsjabloonbestand",
  "description":"Meer informatie over OFT-bestandsindelingen en API's die OFT-bestanden kunnen maken en openen.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een OFT-bestand?

Bestanden met de extensie .oft zijn sjabloonbestanden die zijn gemaakt met Microsoft Outlook. De vooraf opgemaakte lay-out voor berichtsjablonen wordt vervolgens gebruikt voor het verzenden van e-mails met algemene informatie om tijd te besparen. Dergelijke bestanden kunnen worden gegenereerd door een nieuwe e-mail aan te maken, de nodige informatie toe te voegen en vervolgens de vervolgkeuzelijst Opslaan als Office-sjabloon (.oft) van Microsoft Outlook te gebruiken. Gebruikers kunnen de OFT-bestanden openen door erop te dubbelklikken en het wordt geopend in de bijbehorende toepassing op dat specifieke systeem.

## OFT-bestandsstructuur ##

Het .OFT-bestandsformaat gebruikt het [MSG](/nl/email/msg/) bestandsformaat als basis. Het enige verschil is dat OFT-bestanden CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) als opslagklasse (WriteClassStg) hebben, terwijl MSG-bestanden CLSID_MailMessage gebruiken ({00020D0B-0000-0000-C000-000000000046}).

Het CFB_3-formaat is de basis van het MSG-bestand. Het paradigma is gebaseerd op de concepten voor opslag en streams, vrij dicht bij mappen en bestanden. Daarom is een groot verschil met de eerste de hele hiërarchie, verpakt in een afzonderlijk bestand, een samengesteld bestand genoemd. Objecten vormen de berichtbestanden en bestaan uit een enkele eigenschap of zijn verzamelingen. Dankzij deze mogelijkheid kunnen applicaties ingewikkelde, gestructureerde gegevens in één bestand opslaan. Dit formaat specificeert ook meerdere opslagplaatsen, elke opslag vertegenwoordigt het berichtobject als een belangrijk onderdeel. Deze storages bevatten een aantal streams die een eigenschap van die component vertegenwoordigen. Nesten van opslag is ook mogelijk.

### OFT-eigenschappen

Op het hoogste niveau van het .msg-bestand bevatten opslagruimten streams waarin eigenschappen worden opgeslagen. Eigenschappen kunnen als volgt worden gecategoriseerd:

* Eigenschappen vaste lengte
* Variabele lengte eigenschappen
* Vastgoed met meerdere waarden

Ongeacht de categorie, een eigenschap is ofwel een tagged of benoemde. Er is echter geschikte toewijzingsinformatie vereist voor benoemde eigenschappen zoals gespecificeerd door hun toewijzingsopslag.

### OFT-opslag

Storages vormen de belangrijkste componenten van het Message-object. MSG-bestandsindeling vermeldt de volgende opslagplaatsen:

### Structuur op het hoogste niveau

Berichtobject vertegenwoordigt het volledige hoogste niveau van het Msg-bestandsformaat. Afhankelijk van het type, de eigenschappen, het aantal ontvangers en bijlage-objecten, kan een berichtobject verschillende stroomopslagen hebben in het bijbehorende .MSG-bestand.

#### Relatie met andere structuren

Het MSG/OFT-bestandsformaat heeft de volgende relaties met andere structuren:

* De basis van .msg is Samengesteld Bestand Binair Bestandsformaat.
* De eigenschappen die worden gebruikt door Message and Attachment Object Protocol worden gebruikt door dit formaat.

## Referenties

* [[MS-OXMSG]: Outlook MSG-bestandsindeling](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

