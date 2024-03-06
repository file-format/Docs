{
  "date": "2019-10-11",
  "keywords": [
"jp2 fails",
"jp2 faila formāts",
"kas ir jp2 fails",
"failu",
"jp2 piemērs",
"jp2 faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JP2 — attēla faila formāts",
  "description": "Uzziniet par JP2 faila formātu un API, kas var izveidot un atvērt JP2 failus.",
  "linktitle": "JP2",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-lv2"
}
},
  "lastmod": "2020-08-10"
}

## Kas ir JP2 fails? ##

JPEG 2000 (**JP2**) ir attēlu kodēšanas sistēma un vismodernākais attēlu saspiešanas standarts. Tas izmanto viļņu tehnoloģiju, lai vienlaikus kodētu bezzudumu saturu jebkurā kvalitātē. Turklāt bez būtiskas sankcijas par kodēšanas efektivitāti JPEG 2000 spēj efektīvi piekļūt vienam un tam pašam saturam un to atšifrēt dažādās citās izšķirtspējās un kvalitātē. JPEG 2000 koda straumes ir ievērojami mērogojamas, un tajās ir interešu reģioni, kas nodrošina iespēju telpiskai nejaušai piekļuvei.

JPEG 2000 izceļas kā viens no visvairāk mērogojamajiem standartiem. Dažādas attēla daļas var saglabāt, izmantojot dažādas kvalitātes. Ievērojamu veiktspējas eskalāciju var panākt, pasūtot koda straumi dažādos veidos. Tomēr šīs elastības rezultātā JP2 ir nepieciešami sarežģīti un skaitļošanas ziņā sarežģīti kodētāji/dekoderi. Salīdzinājumā ar JPEG, JPEG 2000 rada tikai zvana artefaktus, kas veido gredzenus attēla malas tuvumā un var būt izplūduši, savukārt JPEG izmanto 8 × 8 vizuālo artefaktu blokus, kas var būt gan zvana, gan bloķējoši artefakti. Tam ir līdz 16 384 dažādi komponenti ar izmēriem terapikseļos un precizitāte, kas var sasniegt 38 bitus paraugā.

## Vēsture ##

2000. gadā Apvienotās fotogrāfijas ekspertu grupas komiteja izstrādāja JP2 ar mērķi uzlabot savu diskrēto kosinusa transformāciju balstītu JPEG standartu, izmantojot šo jauno viļņu metodi. JPEG komitejas mērķis bija nodrošināt savas bāzes metodes bez licences maksas. JP2 licencē, iegūstot konkurenci starp 20 uzņēmumiem, viņi uzvarēja ar ūsām. JPEG 2000 ir pasludināts par ISO standartu, lai gan lielākā daļa tīmekļa pārlūkprogrammu kopš 2017. gada nav gatavas sniegt roku JPEG 2000.

## JPEG 2000 attēlu kodēšanas sistēmas daļas ##

Tālāk ir norādītas galvenās daļas, kas veido pilnu JPEG 2000 standartu komplektu.


|Daļa|Nosaukums|Apraksts|Numurs
---|---|---|---|
|1.daļa|Kodēšanas pamatsistēma| Definē koda straumes sintaksi. Dažādi JPEG 2000 attēlu dekodēšanas posmi. Izskaidrojamais faila pamatformāts JP2, metadati un IP tiesības.|ISO/IEC 15444-1
|2.daļa|Paplašinājumi|Definē faila formāta koda straumes paplašinājumus un ļauj demonstrēt HDR paraugus, noteikt krāsu telpas specifikāciju, apgriezt, ģeometriskās transformācijas. dažādas animācijas, metadati un vairāku kodu straume.|ISO/IEC 15444-2
|3.daļa|Motion JPEG 2000 (MJ2 vai MJP2)|Ieviesiet failu formātu kustību sekvencēm, kodē attēlus neatkarīgā koda straumē.|ISO/IEC 15444-3
|4.daļa|Atbilstība|Norāda pārbaudes metodes kodēšanai un dekodēšanai un pārbauda failus gan tukškoda straumēm, gan JP2 failiem.|ISO/IEC 15444-4
|5.daļa|Atsauces programmatūra|Sastāv no divām pirmkoda pakotnēm (Java, C), kas ievieš Core kodēšanas sistēmu un ir pieejamas ar atvērtā pirmkoda licencēm.|ISO/IEC 15444-5
|6.daļa|Saliktā attēla faila formāts|Nosaka JPM faila formātu un nodrošina vairāku lappušu dokumentu attēlveidošanu faksam līdzīgām lietojumprogrammām. Atbalsta JBIG2 un JPEG izmantošanu.|ISO/IEC 15444-6
|8. daļa|JPEG 2000 aizsargāts (JPSEC)|Nodrošina darījumu, satura un tehnoloģiju drošību un nodrošina aizsargātas JPEG 2000 bitu straumes.|ISO/IEC 15444-8
|9.daļa|JPIP|Definē rīkus tīkla vidē, lai piekļūtu metadatiem un attēliem, un norāda interaktīvus un efektīvus protokolus|ISO/IEC 15444-9
|10.daļa|JP3D|1.daļas tilpuma paplašinājums un ievieš Z dimensiju. Paplašina elementu, kodu bloku, iecirkņu un 3D interešu reģiona pieejamības funkciju jēdzienu.|ISO/IEC 15444-10
|Part 11|JPWL|Nodarbojas ar labi organizētu pārraidi bezvadu tīklā, kurā var rasties kļūdas. Šis paplašinājums ir saderīgs ar dekoderiem|ISO/IEC 15444-11
|13.daļa|Sākumlīmeņa kodētājs|Definē Core kodēšanas sistēmas sākuma līmeņa kodētāja ieviešanu.|ISO/IEC 15444-13
|14. daļa|JPXML|A attēlojums XML formātā un izskaidro marķieru segmentus un metodes, lai piekļūtu attēlu iekšējiem datiem.|ISO/IEC 15444-14
|Part 15|HTJ2K (Nepietiekami izstrādāts)|Norāda alternatīvu bloku kodēšanas algoritmu. Algoritms piedāvā desmit reizes lielāku caurlaidspēju un bezzudumu kodēšanu/dekodēšanu.|

## JP2 faila formāts ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Lai gan attēlu paraugus apraksta tikai JPEG 2000, tomēr JPEG-1 ietver citu pievienoto informāciju par krāsu telpu un izšķirtspēju, kas ir būtiska attēla kodēšanai. Ja attēls ir saglabāts kā JPEG 2000 fails, kā paplašinājums tiek izmantots **.jp2**. Šo faila formātu vēl vairāk uzlabo JPEG 2000 2. daļas paplašinājums, kas definē animācijas mehānismus un daudzu koda straumju konfigurāciju vienā attēlā. **.jpx** paplašinājums tiek izmantots, kad attēli tiek saglabāti, izmantojot šo paplašināto faila formātu. Tā kā koda straumes dati netiek uzskatīti par galvenokārt saglabātiem failos, šim nolūkam nav definēts standarta paplašinājums. Lai gan testēšanas nolūkos tas bieži iegūst paplašinājumu **.jpc** vai **.j2k**. Pretēji JPEG-1, JPEG 2000 izvēlas citu veidu, kā kodēt metadatus XML formātā. Standarts 12234-1.4 (ISO TC42 komiteja) tiek izmantots kā atsauce starp Exif tagiem un XML komponentiem. JPEG 2000 var ietvert ISO standartu, XMP.

### Gabali ###
JPEG 2000 faili sastāv no secīgiem gabaliem. Katrai daļai ir 8 baitu galvene: 4 baitu gabala lielums (lielais baits, vispirms augstais baits) un 4 baitu gabala tips — viens no iepriekš definētiem parakstiem: jP vai jP2.

Second chunk must be of type "ftyp" and has a sub-type at offset 8. JPEG 2000, kas definēts pēc apakštipa, kuram ir jābūt vienai no vērtībām: jp2 (faila tips \*.JP2), jp20 (faila tips \*.JPA), jpm (faila tips \*.JPM), jpx (faila tips \*.JPX).

Atkārtojot gabalus, līdz tiek atklāts nezināms veids, mēs veidojam JPEG 2000 attēla/video failu.

### Krāsu transformācija ###

Sākotnēji ir nepieciešama attēlu pārveidošana no RGB krāsu telpas uz citu krāsu telpu. Šim nolūkam ir divi veidi: neatgriezeniskā krāsu transformācija (ICT) un atgriezeniskā krāsu transformācija (RCT). Iepriekšējais izmanto YC,,B,,C,,R,,krāsu telpu, un tas ir jārealizē fiksētā/peldošā punktā, bet vēlāk modificētā YUV krāsu telpā un pēc būtības ir atgriezeniska.// //Nav tikai RGB modelim, JPEG 2000 valoda izmanto vairāku komponentu transformāciju.

### Flīžu ieklāšana ###

Kad krāsu pārveidošana ir pabeigta, attēls tiek pārveidots par taisnstūrveida apgabaliem, ko sauc par elementiem, kurus var pārveidot un kodēt atsevišķi. Visu flīžu izmērs būs vienāds vai visu attēlu var uzskatīt par vienu flīzi. Dekodētājs izmanto flīžu priekšrocības un patērē mazāk atmiņas vai var daļēji kodēt dažus elementus. Lai gan šīs metodes trūkums ir attēla kvalitātes pasliktināšanās.

### Wavelet transformācija ###

Attēls pēc flīžu ieklāšanas tiek pārveidots par viļņveida transformāciju, kas var būt neatgriezenisks vai atgriezenisks, un tiek realizēts, izmantojot konvolūcijas vai pacelšanas shēmu.

### Kompresijas pakāpe ###

Atkarībā no attēla fiziskajām īpašībām tiek iegūts 20% kompresijas pieaugums. JPEG 2000 telpiskās redundances prognozēšanai ir būtiska nozīme saspiešanas procesā, un augstas izšķirtspējas attēliem ir tendence iegūt vislielākās priekšrocības.

## Lietojumprogrammas, ko apkalpo standarts ##

* Uz kadriem balstītu HD video ierakstīšana, rediģēšana un uzglabāšana

* Medicīniskie attēli un biometriskie dati

* satelītattēli, attālā uzrāde un kustības noteikšana

* Klienta/servera komunikācija, tīkla izplatīšana un uzglabāšana.

* Digitālais kino, HDTV tiešraides plūsma, digitalizēti audiovizuālie materiāli


## Atsauces Nr.

* [Pārskats par JPEG 2000](https://jpeg.org/jpeg2000/)

* [JPEG 2000 attēlu kodēšanas sistēma](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)


