{
  "date" : "2021-01-21",
  "keywords" :[ "otp-bestand", "otp-bestandsindeling", "wat is een otp-bestand", "bestand", "otp-voorbeeld", "otp-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP - OpenDocument presentatiesjabloon",
  "description":"Meer informatie over OTP-bestandsindeling en API's die OTP-bestanden kunnen maken en openen.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Wat is een OTP-bestand?

Bestanden met de extensie .otp vertegenwoordigen presentatiesjabloonbestanden die zijn gemaakt door toepassingen in de standaardindeling OASIS OpenDocument. De inhoud van een dergelijk bestand bevat presentatie-informatie in de vorm van dia's met tekst, afbeeldingen, vormen, multimedia-inhoud, overgangseffecten en andere dia-elementen. Deze sjabloonbestanden worden gebruikt om snel nieuwe presentaties te maken op basis van de stijlinformatie die in de sjabloon zelf is opgeslagen. OTP-bestanden kunnen worden gemaakt en opgeslagen met verschillende toepassingen, zoals Impress dat wordt geleverd met OpenOffice-suite en Microsoft PowerPoint. Het OTP-bestandsformaat is vergelijkbaar met Microsoft PowerPoint-sjabloonbestanden [.pot](/nl/presentation/pot/) en [.potx](/nl/presentation/potx/).

## OTP-bestandsindeling

Het OTP-bestandsformaat is gebaseerd op de OpenDocument-standaard die documentrepresentatie als een enkel XML-document ondersteunt, evenals het verzamelen van verschillende subdocumenten in een enkel gecomprimeerd pakket in het [ZIP](/nl/compression/zip/)-formaat. De inhoud van het bestand wordt gedistribueerd in meerdere xml-bestanden die samen zijn verpakt. Deze meerdere [XML](/nl/web/xml/)-bestanden bevatten informatie over de stijl, inhoud, meta-informatie en instellingen van het document zoals hieronder vermeld.

* `content.xml` – Documentinhoud en automatische stijlen die in de inhoud worden gebruikt.
* `styles.xml` – Stijlen die worden gebruikt in de documentinhoud en automatische stijlen die in de stijlen zelf worden gebruikt.
* `meta.xml` – Document meta-informatie, zoals de auteur of het tijdstip van de laatste opslagactie.
* `settings.xml` – Toepassingsspecifieke instellingen, zoals de venstergrootte of printerinformatie.

## Referenties

* [OpenDocument - Door Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

