{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Sužinokite apie ABCDDB failo formatą ir API, kurios gali kurti ir atidaryti ABCDDB failus.",
  "title" : "ABCDDB failo formatas – „Apple“ adresų knygos kontaktų sąrašo duomenų bazės failas",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-lt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Kas yra ABCDDB failas?

Failas su plėtiniu **.ABCDDB** reiškia Apple Address Book Contact List Database. Jis priklauso **Adresų knygos** programai, taip pat žinomai kaip **Kontaktai**. Tai integruota programa, įtraukta į iOS ir macOS operacines sistemas. Adresatų programa leidžia vartotojams išsaugoti ir tvarkyti informaciją, susijusią su jų kontaktais, įskaitant asmenis, įmones ir organizacijas. Ši programa leidžia vartotojams sekti informaciją, pvz., vardus, adresus, telefono numerius ir el. pašto adresus, taip pat suskirstyti savo kontaktus į grupes.

## Ryšys su SQLite ir tipiniu keliu

Apple adresų knygelė (taip pat žinoma kaip kontaktai) saugo kontaktinę informaciją kaip vCard metaduomenų aplanke. **Failas _ABCDDB_ iš tikrųjų yra _SQLite 3 duomenų failas_**.

SQLite yra populiari duomenų bazių valdymo sistema, sukurta taip, kad būtų lengva ir savarankiška. Jis naudojamas daugelyje skirtingų tipų programinės įrangos ir įrenginių. SQLite yra RDBVS tipas, ty saugo duomenis lentelėse, kurios yra tarpusavyje susijusios per raktus. Jis gali apdoroti įvairius duomenų tipus, įskaitant sveikuosius skaičius, slankiojo kablelio skaičius, eilutes ir dvejetainius duomenis. Be to, SQLite palaiko operacijas, kurios leidžia vartotojams kartu atlikti kelias duomenų bazės operacijas kaip vieną darbo vienetą.

Failas su ABCDDB plėtiniu paprastai saugomas čia

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Sugadintų kontaktų duomenų bazės taisymas

Prieš bandydami tai padaryti, pirmiausia padarykite atsarginę kopiją. Tada eikite į

~/Biblioteka/Programų palaikymas/Adresų knyga.

Tame kataloge rasite tris failus, įskaitant vieną su plėtiniu .abcddb

- Adresų knyga-v22.abcddb
- Adresų knyga-v22.abcddb-wal.
- Adresų knyga-v22.abcddb-shm.

Ištrinkite visus šiuos failus ir vėl atidarykite kontaktus, jis vėl pradės veikti.

## Atkurkite adresų knygos duomenų bazę iš atsarginės kopijos

Tarkime, jūsų Adresų knygos duomenų bazės kontaktai yra saugomi adresų knygelė-v22.abcddb.

- Pirmiausia sukurkite atsarginę adresų knygos duomenų kopiją ir uždarykite visas programas.
- Perkelkite duomenų bazės failą į `~/Library/Application Support/AddressBook` pakatalogį
- Paleiskite **Address Book.app**.

## Eksportuokite ABCDDB failo duomenis į „Microsoft Access“.

Kadangi failas yra SQLite 3 duomenų failas, galite eksportuoti duomenis iš abcddb failo į Microsoft Access naudodami ODBC jungtį.

SQLite ODBC jungtis yra programinės įrangos biblioteka ir tvarkyklė, leidžianti programoms, palaikančioms ODBC sąsają, prisijungti prie SQLite duomenų bazės. Ji apima biblioteką, apibrėžiančią ODBC sąsają, ir tvarkyklę, kuri šią sąsają paverčia iškvietimais į SQLite API. Norėdami naudoti SQLite ODBC jungtį, pirmiausia turite ją įdiegti, o tada kompiuteryje nustatyti ODBC duomenų šaltinį. Atlikus šiuos veiksmus, bet kuri programa, turinti ODBC palaikymą, galės prisijungti prie duomenų šaltinio ir nuskaityti duomenis iš SQLite duomenų bazės.

## Nuorodos
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Contact Database for Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Kaip atidaryti arba eksportuoti abcddb failą sistemoje Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -Windows-7-Excel)

