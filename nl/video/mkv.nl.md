{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKV-bestandsindeling",
  "keywords" :[ "mkv", "matroska video", "mkv-formaat", "hoe mkv-bestanden af te spelen", "video", "bestand", "formaat"],
  "description":"Meer informatie over MKV-bestandsindelingen en API's die MKV-bestanden kunnen maken en openen.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Wat is een MKV-bestand? ##

MKV (Matroska Video) is een multimediacontainer vergelijkbaar met de indelingen [MOV](/nl/video/mov/) en [AVI](/nl/video/avi/), maar ondersteunt meer dan één audio- en ondertiteltrack in hetzelfde bestand. Een MKV-bestand is het Matroska-multimediacontainerformaat dat voor video wordt gebruikt. MKV is gebaseerd op Extensible Binary Meta Language en ondersteunt verschillende video- en audiocompressieformaten. Het grote verschil tussen MKV en andere videoformaten is dat MKV een container is en geen codec. MKV-bestanden worden opgeslagen met de bestandsextensie .mkv. MKV kan audio, video en ondertitels in een enkel bestand opnemen, zelfs als die elementen verschillende soorten codering gebruiken. U kunt bijvoorbeeld een MKV-bestand hebben dat H.264-video en MP3 of AAC voor audio bevat. MKV ondersteunt ook beschrijvingen, beoordelingen, albumhoezen en zelfs hoofdstukpunten. Er zijn verschillende belangrijke kenmerken die MKV toekomstbestendig maken. Deze functies omvatten:

- Ondersteuning voor snel zoeken.
- Mogelijkheid om verschillende audio- en videostreams te selecteren.
- Ondersteuning voor ondertitels (hard-gecodeerd en zacht-gecodeerd).
- Ondersteuning voor metadata, hoofdstukken en menu's.
- Mogelijkheid om online te streamen.
- Mogelijkheid om foutieve bestanden te herstellen die de mogelijkheid bieden om beschadigde bestanden af te spelen.

## Korte geschiedenis ##

MKV-bestand is ontstaan in 2002 in Rusland. De hoofdontwikkelaar was Lasse Kärkkäinen die samenwerkte met de oprichter van Matroska, Steve Lhomme, en een team van programmeurs. MKV is ontwikkeld als een open standaardenproject, wat betekent dat het open source en gratis te gebruiken is. Naarmate de tijd verstreek, werd het formaat verbeterd en werd het in 2010 de basis van het WebM-multimediaformaat.

## Matroska-ontwerp ##

Matroska voegt de volgende beperkingen toe aan de EBML-specificatie.

- Het **docType** van de **EBML-header** moet 'matroska' zijn.
- De **EBMLMaxIDLength** van de **EBML-header** moet 4 zijn.
- De **EBMLMaxSizeLength** van de **EBML-header** moet tussen 1 en 8 (inclusief) zijn.

Alle elementen op het hoogste niveau zijn gecodeerd in 4 octetten.

- Taalcodes: Matroska (versie 1 t/m 3) gebruikte taalcodes die ofwel de 3-letterige bibliografische ISO-639-2-vorm kunnen zijn (zoals "fre" voor frans), of een extra landcode kan worden gebruikt zoals "fre-ca" " voor Canadees Frans. Vanaf Matroska versie 4 KAN ISO 639-2 of BCP 47 worden gebruikt voor taalcodes, hoewel BCP 47 wordt aanbevolen.
- Fysieke typen: deze hebben een verschillende betekenis voor zowel audio- als videobestanden. ChapterPhysicalEquiv = 60 betekent bijvoorbeeld (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) voor audio en (DVD / VHS / LASERDISC) voor video.
- Blokstructuur - Blokkop: Blokkop bevat informatie over tracknummer, tijdstempels, type veter, enz.
- Vetersluiting: het is een mechanisme om ruimte te besparen bij het opslaan van gegevens, dat doorgaans wordt gebruikt voor kleine gegevensblokken (frames). Er zijn 3 soorten vetersluiting:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock-structuur: het is geïnspireerd op de **Block-structuur**, met als belangrijkste verschil de toevoeging van **Keyframe** en **Discardable**-vlaggen. Verder is alles hetzelfde.

## Matroska-structuur ##

Een Matroska-document moet zijn samengesteld uit ten minste één **EBML-document** met het **Matroska-documenttype**. Elk **EBML-document** moet beginnen met een **EBML-header** gevolgd door het **EBML-hoofdelement** dat is gedefinieerd als een segment. Matroska definieert verschillende Top-Level Elements die binnen het **Segment** kunnen voorkomen.

EBML gebruikt een systeem van elementen om een EBML-document samen te stellen. Het volgende is de lijst met elementen op het hoogste niveau in het Matroska-bestand:

- **EBML Document**: Wrapper voor het hele bestand.
- **EBML Header**: het bevat de headerinformatie voor het bestand, zoals DocType.
- **Segment**: het bovenste element dat alle andere elementen op het hoogste niveau bevat.
- **SeekHead**: het bevat de positie van segmenten van andere elementen op het hoogste niveau.
- **Info**: het bevat algemene informatie over het segment.
- **Tracks**: een informatief element op het hoogste niveau met veel beschreven tracks.
- **Hoofdstukken**: het wordt gebruikt om basismenu's en partitiegegevens te definiëren.
- **Cluster**: het element op het hoogste niveau met de blokstructuur.
- **Aanwijzingen**: een element op het hoogste niveau dat alle lokale ingangen van het segment bevat die snel toegang zoeken.
- **Bijlagen**: dit bevat bijgevoegde bestanden.
- **Tags**: dit element bevat metadata die tracks, edities, hoofdstukken, bijlagen of het segment als geheel beschrijven.

De volgende tabel toont de structuur van het Matroska-document, waarbij de meeste elementen in een hiërarchie worden weergegeven:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML-koptekst | | | |
| Segment | ZoekHoofd| Zoek | Zoek-ID |
| | | | Zoekpositie |
| | Info | Segment-UID | |
| | | SegmentBestandsnaam | |
| | | PrevUID | |
| | | VorigeBestandsnaam | |
| | | VolgendeUID | |
| | | VolgendeBestandsnaam | |
| | | SegmentFamilie | |
| | | HoofdstukVertalen | |
| | | TijdstempelSchaal | |
| | | Duur | |
| | | DatumUTC | |
| | | Titel | |
| | | Muxing-app | |
| | | SchrijvenApp | |
| | Sporen | Trackinvoer | Tracknummer |
| | | | TrackUID |
| | | | TrackType |
| | | | Naam |
| | | | Taal |
| | | | Codec-ID |
| | | | CodecPrivé |
| | | | CodecNaam |
| | | | Video | Vlaggeïnterlinieerd |
| | | | | Veldvolgorde |
| | | | | StereoModus |
| | | | | AlphaModus |
| | | | | PixelBreedte |
| | | | | PixelHoogte |
| | | | | DisplayBreedte |
| | | | | WeergaveHoogte |
| | | | | AspectRatioType |
| | | | | Kleur |
| | | | Audio | Bemonsteringsfrequentie |
| | | | | Kanalen |
| | | | | Bitdiepte |
| | Hoofdstukken | EditieEntry | EditieUID |
| | | | EditieVlagVerborgen |
| | | | EditionFlagDefault |
| | | | EditieVlagBesteld |
| | | | HoofdstukAtom | HoofdstukUID |
| | | | | ChapterStringUID |
| | | | | HoofdstukTijdStart |
| | | | | HoofdstukTijdEinde |
| | | | | HoofdstukVlagVerborgen |
| | | | | HoofdstukWeergeven | ChapString |
| | | | | | ChapTaal |
| | Cluster | Tijdstempel |
| | | SilentTracks |
| | | Positie |
| | | VorigeGrootte |
| | | SimpleBlock |
| | | Blokgroep |
| | | EncryptedBlock |
| | Aanwijzingen | CuePunt | CueTime |
| | | | CueTrackPosities |
| | Bijlagen | Bijgevoegd bestand | Bestandsbeschrijving |
| | | | Bestandsnaam |
| | | | FileMimeType |
| | | | Bestand-UID |
| | | | Bestandsverwijzing |
| | | | BestandGebruiktStartTime |
| | | | BestandGebruiktEindtijd |
| | Tags | Tag | doelen | TargetTypeValue |
| | | | | Doeltype |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagHoofdstukUID |
| | | | | TagBijlageUID |
| | | | SimpleTag | TagNaam |
| | | | | TagTaal |
| | | | | TagStandaard |
| | | | | TagString |
| | | | | TagBinair |
| | | | | SimpleTag |


### Codecs gebruiken ###

Als u geen nieuwe mediaspeler wilt en liever uw bestaande speler gebruikt, moet u enkele codecs installeren (afkorting voor compressie/decompressie). Hoewel het downloaden van codecs een geldige optie is, moet u voorzichtig zijn met de bron en deze kunnen malware bevatten.

## Referenties ##

- [Matroska door Wikipedia](https://en.wikipedia.org/wiki/Matroska)

