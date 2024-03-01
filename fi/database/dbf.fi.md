{
  "date": "2021-06-15",
  "keywords": [
"DBF",
"laajennus",
"dbf tiedosto",
"dbf tiedostomuoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"mikä on dbf-tiedosto",
"dBASE"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DBF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DBF-tiedostoja.",
  "title": "DBF - dBase-tietokantatiedosto",
  "linktitle": "DBF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-fif"
}
},
  "lastmod": "2021-06-15"
}

## Mikä on DBF-tiedosto?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. DBF-tiedostotyyppi otettiin käyttöön dBASE II:n kanssa vuonna 1983. Se järjestää useita tietueita Array-tyyppisillä kentillä. **xBase**-tietokantaohjelmisto, joka on suosittu, koska se on yhteensopiva useiden tiedostomuotojen kanssa; tukee myös DBF-tiedostoja.

## DBF-tiedostomuoto
DBF-tiedostomuoto kuuluu dBASE-tietokannan hallintajärjestelmään, mutta se voi olla yhteensopiva xBase- tai muiden DBMS-ohjelmistojen kanssa. dbf-tiedoston alkuperäinen versio koostui yksinkertaisesta taulukosta, johon voitiin lisätä, muokata, poistaa tai tulostaa tietoja ASCII-merkkijoukon avulla. Ajan myötä .dbf-tiedostoa parannettiin ja lisätiedostoja lisättiin tietokantajärjestelmän ominaisuuksien ja ominaisuuksien lisäämiseksi.

Nykyaikaisessa dBASE:ssa DBF-tiedosto koostuu otsikosta, tietueista ja EOF (Tiedoston loppu) -merkistä.

- Otsikko sisältää tietoja tiedostosta, kuten tietueiden lukumäärän ja tietueissa käytettyjen kenttätyyppien lukumäärän.
- Tietueet sisältävät todelliset tiedot.
- Tiedoston loppu on merkitty yhdellä tavulla, jonka arvo on 0x1A.

### Tiedoston otsikko
dBase-tiedoston otsikon asettelu on annettu seuraavassa taulukossa:

| Tavu | Sisältö | Merkitys |
---|---|---|
| 0 | 1 tavu | Kelvollinen dBASE DOS-tiedostolle; bitit 0–2 ilmaisevat versionumeron, bitti 3 ilmaisevat dBASE:n olemassaolon DOS-muistiotiedostoa varten, bitit 4–6 osoittavat SQL-taulukon olemassaolon, bitti 7 ilmaisevat minkä tahansa muistiotiedoston olemassaolon (joko dBASE m PLUS tai dBASE DOS) |
| 1-3 | 3 tavua | Viimeisimmän päivityksen päivämäärä; muotoiltu muodossa VVKKPP |
| 4–7 | 32-bittinen numero | Tietueiden lukumäärä tietokantatiedostossa |
| 8–9 | 16-bittinen numero | Tavujen määrä otsikossa |
| 10–11 | 16-bittinen numero | Tietueen tavujen määrä |
| 12–13 | 2 tavua | Varattu; täytä 0 |
| 14 | 1 tavu | Lippu, joka osoittaa keskeneräisen tapahtuman[huomautus 1] |
| 15 | 1 tavu | Salauslippu[huomautus 2] |
| 16–27 | 12 tavua | Varattu dBASE:lle DOS:lle usean käyttäjän ympäristössä |
| 28 | 1 tavu | Tuotanto .mdx-tiedoston lippu; 1, jos tuotanto-.mdx-tiedosto on, 0, jos ei |
| 29 | 1 tavu | Kieliohjaimen tunnus |
| 30–31 | 2 tavua | Varattu; täytä 0 |
| 32–n [viite 3][viite 4] | 32 tavua kukin | joukko kenttäkuvauksia (katso kuvauksien asettelu alla) |
| n + 1 | 1 tavu | 0x0D kenttäkuvaajan taulukon päätteeksi |

- ISMARKEDO-toiminto tarkistaa tämän lipun (ALKUTAPAHTUMA asettaa sen arvoon 1, END TRANSACTION ja ROLLBACK palauttaa sen arvoon 0).
- Jos tämän lipun arvoksi on asetettu 1, näyttöön tulee viesti Tietokanta salattu.
- Kenttien enimmäismäärä on 255.
- n tarkoittaa viimeistä tavua kenttäkuvaustaulukossa.

### Kenttäkuvaustaulukko
Kenttäkuvaajien asettelu dBASE:ssa:

| Tavu | Sisältö | Merkitys |
---|---|---|
| 0–10 | 11 tavua | Kentän nimi ASCII-muodossa (nollatäytetty) |
| 11 | 1 tavu | Kentän tyyppi. Sallitut arvot: C, D, F, L, M tai N (katso merkitykset seuraavasta taulukosta) |
| 12–15 | 4 tavua | Varattu |
| 16 | 1 tavu | Kentän pituus binäärimuodossa (enintään 254 (0xFE)). |
| 17 | 1 tavu | Kenttien desimaaliluku binäärimuodossa |
| 18–19 | 2 tavua | Työalueen tunnus |
| 20 | 1 tavu | Esimerkki |
| 21–30 | 10 tavua | Varattu |
| 31 | 1 tavu | Tuotanto MDX-kentän lippu; 1, jos kentässä on indeksitunniste tuotanto-MDX-tiedostossa, 0, jos ei |

### Tietokannan tietueet
Jokainen tietue alkaa poistolipulla (1-tavuinen). Kentät kääritään tietueiksi ilman kenttäerottimia. Kaikki kenttätiedot ovat ASCII-muotoisia. Kentän tyypistä riippuen sovellus asettaa lisärajoituksia. Tässä on dBasen kenttätyypit:

| Kentän tyyppi | Mnemoninen | Mitä se hyväksyy |
-------|-----|----|
| C | Hahmo | Mikä tahansa ASCII-teksti (täytetty välilyönneillä kentän pituuteen asti) |
| D | Päivämäärä | Numerot ja merkki, jotka erottavat kuukauden, päivän ja vuoden (tallennettu sisäisesti 8-numeroisina VVVVKKPP-muodossa) |
| F | Liukuluku | -, ., 0–9 (tasattu oikealle, täytetty välilyönneillä) |
| L | Looginen | Y, y, N, n, T, t, F, f tai ? (kun alustamaton) |
| M | Muistio | Mikä tahansa ASCII-teksti (tallennettu sisäisesti 10 numerona, jotka edustavat .dbt-lohkonumeroa, tasattu oikealle, täytetty välilyönneillä) |
| N | Numeerinen | -, ., 0–9 (tasattu oikealle, täytetty välilyönneillä) |









## Viitteet ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)


