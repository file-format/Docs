{
  "date": "2019-10-11",
  "keywords": [
"bmp failu",
"bmp faila formātā",
"kas ir bmp fails",
"failu",
"bmp piemērs",
"bmp faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "BMP - attēla faila formāts",
  "description": "Uzziniet par BMP failu formātu un API, kas var izveidot un atvērt BMP failus.",
  "linktitle": "BMP",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-bm-lvp"
}
},
  "lastmod": "2019-09-10"
}

# Kas ir BMP fails? #

Faili ar paplašinājumu .BMP ir bitkartes attēlu faili, kas tiek izmantoti, lai saglabātu bitkartes digitālos attēlus. Šie attēli ir neatkarīgi no grafikas adaptera un tiek saukti arī par ierīces neatkarīgo bitkartes (DIB) faila formātu. Šī neatkarība kalpo faila atvēršanai vairākās platformās, piemēram, Microsoft Windows un Mac. BMP faila formāts var saglabāt datus kā divdimensiju digitālos attēlus gan vienkrāsainos, gan krāsu formātos ar dažādu krāsu dziļumu.

## BMP faila formāta specifikācijas ##

No ierīces neatkarīgās bitkartes darbojas kā palīglīdzeklis, lai apmainītos ar bitkartēm starp ierīcēm un lietojumprogrammām. Šī faila formāta nepārtrauktas attīstības dēļ galvenēs esošā informācija var atšķirties atkarībā no Bitmap versijas. Viens bitkartes fails sastāv no fiksētām, kā arī mainīga izmēra struktūrām noteiktā secībā.

Struktūras bitkartes failā ir sakārtotas šādā secībā:


|Struktūra|Izvēles|Izmērs|Mērķis
---|---|---|---|
|Faila galvene|Nē|14|Lai saglabātu vispārīgu informāciju par bitkartes attēla failu
|DIB galvene|Nē|Fiksēta izmēra|Lai saglabātu detalizētu informāciju par bitkartes attēlu un definētu pikseļu formātu
|Papildu bitu maskas|Jā|12 vai 16 baiti|Lai definētu pikseļu formātu
|Krāsu palete|Daļēji pēc izvēles|Mainīgs izmērs|Lai definētu krāsas, ko izmanto bitkartes attēla dati
|Gap1|Jā|Mainīga izmēra|Struktūras izlīdzināšana
|Pixel Array|No|Variable-size|Pikseļu formātu nosaka DIB galvene vai papildu bitu maskas.
|Gap2|Jā|Mainīga izmēra|Struktūras izlīdzināšana
|ICC Color profile|Yes|Variable-size|Lai definētu krāsu profilu krāsu pārvaldībai

Kad bitkartes attēls tiek ielādēts atmiņā, tas kļūst par DIB struktūru, ko Windows izmanto, izmantojot savu GDI API. Faila galvene neietilpst šajā datu struktūrā. Krāsa var sastāvēt arī no 16 bitu ierakstiem, kas veido indeksus pašreiz norādītajai paletei, nevis precīzām RGB krāsu definīcijām. Apskatīsim dažus no tiem sīkāk, jo īpaši galvenes.

### Bitkartes faila galvene ###

Bitkartes faila galvene ir līdzīga citām failu galvenēm, ko izmanto faila identificēšanai. Tā kā BMP faila formātam ir dažādi varianti, pirmie 2 BMP faila formāta baiti ir rakstzīme B un pēc tam rakstzīme M ASCII kodējumā. Visas veselu skaitļu vērtības tiek saglabātas mazā formātā.

|Nobīde hex|Nobīde dec|Izmērs|Mērķis
---|---|---|---|
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** — OS/2 struktūras bitkartes masīvs * **CI** — OS/2 struktūras krāsu ikona * **CP** — OS/2 konst. krāsu rādītājs * **IC** — OS/2 struktūras ikona * **PT** — OS/2 rādītājs
|02|2|4 baiti|BMP faila lielums baitos
|06|6|2 baiti|Rezervēts; faktiskā vērtība ir atkarīga no lietojumprogrammas, kas izveido attēlu
|08|8|2 baiti|Rezervēts; faktiskā vērtība ir atkarīga no lietojumprogrammas, kas izveido attēlu
|0A|10|4 baiti|Baita nobīde, ti, sākuma adrese, kurā var atrast bitkartes attēla datus (pikseļu masīvu).

#### DIB galvene (bitkartes informācijas galvene) ####

Sīkāka informācija par attēlu ir attēlota šajā galvenē. Pamatojoties uz šo informāciju, tiks noteikta lietojumprogramma, kas tiks izmantota attēla parādīšanai ekrānā. Visās šādās galvenēs ir DWORD (32 bitu) lauks, norādot to lielumu, lai lietojumprogramma varētu viegli noteikt attēlā izmantoto galveni. Tas galvenokārt ir saistīts ar faktu, ka DIB formātam tika veikti vairāki paplašinājumi. Tālāk ir norādīta DIB galvene ar uzskaitītajiem laukiem.

#### Krāsu palete ####

BMP krāsu palete ir struktūru masīvs, kas norāda katras krāsas RGB intensitātes vērtības displeja ierīces krāsu paletē. Katrs bitkartes datu pikselis saglabā vienu vērtību, kas tiek izmantota kā indekss krāsu paletē. Informācija par krāsu, kas saglabāta elementā šajā indeksā, norāda šī pikseļa krāsu. Krāsu pieejamība bitkartes failā atšķiras šādi:

* Viens, 4 un 8 biti — paredzēts vienmēr saturēt krāsu paleti

* Sešpadsmit, 24 un 32 bitu — nekad nesatur krāsu paletes

* Sešpadsmit un 32 bitu BMP faili — krāsu paletes vietā satur bitlauku maskas vērtības


#### Pikseļu krātuve ####

Bitkartes pikseļi tiek saglabāti kā biti, kas iepakoti rindās, kur katras rindas lielums tiek noapaļots līdz 4 baitiem (32 bitu DWORD), izmantojot pildījumu. Kopējo baitu daudzumu, kas nepieciešams attēla pikseļu glabāšanai, nevar tieši aprēķināt, tikai saskaitot bitus. Tā kā tiek izmantots polsterējums, katras rindas lielums ir jānoapaļo līdz 4 baitiem. Aizpildīšanas baiti (ne vienmēr 0) ir jāpievieno rindu beigām, lai rindu garums tiktu palielināts līdz četriem baitiem. Kad pikseļu masīvs tiek ielādēts atmiņā, katrai rindai jāsākas ar atmiņas adresi, kas ir 4 reizes.

Attēlu faktiski apraksta pikseļu masīva 32 bitu DWORD attēlojums. Parasti pikseļi tiek glabāti no apakšas uz augšu, sākot no apakšējā kreisā stūra, virzoties no kreisās puses uz labo un pēc tam rindu pa rindu no attēla apakšas uz augšu. Tālāk ir norādīti pikseļu formāti un to nozīme.

* 1 bits uz pixel (1 bpp) formāts atbalsta 2 atšķirīgas krāsas (piemēram, melnbaltu).

* 2 bitu uz pikseļu (2 bpp) formāts atbalsta 4 atšķirīgas krāsas un saglabā 4 pikseļus uz 1 baitu, un kreisais pikselis atrodas divos nozīmīgākajos bitos. Katra pikseļa vērtība ir 2 bitu indekss tabulā līdz 4 krāsām.

* 4 bitu uz pikseļu (4 bpp) formāts atbalsta 16 atšķirīgas krāsas un saglabā 2 pikseļus uz 1 baitu, un kreisais galējais pikselis atrodas nozīmīgākajā daļā. Katra pikseļa vērtība ir 4 bitu indekss tabulā līdz 16 krāsām.

* 8 bitu uz pikseļu (8 bpp) formāts atbalsta 256 atšķirīgas krāsas un saglabā 1 pikseļu uz 1 baitu. Katrs baits ir indekss tabulā līdz 256 krāsām.

* 16 bitu uz pikseļu (16 bpp) formāts atbalsta 65 536 atšķirīgas krāsas un saglabā 1 pikseļu uz 2 baitu WORD. Katrs VĀRDS var definēt pikseļa alfa, sarkano, zaļo un zilo paraugu.

* 24 bitu pikseļu (24 bpp) formāts atbalsta 16 777 216 atšķirīgas krāsas un saglabā 1 pikseļa vērtību uz 3 baitiem. Katra pikseļa vērtība nosaka pikseļa sarkano, zaļo un zilo paraugu (8.8.8.0.0 RGBAX apzīmējumā). Konkrēti, secībā: zils, zaļš un sarkans (8 biti katrā paraugā).

* 32 bitu uz pikseļu (32 bpp) formāts atbalsta 4 294 967 296 atšķirīgas krāsas un saglabā 1 pikseļu uz 4 baitu DWORD. Katrs DWORD var definēt pikseļa alfa, sarkano, zaļo un zilo paraugu.


## Atsauces Nr.

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP faila formāts](https://en.wikipedia.org/wiki/BMP_file_format)


