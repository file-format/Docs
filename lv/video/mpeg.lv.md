{
  "date": "2023-07-12",
  "keywords": [
"mpeg",
"mpeg fails",
"kas ir mpeg fails",
"kā atvērt mpeg failu",
"failu",
"mpeg faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "MPEG faila formāts — MPEG video",
  "description": "Uzziniet par MPEG formātu un API, kas var izveidot un atvērt MPEG failus.",
  "linktitle": "MPEG",
  "menu": {
    "docs": {
      "identifier": "video-mpeg-lv",
      "parent": "video"
}
},
  "lastmod": "2023-07-12"
}

## Kas ir MPEG fails?

MPEG fails, kas pazīstams arī kā MPEG video fails, ir digitālā video faila formāts, kas video saspiešanai izmanto Moving Picture Experts Group (MPEG) standartus. MPEG ir plaši izmantots formāts video datu glabāšanai un pārsūtīšanai.

MPEG formātā tiek izmantota kompresija ar zaudējumiem, kas nozīmē, ka daļa informācijas tiek izmesta, lai samazinātu faila lielumu. Šis saspiešanas paņēmiens ļauj efektīvi uzglabāt un straumēt video saturu, vienlaikus saglabājot saprātīgu video kvalitāti. Ir vairākas MPEG standarta versijas, tostarp MPEG-1, MPEG-2, MPEG-4 un MPEG-7, katrai no tām ir atšķirīgs saspiešanas un kvalitātes līmenis.

MPEG failiem parasti ir faila paplašinājums .mpeg vai .mpg. Tajos var būt gan video, gan audio dati, kas bieži vien ir apvienoti vienā failā. MPEG faili ir saderīgi ar plašu multivides atskaņotāju un video rediģēšanas programmatūru klāstu, padarot tos par populāru izvēli video satura kopīgošanai un izplatīšanai.

## Kā atvērt MPEG failu?

Ir pieejamas daudzas lietojumprogrammas, kas var atvērt un atskaņot MPEG failus. Šeit ir dažas populāras iespējas:

- VLC Media Player
- Windows Media Player
- QuickTime atskaņotājs
- MPC-HC
- GOM atskaņotājs
- MPlayer
- PotPlayer
- Kodi

## Kā konvertēt MPEG failu?

Ir vairākas video lietojumprogrammas, tostarp VideoLAN VLC multivides atskaņotājs, HandBrake un Apple QuickTime Player, kas var konvertēt MPEG failus citos formātos. Piemēram, VLC var konvertēt MPEG failus šajos formātos

- MP4
- AVI
- MKV
- MOV
- WMV
- FLV

## MPEG failu iekšējās struktūras pārskats

MPEG failu iekšējā struktūra sastāv no dažādiem komponentiem un datu struktūrām, kas organizē un glabā video, audio un citu saistītu informāciju. Šeit ir pārskats par galvenajiem elementiem MPEG failu iekšējā struktūrā:

- **Sistēmu slānis:**

Sistēmu slānis nosaka kopējo MPEG faila struktūru. Tajā ir iekļautas galvenes, programmu straumes un citi ar sistēmu saistīti dati, kas nepieciešami dekodēšanai un atskaņošanai. Sistēmu slānis ir atbildīgs par elementāro straumju sinhronizācijas un multipleksēšanas pārvaldību.

- **Elementary straumes:**

MPEG faili satur atsevišķas elementāras straumes video, audio un citiem datu veidiem. Katra elementārā straume satur saspiestus datus, kas raksturīgi tās veidam. Piemēram, video elementārajā straumē ir saspiesti video kadri, un audio elementārajā straumē ir saspiesti audio paraugi.

- **Video saspiešana:**

MPEG video saspiešanas metodes, piemēram, iekškadra un starpkadru saspiešana, tiek izmantotas, lai samazinātu faila lielumu, vienlaikus saglabājot video kvalitāti. Saspiestie video kadri ir sakārtoti attēlu grupās (GOP), kas sastāv no iekškodētiem (I), paredzētajiem (P) un divvirzienu (B) kadriem.

- **Audio kompresija:**

MPEG faili atbalsta dažādus audio kompresijas kodekus, piemēram, MP3, AAC vai MPEG-1 Audio Layer II. Audio paraugi tiek saspiesti, izmantojot šos kodekus, kas ļauj efektīvi uzglabāt un pārraidīt audio datus.

- ** Sinhronizācija un laiks:**

MPEG faili izmanto laikspiedolus un sinhronizācijas informāciju, lai nodrošinātu pareizu video un audio straumju izlīdzināšanu atskaņošanas laikā. Šie laikspiedoli palīdz uzturēt sinhronizāciju un nodrošina precīzu audio un video kadru dekodēšanas un renderēšanas laiku.

- **Metadati:**

MPEG faili var ietvert metadatus, kas sniedz papildu informāciju par video un audio saturu. Šajos metadatos var būt ietverta tāda informācija kā nosaukums, autors, izveides datums un cita aprakstoša informācija.

- **Paketes un pakotņu galvenes:**

MPEG faili sakārto datus paketēs. Katrā paketē ir pakotnes galvene, kas sniedz informāciju par paketes saturu, piemēram, straumes veidu, paketes lielumu un laika informāciju.

- **Programmas specifiskā informācija (PSI):**

PSI ir sadaļa MPEG failos, kurā ir papildu informācija par programmu straumēm, piemēram, programmas un straumes identifikatori, straumes veids un deskriptori. PSI palīdz dekodēt un demultipleksēt elementārās straumes failā.

- **Transporta straume:**

MPEG-2 ir īpašs transporta plūsmas formāts, ko izmanto video satura apraidei un pārsūtīšanai. Transporta plūsma multipleksē vairākas programmas vienā straumē, ļaujot efektīvi pārraidīt un sinhronizēt audio, video un citus datus tīklos.

## MPEG faila formāts — vairāk informācijas

Šeit ir dažas svarīgas lietas, kas jāzina par MPEG faila formātu:

- **Saspiešana:**

MPEG faili izmanto zaudējumus saspiešanas metodes, lai samazinātu faila lielumu, vienlaikus saglabājot saprātīgu video kvalitāti. Saspiešanas apjoms var atšķirties atkarībā no MPEG versijas un izmantotajiem iestatījumiem.

- **Video un audio:**

MPEG faili var saturēt gan video, gan audio datus. Video dati tiek saspiesti, izmantojot MPEG standartus, savukārt audio var tikt saspiests, izmantojot dažādus audio kodekus, piemēram, MP3 vai AAC.

- **MPEG versijas:**

   There are different versions of the MPEG standard, including MPEG-1, MPEG-2, MPEG-4, and MPEG-7. Each version has its own specifications, capabilities, and levels of compression. MPEG-1 is commonly used for VCDs (Video CDs), while MPEG-2 is used for DVDs and broadcast television. MPEG-4 is widely used for online video streaming, and MPEG-7 focuses on multimedia content description and metadata.

- **Failu paplašinājumi:**

MPEG failiem parasti ir failu paplašinājumi .mpeg vai .mpg. Tomēr var pastāvēt dažādi varianti un paplašinājumi, piemēram, .mp4 MPEG-4 failiem vai .mp3 MPEG-1 audio slāņa 3 failiem.

- **Starpplatformu saderība:**

MPEG failus plaši atbalsta dažādi multivides atskaņotāji, operētājsistēmas un ierīces. Tos var atskaņot Windows, Mac un Linux sistēmās, kā arī viedtālruņos, planšetdatoros un viedtelevizoros.

- **Rediģēšana:**

MPEG failus var rediģēt, izmantojot video rediģēšanas programmatūru. Tomēr, tā kā MPEG izmanto kompresiju ar zaudējumiem, atkārtota faila rediģēšana un pārkodēšana var izraisīt kvalitātes pasliktināšanos. Bieži vien pirms plašas rediģēšanas ieteicams strādāt ar formātiem bez zudumiem vai izveidot rezerves kopijas.

- **Straumēšana:**

MPEG failus parasti izmanto video satura straumēšanai internetā. Jo īpaši MPEG-4 ir populārs tiešsaistes video platformās un video koplietošanas vietnēs, pateicoties tā efektīvai saspiešanai un labajai kvalitātes un izmēra attiecībai.

- **Attīstās standarti:**

MPEG standarti turpina attīstīties, lai neatpaliktu no tehnoloģiju sasniegumiem. Jaunākas versijas un variācijas, piemēram, MPEG-4 10. daļa (pazīstama arī kā H.264 vai AVC) un MPEG-4 14. daļa (MP4), piedāvā uzlabotu saspiešanas efektivitāti un atbalstu tādām uzlabotām funkcijām kā augstas izšķirtspējas video un 3D saturs.

- **Multivides lietojumprogrammas:**

MPEG faili atrod lietojumprogrammas dažādās jomās, tostarp digitālajā televīzijā, straumēšanas pakalpojumos, video konferencēs, videonovērošanā, multivides prezentācijās un citās jomās.

## MPEG pret citiem formātiem

Salīdzinot MPEG faila formātu ar citiem video formātiem, tiek ņemti vērā vairāki faktori, tostarp saspiešanas efektivitāte, saderība, funkcijas un atbalsts. Šeit ir MPEG salīdzinājums ar dažiem populāriem video formātiem:

### MPEG pret AVI (audio video interleave)

- **Saspiešana:**
   
MPEG faili parasti piedāvā augstāku saspiešanas efektivitāti salīdzinājumā ar AVI, kā rezultātā failu izmēri ir mazāki.

- **Saderība:**

AVI failus plaši atbalsta dažādi multivides atskaņotāji, taču MPEG failiem ir plašāka saderība starp ierīcēm un platformām.

- **Iespējas:**

MPEG faili bieži atbalsta uzlabotas funkcijas, piemēram, vairākus audio ierakstus, subtitrus un nodaļas, savukārt AVI ir ierobežots atbalsts šādām funkcijām.

- **Video kvalitāte:**

Atkarībā no saspiešanas iestatījumiem MPEG un AVI var sasniegt līdzīgu video kvalitāti, taču MPEG bieži nodrošina labāku kvalitāti ar zemāku bitu pārraides ātrumu uzlaboto saspiešanas metožu dēļ.

### MPEG pret WMV (Windows Media Video):

- **Saspiešana:**

WMV faili parasti piedāvā labāku saspiešanas efektivitāti, salīdzinot ar MPEG, kā rezultātā faila izmēri ir mazāki, vienlaikus saglabājot labu video kvalitāti.

- **Saderība:**

MPEG failiem ir plašāka saderība ar dažādām ierīcēm un platformām, savukārt WMV faili galvenokārt ir saistīti ar sistēmām, kuru pamatā ir Windows.

- **Iespējas:**

Abi formāti atbalsta virkni funkciju, tostarp vairākus audio ierakstus un subtitrus, taču MPEG bieži nodrošina daudzpusīgāku un plašāku papildu funkciju atbalstu.

- **Video kvalitāte:**

Ar līdzīgiem saspiešanas iestatījumiem MPEG un WMV var sasniegt salīdzināmu video kvalitāti, taču WMV noteiktos scenārijos var darboties labāk, pateicoties uzlabotajām saspiešanas metodēm.

### MPEG pret MP4 (MPEG-4 14. daļa):

- **Saspiešana:**

Gan MPEG, gan MP4 izmanto līdzīgas saspiešanas metodes, un saspiešanas efektivitāte var būt salīdzināma. Tomēr MPEG-4 10. daļa (H.264/AVC) MP4 formātā bieži nodrošina labāku saspiešanu nekā vecāki MPEG formāti.

- **Saderība:**

Gan MPEG, gan MP4 ir plaši izplatīta saderība starp ierīcēm un platformām. MP4 pēdējos gados ir ieguvis ievērojamu popularitāti, pateicoties tā plašajam atbalstam un pieņemšanai.

- **Iespējas:**

MP4 piedāvā uzlabotas funkcijas un iespējas, tostarp atbalstu subtitriem, nodaļām, interaktīvām izvēlnēm un uzlabotiem video kodekiem, piemēram, H.264 un HEVC (H.265). MPEG-4 2. daļa (DivX, Xvid) MP4 atbalsta arī uzlabotās funkcijas.

- **Video kvalitāte:**

Izmantojot salīdzināmus saspiešanas iestatījumus, MPEG un MP4 var sasniegt līdzīgu video kvalitāti. Tomēr MP4 atbalsts uzlabotākiem video kodekiem nodrošina labāku kvalitāti ar zemāku bitu pārraides ātrumu.

## Atsauces
* [MPEG-1](https://en.wikipedia.org/wiki/MPEG-1)


