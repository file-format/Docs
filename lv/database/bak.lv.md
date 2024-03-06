{
  "date": "2020-11-11",
  "keywords": [
"BAK",
"pagarinājumu",
"failu",
"faila formātā",
"BAK faila tips",
"BAK faila paplašinājums",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par BAK faila formātu un API, kas var izveidot un atvērt BAK failus.",
  "title": "BAK faila formāts — datu bāzes dublējuma fails",
  "linktitle": "BAK",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ba-lvk"
}
},
  "lastmod": "2020-12-04"
}

## Kas ir BAK fails?

Fails ar paplašinājumu .bak parasti ir dublējuma fails, ko izmanto dažādi programmatūras rīki, lai saglabātu datu dublējumus. No datu bāzes viedokļa Microsoft SQL Server izmanto BAK failu datu bāzes satura glabāšanai. Visi ar datu bāzi saistītie dati un faili tiek glabāti šajā faila formātā, lai tos varētu izgūt gadījumā, ja datubāze kāda iemesla dēļ var kļūt bojāta vai nederīga. Drošības nolūkos dublējuma failus var glabāt un indeksēt citos serveros. Vairākas lietojumprogrammas var izveidot BAK failus, piemēram, SQL Server Management Studio, Transact-SQL un Windows PowerShell.

## BAK faila formāts

BAK faila iekšējā informācija nav zināma, taču tiek plaši pieņemts, ka tas ir balstīts uz Microsoft lentes formātu (MTF). Ir pieejamas MTF specifikācijas, uz kurām var atsaukties, lai izprastu faila struktūru. Dokumentā ir sniegta informācija par MTF krātuvi ikvienam, kam ir vispārīgas zināšanas par krātuves pārvaldības darbībām, lentes diskdziņiem un failu sistēmām.

### Datu kopas

Datu kopa ir objektu kopums, kas ierakstīts datu nesējā (lentē, optiskajā diskā utt.) datu dublēšanas vai atjaunošanas laikā. Datu kopas sastāv no vairākiem datu nesējiem liela datu apjoma gadījumā.

### Daudzpusējās tirdzniecības sistēmas pamatelementi

MTF fails sastāv no dažiem pamatelementiem, kas veido tā pamatelementus. Šie elementi ir:

#### Deskriptoru bloki

Deskriptoru bloki (DBLK) tiek izmantoti formāta kontrolei un veido MTF faila primāros pamatus. Viens MTF fails definē vairākus DBLK katrai unikālajai lomai. Katrs DBLK ir mainīga garuma datu bloks, kas ir sadalīts šādās četrās daļās:

 * Common Block Header — fiksēta garuma struktūra, kas ir kopīga visiem DBLK. Šī ir vienīgā nepieciešamā bloka galvene.
 * `DBLK tipa informācija` — fiksēta garuma bloks, kas ir raksturīgs definējamā DBLK tipam
 * Operētājsistēmas dati — konkrēti dati, kas definēti, pamatojoties uz DBLK un operētājsistēmu veidu
 * DBLK informācija — mainīga garuma DBLK specifiska informācija, ko nevar saglabāt, izmantojot fiksēta garuma DBLK informāciju.

{{< figure src=../bak.png alt=Microsoft SQL dublējuma faila formāts >}}

#### Datu straume

Datu straumes MTF failā tiek izmantotas datu iekapsulēšanai un izlīdzināšanai. Tas sastāv no straumes galvenes, kam seko straumes dati. Straumes galvenē var ietvert tikai viena veida straumes datus.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL dublējuma faila formāts" >}}

#### FileMarks

Faila atzīme tiek izmantota loģiskai atdalīšanai un ātrai piekļuvei multividei. Failu atzīmes emulē ierīces draiveris vai Soft Filemark Descriptor bloks, ja izmantotā ierīce nenodrošina failu atzīmes.

## Citi BAK faili

Šeit ir citi failu tipi, kas izmanto faila paplašinājumu **.bak**.

**Datu bāze**
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)
- [BAK - Microsoft SQL Server Database Backup](/database/bak-sqlserver/)

**Spēle**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Dažādi**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Iestatījumi**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## Atsauces Nr.

* [[MS-BCP]: lielapjoma kopēšanas formāts](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)


