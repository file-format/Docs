{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "bestand", "extensie", "formaat", "wat is mod-bestandsformaat", "muziek", "mod-bestandsformaat", "mod vs MP3", "specificatie van het mod-bestandsformaat "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over MOD-bestandsindelingen en API's die MOD-bestanden kunnen maken, converteren en openen.",
  "title" :"MOD - Muziekmodulebestand",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Wat is een MOD-bestand?
Een bestand met de extensie .mod is een muziekmodulebestand gemaakt met behulp van het standaard muziekmoduleformaat, dat is gebaseerd op het **Amiga moduleformaat** ontwikkeld door Karsten Obarski en uitgebracht met de **Ultimate Soundtracker** software voor de Commodore Amiga-systeem. Net als een [MIDI](/nl/audio/mid/)-bestand, bestaat het uit nootpatronen en geluidssamples, die verschillende instrumenten vertegenwoordigen die volgens de noten worden afgespeeld. MOD-bestanden worden vooral gebruikt in videogames als achtergrondmuziek en in de **demoscene** computerkunstsubcultuur.

## MOD-bestandsindeling

De MOD is een computerbestandsindeling die wordt gebruikt als basisfunctie om muziek weer te geven, en het was de eerste modulebestandsindeling. MOD-bestanden gebruiken de .mod-bestandsextensie, behalve op de **Amiga** die de kop van een bestand leest om het bestandstype te bepalen, dus het is niet afhankelijk van bestandsnaamextensies. Een MOD-bestand bestaat uit een set van verschillende instrumenten in de vorm van samples, een aantal patronen die aangeven hoe en wanneer de samples moeten worden gespeeld, en een lijst met welke patronen in welke volgorde moeten worden afgespeeld.

### MOD-bestandsformaatspecificaties

Een MOD-bestandspatroon is eigenlijk ontworpen in een sequencer-gebruikersinterface als een tabel met één kolom per kanaal, dus deze tabel heeft vier kolommen (één voor elk Amiga-hardwarekanaal. Elke kolom heeft 64 rijen).

Een cel in de tabel kan ervoor zorgen dat een van de volgende acties plaatsvindt op het kanaal van de kolom wanneer de tijd van de rij is bereikt:

- Start een instrument met het spelen van een nieuwe noot in dit kanaal op een bepaald volume, mogelijk met een speciaal effect erop
- Wijzig het volume of het speciale effect dat op de huidige noot wordt toegepast
- Verander patroonstroom; spring naar een specifieke song of patroonpositie of loop in een patroon
- Niets doen; elke bestaande noot die in dit kanaal wordt gespeeld, blijft spelen

Een instrument is een enkele sample samen met een optionele specificatie van welk deel van de sample kan worden herhaald om een stevige toon vast te houden.

### Timing
Het minimale tijdsbestek was 0,02 seconden in het originele MOD-bestand, of een "vertical blanking" (VSync) -interval, omdat de originele software de VSync-timing gebruikte van de monitor die draaide op 50 Hz (voor PAL) of 60 Hz (voor NTSC) voor timing.

## Referenties

* [MOD (bestandsformaat) - Door Wikipedia](https://en.wikipedia.org/wiki/MOD_(bestandsformaat))

