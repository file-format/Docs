{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST – Outlook saugyklos failo formatas",
  "description": "Sužinokite apie OST failo formatą ir API, kurios gali kurti ir atidaryti OST failus.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra OST failas?

OST arba neprisijungus pasiekiami saugyklos failai yra vartotojo pašto dėžutės duomenys neprisijungus vietiniame kompiuteryje, registruojantis Exchange Server naudojant Microsoft Outlook. Jis automatiškai sukuriamas pirmą kartą naudojant Microsoft Outlook, kai prisijungiama prie serverio. Sukūrus failą, duomenys sinchronizuojami su el. pašto serveriu, kad būtų pasiekiami neprisijungus, taip pat atsijungus nuo el. pašto serverio. OST failai gali naudoti pašto dėžutės elementus, pvz., el. laiškus, kontaktus, kalendoriaus informaciją, pastabas, užduotis ir kitus panašius duomenis. Vartotojai gali kurti el. laiškus ir kitus duomenų elementus OST faile net ir neprisijungę prie serverio, tačiau jie nebus sinchronizuojami su serveriu. Užmezgus ryšį, vietinis failas vėl sinchronizuojamas su serveriu, kad ir serveris, ir vietinė kopija būtų tame pačiame informacijos lygyje.

## OST failo formatas

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* 32 bitų ANSI formatas

* 64 bitų unikodo formatas


PST failo formatas [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), kurį galima įsigyti iš Microsoft, taip pat taikomas OST failo formatui kaip nemokama ir neatšaukiama patento licencija pagal Atvirosios specifikacijos pažadą. Jį sudaro šie skiriamieji elementai:

* Fle antraštė

* Failo antraštės duomenys

* Indekso šakos mazgas

* Indekso lapo mazgas

* (Failo) poslinkio indeksas

* (Prekės) deskriptoriaus indeksas

* Vietiniai aprašai

* Prekių lentelės tipas


### Antraštės informacija

OST failo HEADER struktūra yra pačioje failo pradžioje su 0 poslinkiu. Jame yra metaduomenų informacija apie OST failą ir ROOT informacija, kad būtų galima pasiekti aukščiau aprašytas NDB sluoksnio duomenų struktūras. OST failo formato Unicode ir ANSI versijų HEADER struktūra skiriasi.

Antraštė prasideda 4 baitų magišku žodžiu **!BDN**, vaizduojamu baitais (0x21, 0x42, 0x44, 0x4E). Kitas 2 baitų magiškas skaičius, **SM** (0x53, 0x4D), yra 8 poslinkyje nuo failo pradžios. Versijos informacija (ANSI arba Unicode) yra 10 poslinkis nuo failo pradžios. Hex reikšmė (0x17) nurodo unikodo OST failą, o 0x0E arba 0x0F reiškia ANSI failo formatą.

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
|dwUnique (4 baitai)|Tai yra monotoniškai didėjanti reikšmė, kuri keičiama kiekvieną kartą, kai keičiama PST failo HEADER struktūra. Šios reikšmės funkcija yra pateikti unikalią vertę ir užtikrinti, kad po kiekvieno antraštės modifikavimo HEADER CRC būtų kitoks.
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

## Nuorodos

* [Outlook asmeninių aplankų (.ost) failo formatas](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Asmeninio aplanko failo formato specifikacijos](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


