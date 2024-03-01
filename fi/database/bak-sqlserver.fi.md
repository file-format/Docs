{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak tiedosto",
"Microsoft SQL Server -tietokannan varmuuskopiointi",
"mikä on bak-tiedosto",
"kuinka avata bak-tiedosto",
"tiedosto",
"bak tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK-tiedostomuoto - Microsoft SQL Server -tietokannan varmuuskopio",
  "description": "Opi BAK SQL Server Backup -muodosta ja sovellusliittymistä, jotka voivat luoda ja avata BAK-tiedostoja.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver-fi",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Mikä on BAK-tiedosto?

.bak-tiedosto on Microsoft SQL Serverin yhteydessä varmuuskopiotiedostomuoto, jota käytetään SQL Server -tietokannan kopioiden tallentamiseen. Nämä tiedostot sisältävät tilannekuvan tietokannasta tietyllä hetkellä, mukaan lukien sen skeema, tiedot ja muut asiaan liittyvät tiedot. Ne luodaan käyttämällä SQL Serverin sisäänrakennettua varmuuskopiointi- ja palautustoimintoa, ja ne palvelevat useita tärkeitä tarkoituksia:

1. **Tietojen palautus:** .bak-tiedostot tarjoavat keinon palauttaa tietokanta tietojen katoamisen, vioittumisen tai muiden ongelmien varalta. Kun palautat tietokannan .bak-tiedostosta, voit palauttaa sen aiempaan tilaan, mikä minimoi seisokit ja tietojen menetyksen.

2. **Siirto ja kloonaus:** Varmuuskopiotiedostoja käytetään usein tietokantojen siirtämiseen palvelimien välillä tai tietokantojen kopioiden luomiseen testausta, kehitystä tai raportointia varten. Ne tarjoavat johdonmukaisen ja tehokkaan tavan siirtää tietokantoja ympäristöjen välillä.

3. **Point-in-Time Recovery:** SQL Serverin avulla voit suorittaa ajankohtaisen palautuksen käyttämällä .bak-tiedostoja. Tämä tarkoittaa, että voit palauttaa tietokannan tiettyyn hetkeen, mikä voi olla ratkaisevan tärkeää säännösten noudattamisen tai tietojen tarkastuksen kannalta.

4. **Disaster Recovery:** .bak-tiedostot ovat kriittinen osa katastrofipalautussuunnittelua. Ne varmistavat, että tietosi ovat turvassa ja että ne voidaan palauttaa nopeasti laitteistovikojen, luonnonkatastrofien tai muiden katastrofaalisten tapahtumien sattuessa.

## Luo .BAK-tiedosto SQL Serverissä

Luodaksesi .bak-tiedoston SQL Serverissä, käytät yleensä SQL Server Management Studion (SSMS) tai Transact-SQL:n (T-SQL) komentoja, kuten BACKUP DATABASE tai BACKUP LOG. Tässä on yksinkertaistettu esimerkki siitä, kuinka voit luoda tietokannan varmuuskopion T-SQL:llä:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Palauta .BAK-tiedosto SQL Serverissä

Voit palauttaa tietokannan .bak-tiedostosta käyttämällä RESTORE DATABASE -komentoa:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Kuinka avata BAK-tiedosto SQL Serverissä?

Jos haluat avata .bak-tiedostoon tallennettuja tietoja ja käyttää niitä, sinun on yleensä palautettava se Microsoft SQL Server -esiintymään. Tässä ovat yleiset vaiheet .bak-tiedoston avaamiseksi SQL Server Management Studion (SSMS) avulla:

1. **Käynnistä SQL Server Management Studio**: Avaa SSMS tietokoneellasi. Löydät sen yleensä Käynnistä-valikosta tai etsimällä SQL Server Management Studio.

2. **Yhdistä SQL Server -esiintymään**: Yhdistä SSMS:ssä siihen SQL Server -esiintymään, johon haluat palauttaa tietokannan. Tarvitset tarvittavat käyttöoikeudet tämän toiminnon suorittamiseen.

3. **Palauta tietokanta**:

a. Laajenna SQL Server -esiintymä vasemmalla olevassa Object Explorer -ruudussa.

b. Laajenna Tietokastot-solmu.

c. Napsauta hiiren kakkospainikkeella Tietokastot ja valitse Palauta tietokanta.

4. **Määritä lähde ja kohde**:

a. Kirjoita Palauta tietokanta -valintaikkunan Yleiset-sivulla uuden tietokannan nimi tietokantaan -kenttään. Tämä on palautetun tietokannan nimi.

b. Valitse Lähde-osiossa Laite varmuuskopion mediatyypiksi.

c. Napsauta ...-painiketta Laite-kentän vieressä löytääksesi .bak-tiedoston, jonka haluat palauttaa.

d. Valitse .bak-tiedosto, jonka haluat avata, ja napsauta OK.

5. **Palautusasetukset**: Tarkista ja määritä palautusasetukset tarpeen mukaan. Voit määrittää, korvataanko olemassa oleva tietokanta, määrittää palautusasetukset ja paljon muuta. Varmista, että asetat nämä asetukset tarpeidesi mukaan.

6. **Aloita palautus**: Kun olet määrittänyt palautusasetukset, napsauta OK-painiketta Palauta tietokanta -valintaikkunassa. SQL Server aloittaa palautusprosessin.

7. **Käytä palautettua tietokantaa**: Onnistuneen palautuksen jälkeen voit käyttää palautettua tietokantaa SQL Server Management Studiossa aivan kuten mitä tahansa muuta tietokantaa. Voit suorittaa kyselyitä, tarkastella taulukoita ja käsitellä tietokannan tietoja.

## Muut BAK-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.bak**-tiedostotunnistetta.

**Tietokanta**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Peli**
- {{HYPERLINKKI1}}

**Sekalaista**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Asetukset**
- {{HYPERLINKKI1}}

## Viitteet
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
