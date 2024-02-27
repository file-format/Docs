{
  "date": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg fil",
"hvad er en mpeg-fil",
"hvordan man åbner mpeg-fil",
"fil",
"mpeg filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "MPEG-filformat - MPEG-video",
  "description": "Lær om MPEG-format og API'er, der kan oprette og åbne MPEG-filer.",
  "linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg-da",
      "parent": "video"
}
},
  "lastmod": "2023-07-12"
}

## Hvad er en MPEG-fil?

En MPEG-fil, også kendt som en MPEG-videofil, er et digitalt videofilformat, der bruger MPEG-standarderne (Moving Picture Experts Group) til videokomprimering. MPEG er et meget brugt format til lagring og transmission af videodata.

MPEG-formatet anvender komprimering med tab, hvilket betyder, at nogle oplysninger kasseres for at reducere filstørrelsen. Denne komprimeringsteknik giver mulighed for effektiv lagring og streaming af videoindhold, samtidig med at en rimelig videokvalitet opretholdes. Der er flere versioner af MPEG-standarden, herunder MPEG-1, MPEG-2, MPEG-4 og MPEG-7, hver med forskellige niveauer af komprimering og kvalitet.

MPEG-filer har typisk filtypenavnet .mpeg eller .mpg. De kan indeholde både video- og lyddata, ofte kombineret til en enkelt fil. MPEG-filer er kompatible med en lang række medieafspillere og videoredigeringssoftware, hvilket gør dem til et populært valg til deling og distribution af videoindhold.

## Hvordan åbner jeg en MPEG fil?

Der er adskillige softwareprogrammer tilgængelige, der kan åbne og afspille MPEG-filer. Her er nogle populære muligheder:

- VLC Media Player
- Windows Media Player
- QuickTime Player
- MPC-HC
- GOM-spiller
- MPlayer
- PotPlayer
- Kodi

## Hvordan konverterer man en MPEG-fil?

Der er en række videoapplikationer, herunder VideoLAN VLC medieafspiller, HandBrake og Apple QuickTime Player, som kan konvertere MPEG-filer til andre formater. For eksempel kan VLC konvertere MPEG-filer til disse formater

- MP4
- AVI
- MKV
- MOV
- WMV
- FLV

## Oversigt over intern struktur af MPEG-filer

Den interne struktur af MPEG-filer består af forskellige komponenter og datastrukturer, der organiserer og gemmer video, lyd og anden relateret information. Her er en oversigt over nøgleelementerne i den interne struktur af MPEG-filer:

- **Systemlag:**

Systemlaget definerer MPEG-filens overordnede struktur. Det inkluderer overskrifter, programstrømme og andre systemrelaterede data, der er nødvendige for afkodning og afspilning. Systemlaget er ansvarlig for styring af synkronisering og multipleksing af elementære streams.

- **Elementære strømme:**

MPEG-filer indeholder separate elementære streams til video, lyd og andre datatyper. Hver elementær strøm bærer komprimerede data, der er specifikke for dens type. For eksempel indeholder den elementære videostrøm komprimerede videorammer, og den elementære lydstrøm indeholder komprimerede lydeksempler.

- **Videokomprimering:**

MPEG-videokomprimeringsteknikker, såsom intra-frame og inter-frame-komprimering, bruges til at reducere filstørrelsen og samtidig bevare videokvaliteten. De komprimerede videorammer er organiseret i grupper af billeder (GOP'er), som består af intrakodede (I), forudsagte (P) og tovejs (B) rammer.

- **Lydkomprimering:**

MPEG-filer understøtter forskellige lydkomprimeringscodecs, såsom MP3, AAC eller MPEG-1 Audio Layer II. Lydeksemplerne komprimeres ved hjælp af disse codecs, hvilket muliggør effektiv lagring og transmission af lyddata.

- **Synkronisering og timing:**

MPEG-filer bruger tidsstempler og synkroniseringsoplysninger for at sikre korrekt justering mellem video- og lydstreams under afspilning. Disse tidsstempler hjælper med at opretholde synkronisering og giver nøjagtig timing til afkodning og gengivelse af lyd- og videorammer.

- **Metadata:**

MPEG-filer kan indeholde metadata, der giver yderligere oplysninger om video- og lydindholdet. Disse metadata kan omfatte detaljer såsom titel, forfatter, oprettelsesdato og andre beskrivende oplysninger.

- **Pakker og pakkeoverskrifter:**

MPEG-filer organiserer data i pakker. Hver pakke indeholder en pakkeheader, der giver information om pakkens indhold, såsom strømtype, pakkestørrelse og tidsinformation.

- **Programspecifikke oplysninger (PSI):**

PSI er en sektion i MPEG-filer, der indeholder yderligere oplysninger om programstrømmene, såsom program- og stream-identifikatorer, strømtype og beskrivelser. PSI hjælper med at afkode og demultiplekse de elementære strømme i filen.

- **Transportstrøm:**

I MPEG-2 er der et specifikt transportstream-format, der bruges til udsendelse og transmission af videoindhold. Transportstrømmen multiplekser flere programmer til en enkelt strøm, hvilket muliggør effektiv transmission og synkronisering af lyd, video og andre data over netværk.

## MPEG-filformat - flere oplysninger

Her er nogle vigtige ting at vide om MPEG-filformatet:

- **Kompression:**

MPEG-filer bruger tabsgivende komprimeringsteknikker til at reducere filstørrelsen og samtidig opretholde en rimelig videokvalitet. Mængden af komprimering kan variere afhængigt af MPEG-versionen og de anvendte indstillinger.

- **Video og lyd:**

MPEG-filer kan indeholde både video- og lyddata. Videodataene komprimeres ved hjælp af MPEG-standarder, mens lyden kan komprimeres ved hjælp af forskellige audio-codecs såsom MP3 eller AAC.

- **MPEG-versioner:**

   There are different versions of the MPEG standard, including MPEG-1, MPEG-2, MPEG-4, and MPEG-7. Each version has its own specifications, capabilities, and levels of compression. MPEG-1 is commonly used for VCDs (Video CDs), while MPEG-2 is used for DVDs and broadcast television. MPEG-4 is widely used for online video streaming, and MPEG-7 focuses on multimedia content description and metadata.

- **Filudvidelser:**

MPEG-filer har typisk filtypenavnet .mpeg eller .mpg. Der kan dog eksistere forskellige variationer og udvidelser, såsom .mp4 for MPEG-4-filer eller .mp3 for MPEG-1 Audio Layer 3-filer.

- **Kompatibilitet på tværs af platforme:**

MPEG-filer er bredt understøttet af forskellige medieafspillere, operativsystemer og enheder. De kan afspilles på Windows-, Mac- og Linux-systemer såvel som på smartphones, tablets og smart-tv'er.

- **Redigering:**

MPEG-filer kan redigeres ved hjælp af videoredigeringssoftware. Men da MPEG bruger komprimering med tab, kan gentagen redigering og omkodning af filen resultere i en forringelse af kvaliteten. Det anbefales ofte at arbejde med tabsfrie formater eller lave sikkerhedskopier før omfattende redigering.

- **Streaming:**

MPEG-filer bruges almindeligvis til at streame videoindhold over internettet. Især MPEG-4 er populær til online videoplatforme og videodelingswebsteder på grund af dens effektive komprimering og gode forhold mellem kvalitet og størrelse.

- **Udviklende standarder:**

MPEG-standarderne fortsætter med at udvikle sig for at følge med de teknologiske fremskridt. Nyere versioner og variationer, såsom MPEG-4 Part 10 (også kendt som H.264 eller AVC) og MPEG-4 Part 14 (MP4), tilbyder forbedret komprimeringseffektivitet og understøttelse af avancerede funktioner som high-definition video og 3D-indhold.

- **Multimedieapplikationer:**

MPEG-filer finder applikationer på forskellige områder, herunder digitalt tv, streamingtjenester, videokonferencer, videoovervågning, multimediepræsentationer og mere.

## MPEG vs andre formater

Når man sammenligner MPEG-filformatet med andre videoformater, spiller flere faktorer ind, herunder komprimeringseffektivitet, kompatibilitet, funktioner og support. Her er en sammenligning af MPEG med nogle populære videoformater:

### MPEG vs. AVI (Audio Video Interleave)

- **Kompression:**
   
MPEG-filer tilbyder generelt højere komprimeringseffektivitet sammenlignet med AVI, hvilket resulterer i mindre filstørrelser.

- **Kompatibilitet:**

AVI-filer er bredt understøttet af forskellige medieafspillere, men MPEG-filer har bredere kompatibilitet på tværs af enheder og platforme.

- **Funktioner:**

MPEG-filer understøtter ofte mere avancerede funktioner, såsom flere lydspor, undertekster og kapitler, mens AVI har begrænset understøttelse af sådanne funktioner.

- **Videokvalitet:**

Afhængigt af komprimeringsindstillingerne kan MPEG og AVI opnå lignende videokvalitet, men MPEG giver ofte bedre kvalitet ved lavere bithastigheder på grund af avancerede komprimeringsteknikker.

### MPEG vs. WMV (Windows Media Video):

- **Kompression:**

WMV-filer tilbyder generelt bedre komprimeringseffektivitet sammenlignet med MPEG, hvilket resulterer i mindre filstørrelser og samtidig opretholde god videokvalitet.

- **Kompatibilitet:**

MPEG-filer har bredere kompatibilitet på tværs af forskellige enheder og platforme, mens WMV-filer primært er forbundet med Windows-baserede systemer.

- **Funktioner:**

Begge formater understøtter en række funktioner, herunder flere lydspor og undertekster, men MPEG giver ofte mere alsidighed og bredere understøttelse af avancerede funktioner.

- **Videokvalitet:**

Med lignende komprimeringsindstillinger kan MPEG og WMV opnå sammenlignelig videokvalitet, men WMV kan fungere bedre i visse scenarier på grund af dets avancerede komprimeringsteknikker.

### MPEG vs. MP4 (MPEG-4 del 14):

- **Kompression:**

Både MPEG og MP4 bruger lignende komprimeringsteknikker, og komprimeringseffektiviteten kan være sammenlignelig. Men MPEG-4 Part 10 (H.264/AVC) i MP4 giver ofte bedre komprimering end ældre MPEG-formater.

- **Kompatibilitet:**

Både MPEG og MP4 har udbredt kompatibilitet på tværs af enheder og platforme. MP4 har vundet betydelig popularitet i de seneste år på grund af dens brede støtte og adoption.

- **Funktioner:**

MP4 tilbyder mere avancerede funktioner og muligheder, herunder understøttelse af undertekster, kapitler, interaktive menuer og avancerede video-codecs som H.264 og HEVC (H.265). MPEG-4 Part 2 (DivX, Xvid) i MP4 understøtter også avancerede funktioner.

- **Videokvalitet:**

MPEG og MP4 kan opnå lignende videokvalitet, når du bruger sammenlignelige komprimeringsindstillinger. MP4's understøttelse af mere avancerede video-codecs giver dog mulighed for bedre kvalitet ved lavere bithastigheder.

## Referencer
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)


