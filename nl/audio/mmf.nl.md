{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "bestand", "extensie", "formaat", "audio", "smaf", "mmf-extensie", "mmf-bestanden", "mobiel muziekbestand", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MMF-bestandsindelingen en API's die MMF-bestanden kunnen maken en openen.",
  "title" :"MMF - Bestandsformaat voor mobiele muziek",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Wat is een MMF-bestand?

MMF is een bestandsextensie die is gekoppeld aan een SMAF-bestand. De MMF staat voor Mobile Music File, terwijl de SMAF staat voor Synthetic-Music Mobile Application Format. De MMF-bestanden in een smartphone bevatten systeembeltonen, geluid en kunnen ook afbeeldingen en tekstweergave bevatten. De MMF bevat verder drie soorten instrumentparameters, waaronder FM, PCM en Stream PCM. Deze bestandsindelingen zijn compatibel met het Windows-systeemplatform. De MMF-bestanden zijn gecategoriseerd als gegevensbestanden. Meestal ondersteunt Microsoft Mail MMF-bestanden. Het bestand met het MMF-achtervoegsel kan naar elk mobiel apparaat of systeemplatform worden gekopieerd.

Bovendien zijn deze bestanden veel kleiner in vergelijking met bestanden in standaard MIDI-formaat. [WAV](/nl/audio/wav/)- en [MID](/nl/audio/mid/)-bestanden kunnen worden geconverteerd naar MMF-indeling die vervolgens kan worden gedeeld en gedistribueerd als audio-inhoud. Deze bestanden kunnen via e-mail rechtstreeks op telefoons en pc worden ontvangen.


## Korte geschiedenis van MMF-bestandsindeling

Yamaha heeft SMAF-tools ontwikkeld als geluidsbestanden, zodat smartphones een groter aantal unieke beltonen kunnen opslaan. Yamaha introduceerde SMAF met de productie van hun MA-1, MA-2, MA-3, MA-5 en MA-7 LSI-geluidschips. Al deze formaten werden begin 2000 behoorlijk vertrouwd onder mobiele telefoons op de Oost-Aziatische markt.

Op internationaal niveau werd het MMF-formaat geautoriseerd door Samsung. Met behulp van het MMF-formaat kon Samsung een breed scala aan polyfone beltonen ontwerpen voor gebruik in Samsung-smartphones.

Yamaha wilde het formaat nog populairder maken en daarom publiceerde het op de officiële Yamaha SMAF-bestanden meer tools die compatibel zijn met dit formaat. Hiermee kunnen gebruikers nu eenvoudig MMF-bestanden op hun computers afspelen.


## Specificaties MMF-bestandsindeling ##

MMF-bestanden zijn onderverdeeld in gegevenssecties. Een vooraf ingestelde structuur rond een 8-byte wordt gebruikt om elk segment te beschrijven.
Het 4-byte label omvat CNTI, OPDA, MSTR, MTR en ATR. Gegevensgrootte plus 8 bytes is de chunkgrootte; de hele bestandsgrootte wordt berekend door alle chunkgroottes bij elkaar op te tellen. Als een bestand niet is beschadigd, moet de opgetelde bestandsgrootte gelijk zijn aan de grootte van de primaire header.

### Koptekst ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Hier is een voorbeeld van een MMF-bestand:

![](../mmf.png)

## Referenties

* [MMF - Door Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

