{
  "date": "2019-10-11",
  "keywords": [
"exif fails",
"exif faila formāts",
"kas ir exif fails",
"failu",
"exif piemērs",
"exif faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EXIF",
  "description": "Uzziniet par EXIF faila formātu un API, kas var izveidot un atvērt EXIF failus.",
  "linktitle": "EXIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-exi-lvf"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir EXIF fails?
EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. No šodienas standartu pārvalda Japānas Elektronikas un informācijas tehnoloģiju nozaru asociācija (JEITA). EXIF ir standarts attēlu un skaņas formātu specifikācijām, ko galvenokārt izmanto digitālās kameras un skeneri.

EXIF standarts ietver marķēšanas un metadatu informāciju ar attēla failu. Metadati var saturēt tādu informāciju kā kameras modelis, aizvara ātrums, datums un laiks, diafragmas atvērums, ražotājs, ekspozīcijas laiks, X izšķirtspēja, Y izšķirtspēja utt. Parasti EXIF dati pēc noklusējuma tiek paslēpti. Lai skatītu EXIF datus, attēlu skatīšanas lietojumprogrammā ir jāizvēlas skata rekvizīti. Exif metadatos var ietvert arī sīktēlus, kā arī tehniskos un primāros attēla datus vienā attēla failā.

## Vēsture un versijas ##

* 1995. gada oktobrī JEIDA izveidoja 1. versiju. Šajā versijā JEIDA definēja struktūru, kas sastāv no attēla datu formāta un atribūtu informācijas un pamata tagiem.

* 1997. gada novembra versija 1.1 tika ieviesta ar lielāko daļu tagu no 1. versijas, taču tika pievienoti arī noteikumi par neobligātu atribūtu informāciju un formāta darbību.

* 1998. gada jūnijs, 2. versija ar sRGB krāsu telpu, saspiestiem sīktēliem un audio failiem.

* 1998. gada decembris, versija 2.1 ar uzlabotu krātuvi un atribūtu informāciju.

* 2002. gada februāris, versija 2.2, uzlabota versija 2.1, pievienojot drukas apdari.

* 2003. gada septembris, versija 2.21 ar papildu krāsu telpu, kas pazīstama kā Adobe RGB.


## EXIF faila formāts

EXIF izmanto šādus failu formātus, pievienojot īpašus metadatus.

1. [JPEG](/image/jpeg/) — diskrēta kosinusa transformācija (DCT) saspiestiem attēlu failiem.
1. [TIFF](/image/tiff/) Rev. 6.0 (RGB vai YCbCr) nesaspiestiem attēlu failiem.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) audio failiem (Lineārais [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) vai ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM nesaspiestiem audio datiem, un [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) saspiestiem audio datiem).

### EXIF izmantotais marķieris ###

Marķieris 0xFFE0~~0xFFEF ir Application Marker, ko izmanto lietotāja lietojumprogramma. Piemēram, vecākās digitālās kameras attēlu glabāšanai izmanto JFIF (JPEG failu apmaiņas formātu). JFIF izmanto APP0 (0xFFE0) marķieri, lai ievietotu digitālās kameras konfigurācijas datus un sīktēlu. Turklāt EXIF izmanto arī lietojumprogrammu marķieri datu ievietošanai, bet EXIF izmanto APP1 (0xFFE1) marķieri, lai izvairītos no konflikta ar JFIF formātu. Katrs EXIF failu formāts sākas ar šo formātu.


|SOI marķieris|APP1 marķieris|APP1 dati|cits marķieris
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Tas sākas no SOI (0xFFD8) marķiera, tāpēc tas ir JPEG fails. Tad uzreiz seko marķieris APP1. Visi EXIF dati tiek glabāti šajā APP1 datu apgabalā. SSSS daļa augšējā tabulā nozīmē APP1 datu apgabala lielumu (EXIF datu apgabals). Lūdzu, ņemiet vērā, ka izmērs SSSS ietver arī paša deskriptora lielumu. Pēc SSSS sākas APP1 dati. Pirmā daļa ir īpaši dati, lai identificētu, vai tiek izmantots EXIF vai nē, ASCII rakstzīme EXIF un 2 baiti 0x00. Pēc APP1 marķiera apgabala seko pārējie JPEG marķieri.

### Exif datu struktūra ###

Aptuvena EXIF datu struktūra (APP1) ir parādīta, kā parādīts tālāk. Kā minēts iepriekš, EXIF dati sākas no ASCII rakstzīmes EXIF un 2 baitiem 0x00, pēc tam seko EXIF dati. EXIF datu glabāšanai izmanto TIFF formātu.


|FFE1|APP1 marķieris
---|---|
|SSSS|APP1 dati|APP1 datu lielums
|45786966 0000|Exif galvene
|49492A00 08000000|TIFF galvene
|XXXX. . . .|IFD0 (galvenais attēls) | Katalogs
|LLLLLLLL|Saite uz IFD1
|XXXX. . . .|IFD0 datu apgabals
|XXXX. . . .|Exif SubIFD|Directory
|00000000|Saites beigas
|XXXX. . . .|Exif SubIFD datu apgabals
|XXXX. . . .|IFD1(sīktēla attēls)|Katalogs
|00000000|Saites beigas
|XXXX. . . .|IFD1 datu apgabals
|FFD8XXXX. . . XXXXFFD9|Sīktēls

#### TIFF galvene ####

8 baitu [TIFF](/image/tiff/) faila galvenē ir šāda informācija:

`Baiti 0-1:` Failā izmantotā baitu secība. Juridiskās vērtības ir: II”(4949.H)”MM” (4D4D.H).

II” formātā baitu secība vienmēr ir no vismazāk nozīmīgākā baita līdz visnozīmīgākajam baitam gan 16 bitu, gan 32 bitu veseliem skaitļiem To sauc par mazo baitu secību. MM” formātā baitu secība vienmēr ir no visnozīmīgākā līdz vismazāk nozīmīgajam gan 16 bitu, gan 32 bitu veseliem skaitļiem. To sauc par lielo baitu secību.

`Baiti 2-3:` Patvaļīgs, bet rūpīgi izvēlēts skaitlis (42), kas tālāk identificē failu kā TIFF failu. Baitu secība ir atkarīga no 0-1 baitu vērtības.

`Baiti 4-7:` Pirmā IFD nobīde (baitos). Direktorija var atrasties jebkurā faila vietā pēc galvenes, bet jāsākas ar vārda robežu. Jo īpaši attēlu failu direktorijs var sekot tajā aprakstītajiem attēla datiem. Lasītājiem ir jāseko norādēm, lai kur tie varētu novest. Termins baitu nobīde šajā dokumentā vienmēr tiek lietots, lai apzīmētu vietu attiecībā pret TIFF faila sākumu. Faila pirmā baita nobīde ir 0.

#### Attēlu failu direktorijs ####

IFD satur informāciju par attēlu, kā arī norādes uz faktiskajiem attēla datiem. Tas sastāv no direktoriju ierakstu skaita (ti, lauku skaita) 2 baitu skaita, kam seko 12 baitu lauku ierakstu secība. , kam seko nākamā IFD 4 baitu nobīde (vai 0, ja tāda nav). TIFF failā ir jābūt vismaz 1 IFD, un katram IFD ir jābūt vismaz vienam ierakstam.

##### IFD ieraksts #####

Katrs 12 baitu IFD ieraksts ir šādā formātā.


|Baiti|Apraksts
---|---|
|0-1|Taga, kas identificē lauku
|2-3|Lauka tips
|4-7|Norādītā tipa skaits
|8-11|Vērtības nobīde, lauka vērtības faila nobīde (baitos). Vērtībai jāsākas uz vārda robežas; tādējādi atbilstošā Vērtības nobīde būs pāra skaitlis. Šī faila nobīde var norādīt jebkurā faila vietā, pat pēc attēla datiem

TIFF lauks ir loģiska entītija, kas sastāv no TIFF taga un tā vērtības. Šī loģiskā koncepcija tiek īstenota kā IFD ieraksts, kā arī faktiskā vērtība, ja tā neietilpst vērtības/nobīdes daļā, pēdējie 4 IFD ieraksta baiti. Termini TIFF lauks un IFD ieraksts vairumā kontekstu ir savstarpēji aizstājami.

#### Sīktēls ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. Ir 3 sīktēlu formāti; JPEG formāts (JPEG izmanto YCbCr), RGB TIFF formāts, YCbCr TIFF formāts.

##### JPEG formāta sīktēls #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. Šķiet, ka JPEG formāts un 160x120 pikseļi ir ieteicami sīktēlu formātā Exif2.1 vai jaunākai versijai.

##### TIFF formāta sīktēls #####

Ja Compression(0x0103) Tag vērtība IFD1 ir 1”, sīktēlu formāts nav saspiešana (saukts par TIFF attēlu). Sīktēlu datu sākumpunkts ir StripOffset(0x0111) Tags, sīktēla lielums ir tagu StripByteCounts(0x0117) summa.

## Atsauces Nr.

* [EXIF — Wikipedia](https://en.wikipedia.org/wiki/Exif)

* [EXIF faila formāts](https://www.media.mit.edu/pia/Research/deepview/exif.html)


