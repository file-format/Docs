{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Uzziniet par DSN failu formātu un API, kas var izveidot un atvērt DSN failus.",
  "title" : "DSN faila formāts — datu bāzes avota nosaukuma fails",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-lv",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Kas ir DSN fails?

DSN apzīmē datu avota nosaukums, un tas ir faila formāts, ko izmanto datu bāzes savienojuma informācijas glabāšanai. DSN faili parasti tiek izmantoti kopā ar ODBC (Open Database Connectivity), un tie nodrošina vieglu piekļuvi noteiktai datu bāzei, nodrošinot savienojuma izveidei ar to nepieciešamo informāciju, piemēram, servera nosaukumu, lietotājvārdu un paroli. Fails parasti ir vienkāršs teksts, un to var izveidot un rediģēt, izmantojot teksta redaktoru. To var izmantot dažādās operētājsistēmās, piemēram, Windows, Linux un Mac.

## Kā izveidot DSN failu?

DSN faila izveides metode var atšķirties atkarībā no operētājsistēmas un pieejamajiem rīkiem. Tālāk norādītās darbības sniedz vispārīgu pārskatu par DSN faila izveides procesu Windows sistēmā.

1. Atveriet ODBC datu avota administratoru, sākuma izvēlnē meklējot ODBC datu avoti.
2. Atlasiet cilni Sistēmas DSN un noklikšķiniet uz pogas Pievienot.
3. Izvēlieties atbilstošo draiveri datubāzei, ar kuru vēlaties izveidot savienojumu, un noklikšķiniet uz Pabeigt.
4. Ievadiet nepieciešamo informāciju, lai izveidotu savienojumu ar datu bāzi, piemēram, servera nosaukumu, lietotājvārdu un paroli.
5. Noklikšķiniet uz OK, lai saglabātu DSN failu.

Varat arī izveidot DSN failu manuāli, izveidojot vienkārša teksta failu ar paplašinājumu .dsn un ievadot nepieciešamo savienojuma informāciju šādā formātā:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Pēc tam varat izmantot šī faila ceļu kā DSN savā kodā/skriptā, lai izveidotu savienojumu ar datu bāzi.

## Programmas, kas atver DSN failu

DSN fails ir vienkārša teksta fails, kurā tiek saglabāta informācija, ko izmanto, lai izveidotu savienojumu ar datu bāzi, piemēram, servera nosaukums, lietotājvārds un parole. To parasti izmanto kopā ar ODBC (Open Database Connectivity), lai nodrošinātu vieglu piekļuvi noteiktai datubāzei.

Lai atvērtu un skatītu DSN faila saturu, varat izmantot jebkuru teksta redaktoru, piemēram, Notepad, Sublime Text, Atom u.c. Šīs programmas ļaus atvērt DSN failu un skatīt tajā saglabāto savienojuma informāciju.

Tomēr, lai izmantotu DSN failu, lai izveidotu savienojumu ar datu bāzi un izpildītu tādas darbības kā SELECT, INSERT, UPDATE, DELETE utt., Programma ar ODBC atbalstu, piemēram, programmēšanas valoda, piemēram, Python, Java, C# vai datu bāzes pārvaldības rīks, piemēram, Microsoft Access. , ir nepieciešama SQL Server Management Studio. Šīs programmas var izmantot DSN failā esošo informāciju, lai izveidotu savienojumu ar datu bāzi un veiktu vēlamo darbību.

## Atsauces

* [Kas ir DSN (datu avota nosaukums)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



