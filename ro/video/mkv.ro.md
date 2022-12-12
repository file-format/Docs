{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier MKV",
  "keywords" :[ "mkv", "matroska video", "mkv format", "cum se redă fișierele mkv", "video", "fișier", "format"],
  "description":"Aflați despre formatul de fișier MKV și despre API-urile care pot crea și deschide fișiere MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Ce este un fișier MKV? ##

MKV (Matroska Video) este un container multimedia similar cu formatul [MOV](/ro/video/mov/) și [AVI](/ro/video/avi/), dar acceptă mai mult de o pistă audio și subtitrare în același fișier. Un fișier MKV este formatul de container multimedia Matroska utilizat pentru videoclipuri. MKV se bazează pe Extensible Binary Meta Language și acceptă mai multe formate de compresie video și audio. Diferența majoră dintre MKV și alte formate video este că MKV este un container și nu un codec. Fișierele MKV sunt salvate cu extensia de fișier .mkv. MKV poate încorpora audio, video și subtitrări într-un singur fișier, chiar dacă aceste elemente folosesc diferite tipuri de codare. De exemplu, ați putea avea un fișier MKV care conține video H.264 și MP3 sau AAC pentru audio. MKV acceptă, de asemenea, descrieri, evaluări, ilustrații de copertă și chiar puncte de capitol. Există mai multe caracteristici cheie pentru care MKV este pregătit pentru viitor. Aceste caracteristici includ:

- Suport pentru căutare rapidă.
- Posibilitatea de a selecta diferite fluxuri audio și video.
- Suport pentru subtitrări (codate hard și soft-coded).
- Suport pentru metadate, capitole și meniuri.
- Capacitate de a transmite în flux online.
- Abilitatea de a recupera fișiere eronate care oferă capacitatea de a reda fișiere corupte.

## Scurt istoric ##

Fișierul MKV a apărut în 2002 în Rusia. Dezvoltatorul principal a fost Lasse Kärkkäinen, care a lucrat cu fondatorul Matroska, Steve Lhomme, și o echipă de programatori. MKV a fost dezvoltat ca un proiect cu standarde deschise, ceea ce înseamnă că este open source și este gratuit de utilizat. Odată cu trecerea timpului, formatul a fost îmbunătățit și a devenit baza formatului multimedia WebM în 2010.

## Matroska Design ##

Matroska adaugă următoarele constrângeri la specificația EBML.

- **docType** din **EBML Header** trebuie să fie „matroska”.
- **EBMLMaxIDLength** din **EBML Header** trebuie să fie 4.
- **EBMLMaxSizeLength** din **EBML Header** trebuie să fie între 1 și 8 (inclusiv).

Toate elementele de nivel superior sunt codificate în 4 octeți.

- Coduri de limbă: Matroska (versiunea 1 până la 3) a folosit coduri de limbă care pot fi fie forma bibliografică ISO-639-2 de 3 litere (cum ar fi „fre” pentru franceză), fie codul de țară suplimentar ar putea fi folosit ca „fre-ca " pentru franceza canadiană. Începând cu Matroska versiunea 4, ISO 639-2 sau BCP 47 POT fi utilizat pentru codurile de limbă, deși este recomandat BCP 47.
- Tipuri fizice: Acestea au semnificații diferite atât pentru fișierele audio, cât și pentru cele video. De exemplu, ChapterPhysicalEquiv = 60 înseamnă (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) pentru audio și (DVD / VHS / LASERDISC) pentru video.
- Structura blocului - Antetul blocului: Antetul blocului conține informații despre numărul piesei, marcajele de timp, tipul de strângere etc.
- Lacing: este un mecanism de economisire a spațiului la stocarea datelor, care este de obicei folosit pentru blocuri mici de date (cadre). Există 3 tipuri de șireturi:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Structura SimpleBlock: este inspirată din **structura blocului**, diferența principală fiind adăugarea de steaguri **Keyframe** și **Discardable**. În afară de asta, totul este la fel.

## Structura Matroska ##

Un document Matroska trebuie să fie compus din cel puțin un **Document EBML** folosind **Tipul de document Matroska**. Fiecare **Document EBML** trebuie să înceapă cu un **Antet EBML** urmat de **Elementul rădăcină EBML** care este definit ca un Segment. Matroska definește mai multe elemente de nivel superior care pot apărea în cadrul **Segmentului**.

EBML folosește un sistem de elemente pentru a compune un document EBML. Următoarea este lista de elemente de nivel superior din fișierul Matroska:

- **Document EBML**: Wrapper pentru întregul fișier.
- **EBML Header**: conține informațiile antetului pentru fișier precum DocType.
- **Segment**: elementul superior care conține toate celelalte elemente de nivel superior.
- **SeekHead**: conține poziția Segmentelor altor elemente de nivel superior.
- **Informații**: Conține informații generale despre Segment.
- **Tracks**: un element de informații de nivel superior cu multe piese descrise.
- **Capitole**: este folosit pentru a defini meniurile de bază și datele de partiție.
- **Cluster**: Elementul de nivel superior care conține structura blocului.
- **Indiciile**: un element de nivel superior care conține toate intrările locale ale Segmentului care accelerează căutarea accesului.
- **Atașamente**: Acesta conține fișiere atașate.
- **Etichete**: acest element conține metadate care descriu piese, ediții, capitole, atașamente sau Segmentul în ansamblu.

Următorul tabel arată structura documentului Matroska cu majoritatea elementelor afișate într-o ierarhie:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Antet EBML | | | |
| Segment | SeekHead| Caută | SeekID |
| | | | SeekPosition |
| | Info | SegmentUID | |
| | | SegmentFilename | |
| | | PrevUID | |
| | | PrevFilename | |
| | | NextUID | |
| | | NextFilename | |
| | | SegmentFamily | |
| | | Capitolul Traducere | |
| | | TimestampScale | |
| | | Durata | |
| | | DataUTC | |
| | | Titlu | |
| | | MuxingApp | |
| | | WritingApp | |
| | Piese | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Nume |
| | | | Limba |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | Culoare |
| | | | Audio | Frecvența de eșantionare |
| | | | | Canale |
| | | | | BitDepth |
| | Capitole | EditionEntry | EditionUID |
| | | | EdițieFlagHidden |
| | | | EditionFlagDefault |
| | | | EdițieFlagOrdered |
| | | | ChapterAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | Capitolul Steagul Ascuns |
| | | | | ChapterDisplay | ChapString |
| | | | | | ChapLanguage |
| | Cluster | Marca temporală |
| | | SilentTracks |
| | | Poziție |
| | | PrevSize |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Indicii | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Atasamente | Fișier atașat | Descriere fișier |
| | | | FileName |
| | | | FileMimeType |
| | | | FileUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Etichete | Etichetă | Ținte | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### Folosind codecuri ###

Dacă nu doriți un player media nou și preferați să utilizați playerul existent, va trebui să instalați niște codecuri (scurtare pentru compresie/decompresie). Chiar dacă descărcarea de codecuri este o opțiune validă, ar trebui să fiți atenți la sursă și acestea pot conține malware.

## Referințe ##

- [Matroska de la Wikipedia](https://en.wikipedia.org/wiki/Matroska)

