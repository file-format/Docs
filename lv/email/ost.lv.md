{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST — Outlook krātuves faila formāts",
  "description": "Uzziniet par OST faila formātu un API, kas var izveidot un atvērt OST failus.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir OST fails?

OST vai bezsaistes krātuves faili ir lietotāja pastkastes dati bezsaistes režīmā vietējā datorā, reģistrējoties Exchange Server, izmantojot Microsoft Outlook. Tas tiek automātiski izveidots, pirmo reizi lietojot Microsoft Outlook, kad tiek izveidots savienojums ar serveri. Kad fails ir izveidots, dati tiek sinhronizēti ar e-pasta serveri, lai tie būtu pieejami bezsaistē, kā arī atvienošanas gadījumā no e-pasta servera. OST faili var izmantot pastkastes vienumus, piemēram, e-pastus, kontaktpersonas, kalendāra informāciju, piezīmes, uzdevumus un citus līdzīgus datus. Lietotāji var izveidot e-pastus un citus datu vienumus OST failā pat tad, ja nav savienojuma ar serveri, taču tie netiks sinhronizēti ar serveri. Kad savienojums ir izveidots, lokālais fails atkal tiek sinhronizēts ar serveri, lai gan serveris, gan lokālā kopija atrastos vienā informācijas līmenī.

## OST faila formāts

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* 32 bitu ANSI formāts

* 64 bitu unikoda formāts


PST faila formāts [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), kas pieejams no Microsoft, ir piemērojams arī OST faila formātam kā bezmaksas un neatsaucama patenta licence saskaņā ar Open Specification Promise. Tas sastāv no šādiem atšķirīgiem elementiem:

* Fle galvene

* Faila galvenes dati

* Indeksa filiāles mezgls

* Indeksa lapas mezgls

* (Faila) nobīdes indekss

* (Preces) deskriptora indekss

* Vietējie deskriptori

* Preču tabulas veids


### Galvenes informācija

OST faila HEADER struktūra atrodas faila pašā sākumā ar 0 nobīdi. Tajā ir ietverta metadatu informācija par OST failu un ROOT informācija, lai piekļūtu iepriekš aprakstītajām NDB slāņa datu struktūrām. HEADER struktūra atšķiras OST faila formāta Unicode un ANSI versijām.

Galvene sākas ar 4 baitu burvju vārdu **!BDN**, ko attēlo baiti (0x21, 0x42, 0x44, 0x4E). Vēl viens 2 baitu burvju skaitlis — **SM** (0x53, 0x4D) atrodas 8. nobīdē no faila sākuma. Informācija par versiju (ANSI vai Unicode) atrodas ar nobīdi 10 no faila sākuma. Hex vērtība (0x17) norāda unikoda OST failu, savukārt 0x0E vai 0x0F apzīmē ANSI faila formātu.

|Lauks|Apraksts
---|---|
|dwMagic (4 baiti)|JĀBŪT {0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPartial (4 baiti)|32 bitu CRC vērtība 471 baita datiem, sākot no wMagicClient (0ffset 0x0008)
|wMagicClient (2 baiti)|JĀBŪT {0x53, 0x4D }.
|wVer (2 baiti)|Faila formāta versija. Šai vērtībai OBLIGĀTI ir 14 vai 15, ja fails ir ANSI PST fails, un OBLIGĀTI ir 23, ja fails ir unikoda PST fails.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Jauna PST faila veidotājiem, kuru pamatā ir šis dokuments, BŪTU inicializējusi šo vērtību uz 19.
|bPlatformCreate (1 baits)|Šī vērtība OBLIGĀTI jāiestata uz 0x01.
|bPlatformAccess (1 baits)|Šī vērtība OBLIGĀTI jāiestata uz 0x01.
|dwReserved (8 baiti)|
|bidUnused (tikai 8 baiti Unicode)|Nelietots polsterējums ir pievienots, kad tika izveidots Unicode PST faila formāts.
|bidNextP (Unicode: 8 baiti; ANSI: 4 baiti)|Nākamā lapa BID. Lapās ir īpašs skaitītājs bidIndex vērtību piešķiršanai. No šī skaitītāja tiek piešķirta bidIndex vērtība lapu BID.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Sīkāku informāciju skatiet 2.2.2.2. sadaļā.
|dwUnique (4 baiti)|Šī ir monotoni pieaugoša vērtība, kas tiek mainīta katru reizi, kad tiek mainīta PST faila HEADER struktūra. Šīs vērtības funkcija ir nodrošināt unikālu vērtību un nodrošināt, ka HEADER CRC atšķiras pēc katras galvenes modifikācijas.
|rgnid[] (128 baiti)|Fiksēts masīvs ar 32 NID, katrs atbilst vienam no 32 iespējamajiem NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_MESSAGE_)
|qwUnused (8 baiti)|Neizmantota vieta; OBLIGĀTI jāiestata uz nulli. Tikai unikoda PST faila formāts.
|sakne (Unikods: 72 baiti; ANSI: 40 baiti) | ROOT struktūra (2.2.2.5. sadaļa).
|dwAlign (4 baiti)|Nelietoti līdzināšanas baiti; OBLIGĀTI jāiestata uz nulli. Tikai unikoda PST faila formāts.
|rgbFM (128 baiti)|Novecojusi FMap. Tas vairs netiek izmantots un OBLIGĀTI jāaizpilda ar 0xFF. Lasītājiem BŪTU JĀŅEMIET vērā šo baitu vērtība.
|rgbFP (128 baiti)|Novecojusi FPMap. Tas vairs netiek izmantots un OBLIGĀTI jāaizpilda ar 0xFF. Lasītājiem BŪTU JĀŅEMIET vērā šo baitu vērtība.
|bSentinel (1 baits) | OBLIGĀTI jāiestata uz 0x80.
|bCryptMethod (1 baits)|Norāda, kā tiek kodēti dati PST failā. OBLIGĀTI jāiestata uz kādu no iepriekš definētajām vērtībām (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbRezervēts (2 baiti)| Rezervēts; OBLIGĀTI jāiestata uz nulli.
|bidNextB (8 baiti)|Norāda nākamo pieejamo BID vērtību. Tikai unikoda PST faila formāts.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Sīkāku informāciju skatiet 2.2.2.2. sadaļā.
|dwCRCFull (4 baiti)|32 bitu CRC vērtība 516 baitiem datiem, sākot no wMagicClient līdz bidNextB, ieskaitot. Tikai unikoda PST faila formāts.
|ullReserved (8 baiti)|Rezervēts; OBLIGĀTI jāiestata uz nulli. Tikai ANSI PST faila formāts.
|dwReserved (4 baiti)|Rezervēts; OBLIGĀTI jāiestata uz nulli. Tikai ANSI PST faila formāts.
|rgbReserved2 (3 baiti)|
|bRezervēts (1 baits) |
|rgbReserved3 (32 baiti) |

## Atsauces

* [Outlook personisko mapju (.ost) faila formāts](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Personīgo mapju faila formāta specifikācijas](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


