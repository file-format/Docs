{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "bestand", "extensie", "format", "wat is een cda-bestand", "muziek", "cda-bestandsformaat", "cda-bestandsformaatspecificatie"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over CDA-bestandsindelingen en API's die CDA-bestanden kunnen maken, converteren en openen.",
  "title" :"CDA - CD-audiotrack-snelkoppelingsbestand",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Wat is een CDA-bestand?

Een bestand met de extensie .cda is een klein stub-bestand dat door Microsoft Windows wordt gegenereerd voor elke audiotrack op een audio-cd. Deze bestanden bevatten typische informatie zoals tracktijden en een Windows-snelkoppeling waarmee gebruikers toegang hebben tot de specifieke audiotracks. De CDA-bestanden zijn geen muziek, maar ze verwijzen naar een muziekbestand dat ergens op de opslag staat. We kunnen het zeggen als een snelkoppeling van een audiobestand dat zich op een cd bevindt.

## CDA-bestandsindeling

Het CDA-bestandsformaat wordt gebruikt om een computer te vertellen welk audiobestand op een cd moet worden afgespeeld. Dus de CDA-bestanden worden nutteloos als ze worden gescheiden van een CD die ze vertegenwoordigen. De CDA-bestanden worden algemeen beschouwd als RIFF-bronnen. Er is slechts één blok met de naam "CDDA" en bevat slechts één gegevensblok met de naam "FMT" in de huidige versie van het .cda-bestand. Dit blok is 24 bytes lang. De identifier die door Windows is gemaakt, wordt gebruikt door de Windows 95 en Windows 98 gerelateerde cd-drive en de speler kan geen verbinding maken met FreeDB of CDDB. Zodat het de titel van het nummer en de naam van de artiest kan weergeven, die u handmatig moet invoeren in het bestand cdplayer.ini.

### Organisatie van een CDA-bestand

De volgende tabel toont de informatie over typische offsets:
| offset | lengte | inhoud |
---|---|---|
| 0x00 | 4 | de 4 ASCII-tekens "RIFF" |
| 0x04 | 4 | de grootte van de volgende chunk: altijd 36 (44 - 8), op 4 bytes (Intel-volgorde) |
| 0x08 | 4 | chunk-ID: de 4 ASCII-tekens "CDDA" |
| 0x0C | 4 | de 3 ASCII-tekens "fmt" gevolgd door een spatie |
| 0x10 | 4 | lengte van de chunk: altijd 24, op 4 bytes (Intel-volgorde) |
| 0x14 | 2 | versie van het cd-formaat, op 2 bytes (Intel-volgorde). In mei 2006, altijd gelijk aan 1. |
| 0x016 | 2 | nummer van het bereik, op 2 bytes (Intel-bestelling). Het eerste nummer heeft het nummer 1. |
| 0x18 | 4 | identifier berekend door Windows voor cdplayer.exe. |
| 0x1c | 4 | range offset, in aantal frames (Intel order) |
| 0x20 | 4 | duur van de track, totaal aantal frames (Intel order) |
| 0x24 | 1 | bereik positie: frames |
| 0x25 | 1 | bereik positie: seconden |
| 0x26 | 1 | bereik positie: minuten |
| 0x27 | 1 | een null-byte (binaire waarde 0) |
| 0x28 | 1 | duur van de track: frames |
| 0x29 | 1 | duur van de track: seconden |
| 0x2a | 1 | duur van het nummer: minuten |
| 0x2b | 1 | een null-byte (binaire waarde 0) |

## Referenties

* [.cda-bestand - Door Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

