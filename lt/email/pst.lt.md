{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PST – „Outlook“ asmeninės informacijos saugyklos failo formatas",
  "description": "Sužinokite apie PST failo formatą ir API, kurios gali kurti ir atidaryti PST failus.",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ps-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra PST failas?

Failai su plėtiniu .pst yra Outlook asmeninės saugyklos failai (taip pat vadinami asmeninės saugyklos lentele), kuriuose saugoma įvairi vartotojo informacija. Vartotojo informacija saugoma įvairių tipų aplankuose, kuriuose yra el. laiškai, kalendoriaus elementai, užrašai, kontaktai ir keli kiti failų formatai. PST failai naudojami archyvuoti el. pašto duomenis neprisijungus, kuriuos vėliau galima įkelti ir peržiūrėti įvairiose programose.

## PST failo formato specifikacijos

Microsoft siūlo PST failo formatą [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) kaip nemokamą ir neatšaukiamą nemokamą patento licenciją pagal Open Specification Promise.

### PST formatų tipas

PST failų formatai skirstomi į du tipus pagal failo tipo kodavimą. ANSI užkoduoti PST failai yra senesni failų formatai ir juos palaiko tik Outlook 2002 ir ankstesnės versijos. Tokie failai turi maksimalų 2 GB (2^^31^^ baitų) dydžio limitą ir nepalaiko Unikodo. Modernesnis failo formato tipas, pagrįstas Unicode kodavimu, pašalina failo dydžio apribojimą ir gali pasiekti maksimalų 50 GB duomenų dydį.

### Loginis PST failo formato organizavimas

PST failo formato pagrindas yra B-Tree, kuris tvarko duomenis ir leidžia atlikti paieškas, nuoseklią prieigą, įterpti, ištrinti ir tt logaritminiu laiku. Bendra PST failo struktūra suskirstyta į tris sluoksnius.

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

Mazgų duomenų bazės (NDB) sluoksnis – mazgų duomenų bazės sluoksnis yra žemesniame PST failo lygyje ir apima mazgų duomenų bazę. Šie mazgai iš tikrųjų yra žemesnio lygio PST failo formato saugyklos. NDB sluoksnį sudaro antraštė, failų paskirstymo informacija, blokai ir BTree (mazgas BTree ir blokas BTree) saugojimo požiūriu. NDB sluoksnio mazgai ir blokai yra susieti per Data BID, kuri yra viena iš keturių mazgo nuorodos ypatybių, ty NID (mazgo ID), pirminio NID, duomenų BID (bloko BID) ir submazgo BID.

Sąrašai, lentelės ir ypatybių sluoksnis – LTP sluoksnis suteikia loginį supratimą apie aukštesnio lygio sąvokas NDB viršuje. Be kitų elementų, LTP sluoksnį daugiausia sudaro Property Context (PC) ir Table Context (TC). PC yra savybių rinkinys, o TC yra dvimatė savybių rinkinio ir jų buvimo matrica. Efektyviai įdiegiant asmeninius kompiuterius ir TC, LTP sluoksnis NDB mazge naudoja šias dviejų tipų duomenų struktūras:

* Heap On Node (HN) – leidžia iš dalies paskirstyti mazgo duomenų srautą į mažus, kintamo dydžio fragmentus.

* BTree on Heap (BTH) – BTH suteikia patogų ir praktišką būdą ieškoti duomenų kompiuteriuose, aprašyti aukščiau, yra realizuojami kaip BTH, todėl yra įgyvendinami statant HN struktūrą.


Pranešimų sluoksnis – šiame sluoksnyje įdiegtos aukštesnio lygio taisyklės ir verslo logika dirbant su PST failais. Šio sluoksnio loginė išvestis yra aplanko objektai, pranešimų objektai, priedų objektai ir ypatybės, o tai įmanoma sujungiant LTP ir NDB sluoksnius. Šiame lygmenyje taip pat apibrėžtos taisyklės ir reikalavimai, kurių reikia laikytis keičiant PST turinį.

### Fizinis PST failo formato organizavimas

Aukštas PST failo failų organizavimo lygis yra toks, kaip parodyta paveikslėlyje žemiau. Tai tik įvairių sąvokų iš loginių PST failo elementų apžvalga.

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### PST antraštės informacija

PST failo HEADER struktūra yra pačioje failo pradžioje su 0 poslinkiu. Jame yra metaduomenų informacija apie PST failą ir ROOT informacija, skirta pasiekti aukščiau aprašytas NDB sluoksnio duomenų struktūras. PST failo formato Unicode ir ANSI versijų HEADER struktūra skiriasi.

Antraštė prasideda 4 baitų magišku žodžiu **!BDN**, vaizduojamu baitais (0x21, 0x42, 0x44, 0x4E). Kitas 2 baitų magiškas skaičius, **SM** (0x53, 0x4D), yra 8 poslinkyje nuo failo pradžios. Versijos informacija (ANSI arba Unicode) yra 10 poslinkis nuo failo pradžios. Hex reikšmė (0x17) nurodo unikodo PST failą, o 0x0E arba 0x0F reiškia ANSI failo formatą.

|Laukas|Aprašymas
---|---|
|dwMagic (4 baitai) | PRIVALO būti {0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPartial (4 baitai) | 471 baito duomenų 32 bitų CRC reikšmė, pradedant nuo wMagicClient (0ffset 0x0008)
|wMagicClient (2 baitai)|PRIVALO būti { 0x53, 0x4D }.
|wVer (2 baitai)|Failo formato versija. Ši vertė PRIVALO būti 14 arba 15, jei failas yra ANSI PST failas, ir PRIVALO būti 23, jei failas yra unikodo PST failas.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Naujo PST failo, pagrįsto šiuo dokumentu, kūrėjai TURI inicijuoti šią reikšmę į 19.
|bPlatformCreate (1 baitas)|Ši reikšmė PRIVALO būti nustatyta į 0x01.
|bPlatformAccess (1 baitas)|Ši reikšmė PRIVALO būti nustatyta į 0x01.
|dwReserved (8 baitai)|
|bidUnused (tik 8 baitai Unicode)|Nenaudojamas užpildas pridėtas, kai buvo sukurtas Unicode PST failo formatas.
|bidNextP (Unikodas: 8 baitai; ANSI: 4 baitai)|Kitas puslapis BID. Puslapiuose yra specialus skaitiklis, skirtas paskirstyti bidIndex reikšmes. Puslapių BID bidIndex vertė priskiriama iš šio skaitiklio.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Daugiau informacijos rasite 2.2.2.2 skyriuje.
|dwUnique (4 baitai)|Tai yra monotoniškai didėjanti reikšmė, kuri keičiama kiekvieną kartą, kai keičiama PST failo HEADER struktūra. Šios reikšmės funkcija yra suteikti unikalią vertę ir užtikrinti, kad po kiekvieno antraštės modifikavimo HEADER CRC būtų kitoks.
|rgnid[] (128 baitai)|Fiksuotas masyvas iš 32 NID, kurių kiekvienas atitinka vieną iš 32 galimų NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_MESSAGE_)
|qwUnused (8 baitai)|Nenaudojama vieta; PRIVALO būti nustatytas į nulį. Tik unikodo PST failo formatas.
|root (Unikodas: 72 baitai; ANSI: 40 baitų)|ROOT struktūra (2.2.2.5 skyrius).
|dwAlign (4 baitai)|Nenaudojami lygiavimo baitai; PRIVALO būti nustatytas į nulį. Tik unikodo PST failo formatas.
|rgbFM (128 baitai)|Nebenaudojamas FMap. Tai nebenaudojama ir PRIVALO būti užpildyta 0xFF. Skaitytojai TURI nekreipti dėmesio į šių baitų reikšmę.
|rgbFP (128 baitai)|Nebenaudojamas FPMap. Tai nebenaudojama ir PRIVALO būti užpildyta 0xFF. Skaitytojai TURI nekreipti dėmesio į šių baitų reikšmę.
|bSentinel (1 baitas) | PRIVALO būti nustatytas į 0x80.
|bCryptMethod (1 baitas)|Nurodo, kaip koduojami PST failo duomenys. PRIVALO būti nustatyta į vieną iš iš anksto nustatytų reikšmių (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbRezervuota (2 baitai)| Rezervuota; PRIVALO būti nustatytas į nulį.
|bidNextB (8 baitai)|Nurodo kitą galimą BID reikšmę. Tik unikodo PST failo formatas.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Daugiau informacijos rasite 2.2.2.2 skyriuje.
|dwCRCFull (4 baitai)|516 baitų duomenų, pradedant nuo wMagicClient iki bidNextB, 32 bitų CRC reikšmė. Tik unikodo PST failo formatas.
|ullReserved (8 baitai)|Rezervuota; PRIVALO būti nustatytas į nulį. Tik ANSI PST failo formatas.
|dwReserved (4 baitai)|Rezervuota; PRIVALO būti nustatytas į nulį. Tik ANSI PST failo formatas.
|rgbReserved2 (3 baitai)|
|bRezervuota (1 baitas) |
|rgbReserved3 (32 baitai) |

### Duomenų apsauga ###

Saugumo sumetimais PST failai taip pat gali būti apsaugoti slaptažodžiu, todėl įkeliama programa turi pritaikyti slaptažodį, kad būtų galima peržiūrėti. PST failui pritaikytas slaptažodis išsaugomas pranešimų saugykloje. Tačiau tai neužtikrina tvirtos duomenų apsaugos, nes slaptažodį galima pašalinti turimais įrankiais. Be to, vartotojo nurodytas slaptažodis nenaudojamas kaip šifravimo algoritmų kodavimo ir dekodavimo rakto dalis. Taigi nėra jokios naudos apsaugoti duomenis, kuriuos turi pasiekti neįgalioti asmenys. Slaptažodžio saugojimas kaip CRC-32 pradinės eilutės maišas taip pat daro jį silpnu duomenų apsaugos nuo brutalios jėgos metodu.

## Nuorodos Nr.

* [Outlook asmeninių aplankų (.pst) failo formatas](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Asmeninio aplanko failo formato specifikacijos](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


