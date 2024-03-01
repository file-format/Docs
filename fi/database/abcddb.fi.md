{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi ABCDDB-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata ABCDDB-tiedostoja.",
  "title" : "ABCDDB-tiedostomuoto - Applen osoitekirjan yhteystietoluettelotietokantatiedosto",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-fi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Mikä on ABCDDB-tiedosto?

Tiedosto, jonka tunniste on **.ABCDDB**, tarkoittaa Apple Address Book Contact List Database -tietokantaa. Se kuuluu **Osoitekirja**-sovellukseen, joka tunnetaan myös nimellä **Yhteystiedot**. Se on sisäänrakennettu sovellus, joka sisältyy iOS- ja macOS-käyttöjärjestelmiin. Yhteystiedot-sovelluksen avulla käyttäjät voivat tallentaa ja järjestää yhteystietoihinsa liittyviä tietoja, mukaan lukien yksityishenkilöt, yritykset ja organisaatiot. Tämän sovelluksen avulla käyttäjät voivat seurata tietoja, kuten nimiä, osoitteita, puhelinnumeroita ja sähköpostiosoitteita, sekä luokitella yhteystietonsa ryhmiin.

## Suhde SQLiteen ja Typical Pathiin

Applen osoitekirja (tunnetaan myös nimellä Yhteystiedot) tallentaa yhteystiedot vCard-muodossa metatietokansioon. **Tiedosto _ABCDDB_ on itse asiassa _SQLite 3 -datatiedosto_**.

SQLite on suosittu tietokannan hallintajärjestelmä, joka on suunniteltu kevyeksi ja itsenäiseksi. Sitä käytetään monissa erilaisissa ohjelmistoissa ja laitteissa. SQLite on eräänlainen RDBMS, mikä tarkoittaa, että se tallentaa tiedot taulukoihin, jotka liittyvät toisiinsa avainten kautta. Se pystyy käsittelemään useita tietotyyppejä, mukaan lukien kokonaisluvut, liukulukuluvut, merkkijonot ja binääritiedot. Lisäksi SQLite tukee tapahtumia, joiden avulla käyttäjät voivat suorittaa useita tietokantatoimintoja yhdessä yhtenä työyksikkönä.

Tiedosto, jonka laajennus on ABCDDB, tallennetaan yleensä tähän

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Korjaa vioittunut yhteystietokanta

Ota ensin varmuuskopio ennen kuin yrität tehdä tämän. Siirry sitten osoitteeseen

`~/Kirjasto/Sovellustuki/Osoitekirja`

Tästä hakemistosta löydät kolme tiedostoa, joista yksi on .abcddb-tunniste

- `osoitekirja-v22.abcddb`
- `osoitekirja-v22.abcddb-wal`
- osoitekirja-v22.abcddb-shm.

Poista kaikki nämä tiedostot ja avaa yhteystiedot uudelleen, se alkaa toimia uudelleen.

## Palauta osoitekirjan tietokanta varmuuskopiosta

Oletetaan, että AddressBook-tietokantasi yhteystiedot on tallennettu hakemistoon addressbook-v22.abcddb.

- Varmuuskopioi ensin osoitekirjan tiedot ja sulje kaikki sovellukset.
- Siirrä tietokantatiedostosi alihakemistoon ~/Library/Application Support/AddressBook
- Käynnistä **Address Book.app**.

## Vie ABCDDB-tiedoston tiedot Microsoft Accessiin

Koska tiedosto on SQLite 3 -datatiedosto, voit viedä abcddb-tiedoston sisältämät tiedot Microsoft Accessiin ODBC-liittimen avulla.

SQLite ODBC -liitin on ohjelmistokirjasto ja -ohjain, jonka avulla ODBC-liitäntää tukevat sovellukset voivat muodostaa yhteyden SQLite-tietokantaan. Se sisältää kirjaston, joka määrittää ODBC-rajapinnan, ja ohjaimen, joka muuttaa tämän rajapinnan kutsuiksi SQLite API:lle. Jotta voit käyttää SQLite ODBC -liitintä, sinun on ensin asennettava se ja määritettävä sitten ODBC-tietolähde tietokoneellesi. Näiden vaiheiden suorittamisen jälkeen kaikki ODBC-tuella varustetut sovellukset voivat muodostaa yhteyden tietolähteeseen ja hakea tietoja SQLite-tietokannasta.

## Viitteet
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Macin yhteystietokanta](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Miten voin avata tai viedä abcddb-tiedoston Windows 7 Excelissä?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

