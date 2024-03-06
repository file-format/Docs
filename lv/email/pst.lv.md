{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PST — Outlook personiskās informācijas krātuves faila formāts",
  "description": "Uzziniet par PST faila formātu un API, kas var izveidot un atvērt PST failus.",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ps-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir PST fails?

Faili ar paplašinājumu .pst ir Outlook personiskās krātuves faili (saukti arī par personīgo krātuves tabulu), kuros tiek glabāta dažāda lietotāja informācija. Lietotāja informācija tiek glabāta dažāda veida mapēs, kas ietver e-pastus, kalendāra vienumus, piezīmes, kontaktus un vairākus citus failu formātus. PST faili tiek izmantoti e-pasta datu arhivēšanai bezsaistē, ko vēlāk var ielādēt un skatīt dažādās lietojumprogrammās.

## PST faila formāta specifikācijas

PST faila formāts [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) ir pieejams korporācijā Microsoft kā bezmaksas un neatsaucama bezmaksas patentu licence, izmantojot Open Specification Promise.

### PST formātu veids

PST failu formāti ir iedalīti divos veidos, pamatojoties uz faila tipa kodējumu. ANSI kodētie PST faili ir vecāki failu formāti, un tos atbalsta tikai Outlook 2002 un vecākas versijas. Šādu failu maksimālais lieluma ierobežojums ir 2 GB (2^^31^^ baiti), un tie neatbalsta Unicode. Mūsdienīgāks faila formāta veids, kura pamatā ir Unicode kodējums, novērš faila lieluma ierobežojumu un var sasniegt maksimālo datu lielumu 50 GB.

### PST faila formāta loģiskā organizācija

PST faila formāta pamatā ir B-Tree, kas saglabā datu kārtošanu un ļauj logaritmiskā laikā meklēt, secīgu piekļuvi, ievietošanu, dzēšanu utt. PST faila kopējā struktūra ir sakārtota trīs slāņos.

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

Mezglu datu bāzes (NDB) slānis — mezglu datu bāzes slānis atrodas PST faila zemākajā līmenī un ietver mezglu datu bāzi. Šie mezgli faktiski ir zemāka līmeņa PST faila formāta krātuves iespējas. NDB slānis sastāv no galvenes, failu piešķiršanas informācijas, blokiem un BTrees (Node BTree un Block BTree) no krātuves viedokļa. NDB slāņa mezgli un bloki ir saistīti, izmantojot datu BID, kas ir viens no četriem mezgla atsauces rekvizītiem, ti, NID (mezgla ID), mātes NID, datu BID (bloka BID) un apakšmezgla BID.

Saraksti, tabulas un rekvizītu slānis - LTP slānis nodrošina loģisku izpratni par augstāka līmeņa jēdzieniem papildus NDB. Papildus citiem elementiem LTP slānis galvenokārt sastāv no īpašuma konteksta (PC) un tabulas konteksta (TC). PC ir īpašību kopums, savukārt TC ir rekvizītu kolekcijas un to klātbūtnes divdimensiju matrica. Efektīva personālo datoru un TC ieviešana, LTP slānis izmanto šādu divu veidu datu struktūras NDB mezglā:

* Heap On Node (HN) — ļauj sadalīt mezgla datu plūsmu mazos, mainīga izmēra fragmentos.

* BTree on Heap (BTH) - BTH nodrošina ērtu un praktisku veidu, kā meklēt datu datoros, kas aprakstīti iepriekš, tiek realizēti kā BTH, un tāpēc tas tiek ieviests, veidojot HN struktūru.


`Ziņojumapmaiņas slānis -` Šajā slānī ir ieviesti augstāka līmeņa noteikumi un biznesa loģika darbam ar PST failiem. Šī slāņa loģiskā izvade tiek iegūta kā mapju objekti, ziņojumu objekti, pielikuma objekti un rekvizīti, kas ir iespējams, apvienojot LTP un NDB slāņus. Šajā slānī ir definēti arī noteikumi un prasības, kas jāievēro, mainot PST saturu.

### PST faila formāta fiziskā organizācija

Augsts PST faila failu organizācijas līmenis ir tāds, kā parādīts zemāk esošajā attēlā. Šis ir tikai pārskats par dažādiem jēdzieniem no PST faila loģiskajiem elementiem.

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### PST galvenes informācija

PST faila HEADER struktūra atrodas faila pašā sākumā ar 0 nobīdi. Tajā ir ietverta metadatu informācija par PST failu un ROOT informācija, lai piekļūtu iepriekš aprakstītajām NDB slāņa datu struktūrām. PST faila formāta Unikoda un ANSI versijām HEADER struktūra atšķiras.

Galvene sākas ar 4 baitu burvju vārdu **!BDN**, ko attēlo baiti (0x21, 0x42, 0x44, 0x4E). Vēl viens 2 baitu burvju skaitlis — **SM** (0x53, 0x4D) atrodas 8. nobīdē no faila sākuma. Informācija par versiju (ANSI vai Unicode) atrodas ar nobīdi 10 no faila sākuma. Hex vērtība (0x17) norāda unikoda PST failu, savukārt 0x0E vai 0x0F apzīmē ANSI faila formātu.

|Lauks|Apraksts
---|---|
|dwMagic (4 baiti)|JĀBŪT {0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPartial (4 baiti)|32 bitu CRC vērtība 471 baita datiem, sākot no wMagicClient (0ffset 0x0008)
|wMagicClient (2 baiti)|JĀBŪT {0x53, 0x4D }.
|wVer (2 baiti)|Faila formāta versija. Šai vērtībai OBLIGĀTI ir 14 vai 15, ja fails ir ANSI PST fails, un OBLIGĀTI ir 23, ja fails ir unikoda PST fails.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Jauna PST faila veidotājiem, kuru pamatā ir šis dokuments, BŪTU inicializējusi šo vērtību uz 19.
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

### Datu aizsardzība ###

Drošības nolūkos PST failus var arī aizsargāt ar paroli, tāpēc ielādes lietojumprogrammai ir jāpiemēro parole, pirms to var skatīt. PST failam lietotā parole tiek saglabāta ziņojumu krātuvē. Tomēr tas nenodrošina spēcīgu datu aizsardzību, jo paroli var noņemt, izmantojot pieejamos rīkus. Arī lietotāja norādītā parole netiek izmantota kā daļa no atslēgas kodēšanas un dekodēšanas šifrēšanas algoritmiem. Tādējādi nav nekādu labumu no datu aizsardzības, kuriem nevar piekļūt nesankcionētas personas. Paroles glabāšana kā sākotnējās virknes CRC-32 jaucējvārds arī padara to par vāju metodi datu drošībai pret brutālu spēku pieeju.

## Atsauces Nr.
* [Outlook personisko mapju (.pst) faila formāts](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Personīgo mapju faila formāta specifikācijas](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
