{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Sužinokite apie DSN failo formatą ir API, kurios gali kurti ir atidaryti DSN failus.",
  "title" : "DSN failo formatas – duomenų bazės šaltinio pavadinimo failas",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-lt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Kas yra DSN failas?

DSN reiškia duomenų šaltinio pavadinimą ir yra failo formatas, naudojamas duomenų bazės ryšio informacijai saugoti. DSN failai paprastai naudojami kartu su ODBC (Open Database Connectivity) ir leidžia lengvai pasiekti konkrečią duomenų bazę, pateikiant reikiamą informaciją, kad būtų galima prie jos prisijungti, pvz., serverio pavadinimą, vartotojo vardą ir slaptažodį. Failas paprastai yra paprasto teksto, jį galima sukurti ir redaguoti naudojant teksto rengyklę. Jis gali būti naudojamas įvairiose operacinėse sistemose, tokiose kaip Windows, Linux ir Mac.

## Kaip sukurti DSN failą?

DSN failo kūrimo būdas gali skirtis priklausomai nuo operacinės sistemos ir turimų įrankių. Šie veiksmai pateikia bendrą DSN failo kūrimo proceso Windows sistemoje apžvalgą.

1. Atidarykite ODBC duomenų šaltinio administratorių pradiniame meniu ieškodami ODBC duomenų šaltiniai.
2. Pasirinkite skirtuką Sistemos DSN ir spustelėkite mygtuką Pridėti.
3. Pasirinkite tinkamą duomenų bazės, prie kurios norite prisijungti, tvarkyklę ir spustelėkite Baigti.
4. Įveskite reikalingą informaciją, kad prisijungtumėte prie duomenų bazės, pvz., serverio pavadinimą, vartotojo vardą ir slaptažodį.
5. Spustelėkite Gerai, kad išsaugotumėte DSN failą.

Arba galite sukurti DSN failą rankiniu būdu, sukurdami paprasto teksto failą su plėtiniu .dsn ir įvesdami reikiamą ryšio informaciją tokiu formatu:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Tada galite naudoti šio failo kelią kaip DSN savo kode / scenarijuje, kad prisijungtumėte prie duomenų bazės.

## Programos, atidarančios DSN failą

DSN failas yra paprasto teksto failas, kuriame saugoma informacija, naudojama prisijungti prie duomenų bazės, pvz., serverio pavadinimas, vartotojo vardas ir slaptažodis. Paprastai jis naudojamas kartu su ODBC (Open Database Connectivity), kad būtų galima lengvai pasiekti konkrečią duomenų bazę.

Norėdami atidaryti ir peržiūrėti DSN failo turinį, galite naudoti bet kurį teksto rengyklę, pvz., Notepad, Sublime Text, Atom ir kt. Šios programos leis jums atidaryti DSN failą ir peržiūrėti jame saugomą ryšio informaciją.

Tačiau norint naudoti DSN failą prisijungti prie duomenų bazės ir atlikti tokias operacijas kaip SELECT, INSERT, UPDATE, DELETE ir tt, programa su ODBC palaikymu, pvz., programavimo kalba, pvz., Python, Java, C# arba duomenų bazės valdymo įrankis, pvz., Microsoft Access. , reikalinga SQL Server Management Studio. Šios programos gali naudoti DSN faile esančią informaciją, kad prisijungtų prie duomenų bazės ir atliktų pageidaujamą operaciją.

## Nuorodos

* [Kas yra DSN (duomenų šaltinio pavadinimas)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



