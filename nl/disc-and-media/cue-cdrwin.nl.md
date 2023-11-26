{
"date":"2023-10-18",
   "keywords":[
"keu",
"cue-bestand",
"cue cdrwin cue-bladbestand",
"hoe een cue-bestand openen",
"bestand",
"cue-bestandsextensie",
"verlenging",
"bestand"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title":"CUE-bestandsindeling - CDRWIN Cue Sheet",
   "description":"Leer meer over het CUE CDRWIN Cue Sheet-bestandsformaat en API's die CUE-bestanden kunnen maken en openen.",
"linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin",
"parent":" schijf-en-media"
}
},
"lastmod":"2023-10-18"
}

## Wat is een CUE-bestand?

Een **.CUE**-bestand, ook bekend als **CDRWIN Cue Sheet**, is een tekstbestand met informatie over de tracks en de lay-out van een audio-cd of schijfimage, meestal in BIN- of ISO-indeling. Deze bestanden worden vaak gebruikt om de structuur en inhoud van de schijf te beschrijven, waardoor cd-brandsoftware of virtuele schijfsoftware de originele schijf nauwkeurig kan reproduceren.

## Voorbeeld van CUE-bestand

Hier is een voorbeeld van hoe het ".cue"-bestand eruit zou kunnen zien:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN-cuesheet

CDRWIN Cue Sheet is een specifieke variant van het ".cue"-bestandsformaat dat wordt gebruikt door CDRWIN-software. CDRWIN is software voor het branden en schrijven van cd's/dvd's en de ".cue"-vellen zijn ontworpen voor gebruik met deze software. Deze ".cue"-vellen bevatten informatie die CDRWIN nodig heeft om nauwkeurig cd's of dvd's te maken of te branden.

Hier zijn enkele belangrijke details die specifiek zijn voor CDRWIN Cue Sheets:

1. **Uniek voor CDRWIN**: CDRWIN's ".cue"-vellen hebben een eigen formaat dat specifiek is voor CDRWIN-software. Hoewel ze overeenkomsten vertonen met standaard ".cue"-bestanden, zijn ze op maat gemaakt om te werken met de functies en instellingen van CDRWIN.
    






2. **Gebruiksvriendelijke interface**: CDRWIN biedt een eenvoudig te gebruiken interface voor het maken en bewerken van de ".cue"-bladen. Gebruikers kunnen op gebruiksvriendelijke wijze informatie over tracks, indexen, hiaten en andere parameters toevoegen of wijzigen.
    






3. **Compatibele schijftypen**: CDRWIN-cuesheets worden voornamelijk gebruikt voor het maken van verschillende soorten cd's en dvd's, waaronder dataschijven, audio-cd's, schijven met gemengde modus en meer. Met dit formaat kunnen gebruikers het type en de inhoud van de schijf die ze willen maken specificeren.
    






4. **Controle over schijfindeling**: CDRWIN Cue Sheets bieden gedetailleerde controle over de indeling en structuur van de schijf, inclusief trackvolgorde, pauze-/afstandsinstellingen en eventuele andere specifieke voorkeuren die de gebruiker heeft.
    






5. **ISO- en BIN-ondersteuning**: CDRWIN kan werken met zowel ISO- als BIN-schijfimageformaten. Het ".cue"-blad specificeert welk afbeeldingsbestand voor de schijf wordt gebruikt, waardoor een goede synchronisatie tussen cues en afbeelding wordt gegarandeerd.
    






6. **Branden en rippen**: deze ".cue"-vellen zijn cruciaal bij het branden van schijven of het rippen van nummers van schijven met CDRWIN. Ze helpen ervoor te zorgen dat het eindproduct overeenkomt met de beoogde lay-out en inhoud.
    






7. **Back-up en herstel**: CDRWIN-gebruikers maken vaak ".cue"-bladen wanneer ze back-ups maken van hun cd's of dvd's. Deze vellen kunnen later worden gebruikt om de inhoud van de schijf te herstellen, inclusief de tracklay-out en timing.

## Hoe open je een CUE-bestand?

CDRWIN Cue Sheets zijn specifiek ontworpen voor CDRWIN-software, dus ze zijn doorgaans bedoeld om te worden geopend en gebruikt binnen CDRWIN.

Programma's die CUE-bestanden openen of ernaar verwijzen

-CDRWIN
- Slimme projecten IsoBuster
- EZB-systemen UltraISO

## Andere CUE-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cue** gebruiken.

**Schijf en media**
- [CUE - Cue-bladbestand](/nl/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/nl/disc-and-media/cue-cdrwin/)

## Referenties
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)

