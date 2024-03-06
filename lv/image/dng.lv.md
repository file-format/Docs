{
  "date": "2019-10-11",
  "keywords": [
"dng fails",
"dng faila formātā",
"kas ir dng fails",
"failu",
"dng piemērs",
"dng faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DNG — digitālās kameras attēla faila formāts",
  "description": "Uzziniet par DNG failu formātu un API, kas var izveidot un atvērt DNG failus.",
  "linktitle": "DNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dn-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir DNG fails?

DNG is a digital camera image format used for the storage of raw files. It has been developed by Adobe in September 2004. Tas galvenokārt tika izstrādāts digitālajai fotogrāfijai. DNG ir [TIFF](/image/tiff/)/EP standarta formāta paplašinājums, un tajā ievērojami tiek izmantoti metadati. Lai manipulētu ar neapstrādātiem datiem no digitālajām kamerām ar vieglu elastību un māksliniecisku kontroli, fotogrāfi izvēlas kameru neapstrādātus failus. JPEG un TIFF formātos tiek glabāti attēli, kurus apstrādā kamera, tāpēc šādos formātos nav daudz vietas pārveidošanai.

## DNG faila formāta vēsture un versijas

Till now there have been 5 versions of DNG specification so far. Version 1.0.0.0 was launched in September 2004 along with the release of "2.3" (ACR and DNG Converter). In February 2005 version 1.1.0.0 was published.  In May 2008 version 1.2.0.0 was released and was used in "4.4". Version 1.3.0.0 was published in June 2009. Versija 1.4.0.0 parādījās 2012. gadā.

## DNG faila formāts

Savukārt kameras neapstrādātie faili tver neapstrādātus vai zemu apstrādātus datus tieši no sensora. Tā kā tie ir līdzīgi filmu negatīviem, kameras neapstrādātie formāti ir pazīstami arī kā digitālie negatīvi. Neapstrādātu formātu priekšrocība ir gala lietotāja palielināta mākslinieciskā kontrole. Lietotājs var pielāgot dažādus parametru diapazonus atbilstoši prasībām, piemēram, baltā balansam, toņu kartēšanai, trokšņu samazināšanai, asināšanai un tā tālāk. No otras puses, kameras neapstrādātais fails ir jāapstrādā jebkurai lietošanai, izmantojot jebkuru programmatūru vai pārveidotāju.

Tā kā kameras neapstrādātajiem failiem nebija pieejams standarta formāts, galalietotājam tas radīja vairākas problēmas. Šīs problēmas risināja Adobe un definēja nepatentētu formātu kameras neapstrādātajiem failiem. Formāts ir pazīstams kā Digital Negative vai DNG. DNG var izmantot plaša aparatūras un programmatūras klāsts neapstrādātu failu apstrādei. Turklāt DNG var izmantot arī kā starpformātu, lai saglabātu attēlus, kas sākotnēji tika uzņemti ar kameru, kam ir savi patentēti neapstrādāti formāti.

### DNG faila formāta specifikācijas

Šajā sadaļā mēs aprakstīsim DNG formātu kā TIFF 6.0 paplašinājumu.

* **Failu paplašinājumi**: DNG izmanto paplašinājumus “.DNG” vai “.TIF”.

* **SubIFD koki**: DNG neatbalsta SubIFD ķēdes, tā vietā DNG iesaka izmantot SubIFD kokus, kā minēts TIFF-EP specifikācijās. Augstākajā kvalitātē un izšķirtspējā var izmantot NewSubFileType 0, savukārt pazeminātas kvalitātes sīktēliem ir jāizmanto NewSubFileType, kas vienāds ar 1. Ir arī ieteicams, lai gan tas nav obligāti, ka pirmajam IFD ir jābūt zemas kvalitātes vai izšķirtspējas sīktēlam.

* **Baitu secība**: DNG lasītājiem ir jāatbalsta baitu secība, arī failiem no noteikta kameras modeļa.

* **Maskētie pikseļi**: lielākā daļa kameras sensoru aprēķina pilnībā maskētus pikseļus sensora malās, izmantojot melnu kodējumu. Šos pikseļus var iekļaut vai apgriezt, pirms attēls tiek saglabāts DNG formātā. Ja maskētie pikseļi nav apgriezti, tad ActiveArea tagā ir jānorāda šo pikseļu laukums. No šiem pikseļiem iegūtā informācija par melnās krāsas kodēšanas līmeni ir jāizmanto vai nu pirms neapstrādāto datu saglabāšanas, vai arī tā var tikt iekļauta DNG failā, norādot melnās krāsas līmeni.

* **Defektīvi pikseļi**: pirms neapstrādātu datu saglabāšanas kā DNG, defektīvie pikseļi ir jāizslēdz.

* **Metadati**: metadatus var iekļaut DNG jebkurā no šiem veidiem:  

** Izmantojot TIFF-EP vai EXIF metadatu tagus
** Izmantojot IPTC metadatu tagu (33723)
** Izmantojot XMP metadatu tagu (700)
* **Patentēti dati**: parasti piegādātāji iekļauj patentētus datus neapstrādātā failā, ko izmantos viņu pašu pārveidotāji. DNG saglabā savus patentētos datus privātos tagos, privātos IFD un privātā MakerNote. Pārdevējiem ir jāizmanto DNGPrivateData un MakerNoteSafety tagi, lai nodrošinātu, ka lietojumprogrammas, kas rediģē DNG failus, saglabā šos patentētos datus.


Tālāk ir norādīti daži svarīgi TIFF tagu ierobežojumi un paplašinājumi.

**BitsPerSample**

Tiek atbalstīti 8 līdz 32 biti paraugā. Katram paraugam ir jābūt vienādam dziļumam, ja SamplesPerPixel nav vienāds ar 1. Bet, ja BitsPerSample nav vienāds ar 8 vai 16 vai 32, biti ir jāiepako baitos, izmantojot TIFF noklusējuma FillOrder 1 (big-endian).

**Kompresija**

Tiek atbalstītas divas saspiešanas taga vērtības:

* 1. vērtība: nesaspiesti dati.

* 7. vērtība: JPEG saspiesti dati, vai nu bāzes līnijas DCT JPEG, vai bezzudumu JPEG saspiešana.


**Fotometriskā interpretācija**

Tālāk norādītās vērtības tiek atbalstītas tikai sīktēlu un priekšskatījuma IFD.

* 1 = BlackIsZero. Tiek pieņemts, ka tas atrodas gamma 2.2 krāsu telpā.

* 2 = RGB. Tiek pieņemts, ka atrodas sRGB krāsu telpā.

* 6 = YCbCr. Izmanto JPEG kodētiem priekšskatījuma attēliem.


Neapstrādātam IFD tiek atbalstītas šādas vērtības, un tiek pieņemts, ka tās ir kameras sākotnējā krāsu telpa:

* 32803 # CFA (krāsu filtru masīvs).

* 34892 # LinearRaw.


**Orientācija**

Orientācijas tags tiek izmantots failu pārlūkprogrammām, lai tās varētu veikt DNG failu bezzudumu rotāciju. DNG lasītājiem ir jāatbalsta visas iespējamās orientācijas, tostarp spoguļorientācijas.

## Funkcijas jaunākajā DNG versijā

DNG versijai 1.4, 2012. gada oktobrim, ir šādas papildu funkcijas.

* Noklusējuma lietotāja apgriešana

* Caurspīdīgums

* peldošā komata (HDR)

* Zaudēta kompresija

* Starpniekserveri


## Atsauces Nr.

* [DNG specifikācijas — Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0 .0.pdf)

* [Digital Negative — Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)

* [DNG — digitālo kameru neapstrādātu datu publiska arhīva formāts](https://helpx.adobe.com/camera-raw/digital-negative.html)


