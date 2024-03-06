{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Uzziniet par ABCDDB faila formātu un API, kas var izveidot un atvērt ABCDDB failus.",
  "title" : "ABCDDB faila formāts — Apple adrešu grāmatas kontaktu saraksta datu bāzes fails",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-lv",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Kas ir ABCDDB fails?

Fails ar paplašinājumu **.ABCDDB** apzīmē Apple Address Book Contact List Database. Tas pieder lietojumprogrammai **Adrešu grāmata**, kas pazīstama arī kā **Kontakti**. Tā ir iebūvēta lietojumprogramma, kas ir iekļauta iOS un macOS operētājsistēmās. Lietojumprogramma Kontakti ļauj lietotājiem saglabāt un sakārtot informāciju, kas saistīta ar viņu kontaktpersonām, tostarp personām, uzņēmumiem un organizācijām. Šī lietotne ļauj lietotājiem sekot līdzi informācijai, piemēram, vārdiem, adresēm, tālruņu numuriem un e-pasta adresēm, kā arī klasificēt savus kontaktus grupās.

## Saistība ar SQLite un tipisko ceļu

Apple adrešu grāmata (pazīstama arī kā kontaktpersonas) saglabā kontaktinformāciju kā vCards metadatu mapē. **Fails _ABCDDB_ faktiski ir _SQLite 3 datu fails_**.

SQLite ir populāra datu bāzes pārvaldības sistēma, kas ir izstrādāta tā, lai tā būtu viegla un autonoma. To izmanto dažāda veida programmatūrā un ierīcēs. SQLite ir RDBMS veids, kas nozīmē, ka tas saglabā datus tabulās, kas ir saistītas viena ar otru, izmantojot atslēgas. Tas var apstrādāt dažādus datu tipus, tostarp veselus skaitļus, peldošā komata skaitļus, virknes un bināros datus. Turklāt SQLite atbalsta transakcijas, kas lietotājiem ļauj veikt vairākas datu bāzes darbības kopā kā vienu darba vienību.

Fails ar ABCDDB paplašinājumu parasti tiek glabāts šeit

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Bojātu kontaktpersonu datu bāzes labošana

Pirms mēģināt to izdarīt, lūdzu, vispirms izveidojiet dublējumu. Pēc tam, lūdzu, dodieties uz

`~/Bibliotēka/Lietojumprogrammu atbalsts/Adrešu grāmata`

Šajā direktorijā atradīsit trīs failus, tostarp vienu ar paplašinājumu .abcddb

- Addressbook-v22.abcddb
- Addressbook-v22.abcddb-wal
- Addressbook-v22.abcddb-shm

Izdzēsiet visus šos failus un atkārtoti atveriet sadaļu Kontakti, tas atsāks darboties.

## Atjaunojiet adrešu grāmatas datu bāzi no dublējuma

Pieņemsim, ka jūsu adrešu grāmatas datu bāzes kontaktpersonas tiek glabātas `addressbook-v22.abcddb`.

- Vispirms dublējiet adrešu grāmatas datus un aizveriet visas lietojumprogrammas.
- Pārvietojiet datu bāzes failu uz apakšdirektoriju ~/Library/Application Support/AddressBook
- Palaidiet **Address Book.app**.

## Eksportējiet ABCDDB faila datus uz Microsoft Access

Tā kā fails ir SQLite 3 datu fails, varat eksportēt abcddb faila datus programmā Microsoft Access, izmantojot ODBC savienotāju.

SQLite ODBC savienotājs ir programmatūras bibliotēka un draiveris, kas ļauj lietojumprogrammām, kas atbalsta ODBC saskarni, izveidot savienojumu ar SQLite datu bāzi. Tajā ir iekļauta bibliotēka, kas definē ODBC saskarni, un draiveris, kas šo saskarni pārvērš izsaukumos uz SQLite API. Lai izmantotu SQLite ODBC savienotāju, vispirms tas ir jāinstalē un pēc tam datorā jāiestata ODBC datu avots. Pēc šo darbību veikšanas jebkura lietojumprogramma, kas ir aprīkota ar ODBC atbalstu, varēs izveidot savienojumu ar datu avotu un izgūt datus no SQLite datu bāzes.

## Atsauces
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Mac kontaktpersonu datu bāze](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Kā es varu atvērt vai eksportēt abcddb failu programmā Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -Windows-7-Excel)

