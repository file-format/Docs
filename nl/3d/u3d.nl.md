{
  "date" : "2019-10-11",
  "keywords" :[ "u3d-bestand", "u3d-bestandsindeling", "wat is een u3d-bestand", "bestand", "u3d-voorbeeld", "u3d-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Universeel 3D-bestandsformaat",
  "description":"Meer informatie over de U3D-bestandsindeling en API's die U3D-bestanden kunnen openen en maken.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een U3D-bestand?

**U3D** (Universal 3D) is een gecomprimeerde bestandsindeling en gegevensstructuur voor 3D-computergraphics. Het bevat 3D-modelinformatie zoals driehoeksmazen, belichting, schaduw, bewegingsgegevens, lijnen en punten met kleur en structuur. Het formaat werd in augustus 2005 geaccepteerd als [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm) standaard. 3D [PDF](/nl/pdf/)-documenten ondersteunen U3D objecten insluiten en kunnen worden bekeken in Adobe Reader (versie 7 en hoger).

U3D-formaat is ontwikkeld met het oog op het doel om een universele standaard voor driedimensionale gegevensopslag en -uitwisseling vast te stellen. Het formaat wordt echter vooral gebruikt in codering voor 3D PDF in plaats van te worden gebruikt als een uitwisselingsformaat. Acrobat 3D converteert een ondersteund 3D-bestandstype naar U3D of PRC bij conversie naar de PDF.

## U3D-bestandsindeling

U3D-bestanden hebben een binaire bestandsindeling die vier edities heeft ondergaan, zoals beschreven in het referentiedocument [ECMA-363](http://www.ecma-international.org/publications/standards/Ecma-363.htm), wat resulteerde in een update van de specificaties bij elke editie. De PDF-bestandsstandaard ISO-32000 accepteert U3D als toegestaan annotatie- en multimediatype.

De eerste editie van U3D was gericht op de belangrijkste representaties van 3D-grafische eigenschappen zoals geometrie, kleur, texturen, belichting, botten en op transformatie gebaseerde animatie. De tweede en derde editie corrigeerden enkele fouten in de eerste editie, waarbij de derde versie het meest gebruikte type in industriële software was. De vierde editie geeft definities voor primitieven van hogere orde (gekromde oppervlakken). [U3D-specificaties](http://www.ecma-international.org/publications/standards/Ecma-363.htm) zijn online beschikbaar voor gebruikersreferentie op de ECMA-website.

### Gegevenstypen in U3D-bestanden

Het binaire bestand bevat de volgende typen: U8, U16, U32, U64, I16, I32, F32, F64 en String.

* U8: een niet-ondertekend 8-bits geheel getal
* U16: een niet-ondertekend 16-bits geheel getal
* U32: een niet-ondertekend 32-bits geheel getal
* U64: een niet-ondertekend 64-bits geheel getal
* I16: een ondertekend 16-bits geheel getal
* F32: Een IEEE single-precision float.
* F64: Een IEEE dubbele precisie float.
* String: Strings in een U3D-bestand beginnen met een niet-ondertekend 16-bits geheel getal dat de totale lengte van de tekens in de string definieert. Strings worden altijd hoofdlettergevoelig verwerkt.

## U3D-bestandsstructuur

Een U3D-bestand bevat een reeks blokken. Er zijn 3 verschillende soorten blok in elk U3D-bestand.

* Bestandskoptekstblok
* Aangifteblok
* Vervolgblok

De loader bepaalt het einde van een blok als de gegevens in dat blok niet nodig zijn of als er geen decoder voor dat bloktype beschikbaar is.

{{< figure src="../u3d.png" alt="U3D-bestandsindeling" >}}

### Bestandskoptekstblok
Een bestandsheaderblok bevat bestandsinformatie die door de geladen persoon wordt gebruikt om te bepalen hoe het bestand moet worden gelezen.

### Aangifteblok

De aangifteblokken bevatten informatie over de objecten in het bestand. De objecten in een aangifteblok moeten gedefinieerd zijn.

### Vervolgblok

Aanvullende informatie voor objecten die in een aangifteblok zijn aangegeven, vindt u in het vervolgblok. Elk vervolgblok moet worden gekoppeld aan een declaratieblok.


## Referenties ##

* [U3D-bestandsindeling - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [ECMA U3D-bestandsformaatspecificaties](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

