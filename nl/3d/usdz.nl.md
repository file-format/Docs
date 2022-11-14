{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz-bestand", "usdz-bestandsindeling", "bestandsindeling", "3d", "usdz-bestandsdownload"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - ZIP-indeling voor universele scènebeschrijving",
  "description":"Meer informatie over het USDZ-bestandsformaat en API's die USDZ-bestanden kunnen openen en maken.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Wat is een USDZ-bestand?

Een bestand met .usdz is een niet-gecomprimeerd en niet-versleuteld ZIP-archief voor de bestandsindeling [USD](/nl/3d/usd/) (Universal Scene Description) die bestanden van andere formaten (zoals texturen en animaties) bevat en proxy's bevat voor andere formaten (zoals texturen en animaties) die zijn ingesloten in het archief en voert ze rechtstreeks uit met de USD-runtime zonder dat ze hoeven uit te pakken. USDZ-bestanden zijn pakketten waarvan het ontwerp is gebaseerd op de nieuwe abstractie op Ar-niveau van een pakket. Usdz is geregistreerd bij IANA en heeft de mediatypenaam van het model en een subtypenaam vnd.usd+zip en de details ervan zijn te vinden op [IANA-registratiepagina](https://www.iana.org/assignments/media- types/model/vnd.usdz+zip).

## USDZ-bestandsindeling

USDZ-bestanden zijn gebaseerd op het ZIP-bestandsformaat dat individuele bestanden in de container archiveert. Hierdoor kan de ontvanger de inhoud gewoon uitpakken en de normale USD-scènebeschrijvingsbestanden gebruiken om mee te werken en te inspecteren. Bijna alle besturingssystemen bieden ingebouwde ondersteuning voor de ZIP-bestandsindelingen en het kiezen van dit archiveringsformaat boven elke aangepaste methode maakt het gemakkelijk voor USDZ-bestanden om nuttig te zijn als een eenvoudig transportprotocol.

### ZIP-beperkingen

Het USDZ-bestandsformaat gebruikt het ZIP-bestandsformaat zonder enige `compressie` en `codering`. Dit was bedoeld om te voldoen aan twee eisen:

* Voor een pakket dat al in het geheugen is geladen of als een enkel bestand op schijf, zijn de API's beschikbaar in USD voor toegang tot de gegevens in de afbeelding
* Het zou niet nodig moeten zijn om bestanden naar schijf te extraheren of meer heap-opslag toe te wijzen

Met USDZ wordt aan beide vereisten voldaan, aangezien de meeste afbeeldingsindelingen zelf interne compressieschema's toestaan, wat resulteert in een compacte bestandsgrootte.

### Lay-outvereisten

USDZ-pakketten vereisen dat de lay-out van bestanden binnen het pakket is dat de gegevens voor elk bestand moeten beginnen bij een veelvoud van 64 bytes vanaf het begin van het pakket. Het pakket moet echter beginnen met een native [USD](/nl/3d/usd/)-bestand in het geval dat het pakket wordt getarget met een eenvoudige verwijzing. In een dergelijk geval wordt dit eerste USD-bestand de standaardlaag genoemd. Klanten die "streambare inhoud" willen leveren, kunnen ook andere lay-outbeperkingen overwegen.

## USDZ-bestand downloaden
Omdat de usdz-bestanden vol zitten met andere afbeeldingen van hoge kwaliteit en usd-bestanden, kunnen ze meer schijfruimte in beslag nemen. Hier vindt u een eenvoudig en kleiner USDZ-voorbeeldbestand om te downloaden:

- [Voorbeeld.usdz](../voorbeeld.usdz)

## Referenties

* [specificaties voor USDZ-bestandsindeling](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)

