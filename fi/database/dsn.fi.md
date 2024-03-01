{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi DSN-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DSN-tiedostoja.",
  "title" : "DSN-tiedostomuoto - Tietokannan lähteen nimitiedosto",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-fi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Mikä on DSN-tiedosto?

DSN on lyhenne sanoista Data Source Name ja se on tiedostomuoto, jota käytetään tietokantayhteystietojen tallentamiseen. DSN-tiedostoja käytetään yleensä yhdessä ODBC:n (Open Database Connectivity) kanssa, ja ne mahdollistavat helpon pääsyn tiettyyn tietokantaan antamalla siihen yhteyden muodostamiseen tarvittavat tiedot, kuten palvelimen nimen, käyttäjätunnuksen ja salasanan. Tiedosto on yleensä pelkkää tekstiä, ja se voidaan luoda ja muokata tekstieditorilla. Sitä voidaan käyttää useissa käyttöjärjestelmissä, kuten Windows, Linux ja Mac.

## Kuinka luoda DSN-tiedosto?

DSN-tiedoston luontitapa voi vaihdella käyttöjärjestelmän ja käytettävissä olevien työkalujen mukaan. Seuraavat vaiheet tarjoavat yleiskatsauksen DSN-tiedoston luomisprosessista Windows-järjestelmässä.

1. Avaa ODBC-tietolähteen järjestelmänvalvoja etsimällä aloitusvalikosta ODBC Data Sources.
2. Valitse System DSN -välilehti ja napsauta Lisää -painiketta.
3. Valitse sopiva ohjain tietokannalle, johon haluat muodostaa yhteyden, ja napsauta Valmis.
4. Täytä tarvittavat tiedot muodostaaksesi yhteyden tietokantaan, kuten palvelimen nimi, käyttäjätunnus ja salasana.
5. Napsauta OK tallentaaksesi DSN-tiedoston.

Vaihtoehtoisesti voit luoda DSN-tiedoston manuaalisesti luomalla pelkkä tekstitiedoston .dsn-tunnisteella ja syöttämällä tarvittavat yhteystiedot muodossa:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Voit sitten käyttää tämän tiedoston polkua DSN:nä koodissasi/komentosarjassasi muodostaaksesi yhteyden tietokantaan.

## Ohjelmat, jotka avaavat DSN-tiedoston

DSN-tiedosto on pelkkä tekstitiedosto, joka tallentaa tietoja, joita käytetään yhteyden muodostamiseen tietokantaan, kuten palvelimen nimi, käyttäjätunnus ja salasana. Sitä käytetään yleensä yhdessä ODBC:n (Open Database Connectivity) kanssa helpon pääsyn tarjoamiseen tiettyyn tietokantaan.

Voit avata ja tarkastella DSN-tiedoston sisältöä käyttämällä mitä tahansa tekstieditoria, kuten Muistio-, Sublime-teksti-, Atom- ja niin edelleen. Näiden ohjelmien avulla voit avata DSN-tiedoston ja tarkastella siihen tallennettuja yhteystietoja.

Jos haluat kuitenkin käyttää DSN-tiedostoa yhteyden muodostamiseen tietokantaan ja toimintojen, kuten SELECT, INSERT, UPDATE, DELETE jne. suorittamiseen, ODBC-tuella varustettu ohjelma, kuten ohjelmointikieli, kuten Python, Java, C# tai tietokannan hallintatyökalu, kuten Microsoft Access. , SQL Server Management Studio vaaditaan. Nämä ohjelmat voivat käyttää DSN-tiedoston tietoja muodostaakseen yhteyden tietokantaan ja suorittaakseen halutun toiminnon.

## Viitteet

* [Mikä on DSN (tietolähteen nimi)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



