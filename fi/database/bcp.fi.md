{
  "date": "2020-11-11",
  "keywords": [
"BCP",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi BCP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BCP-tiedostoja.",
  "title": "BCP - SQL Server Bulk Copy File Format",
  "linktitle": "BCP",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bc-fip"
}
},
  "lastmod": "2020-08-12"
}

## Mikä on BCP-tiedosto?

BCP (Bulk Copy Format) on Microsoft SQL Serverin tekninen tietomuoto, joka määrittää tietorakenteet erilaisten tietokannan tietotyyppiarvojen tallentamiseksi tuontia/vientiä varten. Muoto määrittelee täysin jokaisen tietosarakkeen tulkinnan niin, että datatiedostossa määritetty arvojoukko voidaan lukea. [BCP](https://learn.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) -apuohjelma käyttää BCP-tiedostomuotoa tietojen lukemiseen tällaisesta tiedostosta ja sen tunnistamiseen.


## BCP-tiedostomuoto

BCP-muotoinen tiedosto on XML-dokumentti, joka määrittää sarakkeiden järjestyksen, nimen ja tietotyypin. Sen avulla käyttäjät voivat tuoda/viedä suuria määriä tietoja tietotiedostosta, jossa määritetään nämä kentät. Tästä on apua data-arvojen joukkotuonnissa datatiedostoista. Tietokenttien lukumäärä ja järjestys datatiedostossa voivat poiketa kohdetaulukon sarakkeiden kentistä. Tällöin BCP-tietomuototiedosto tulee avuksi määrittämällä sarakkeiden järjestyksen ja tyypin tietojen tuontia varten.

Muototiedoston rakenne on esitetty seuraavassa muodossa.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### BCP-tietotyypit

|Tietotyyppi|alue|Esitys|
---|---|---|
|BigInt|-263 (-9 223 372 036 854 775 808) - 263-1 (9 223 372 036 854 775 807)|`BigInt = [-]1*19 DIGIT`|
|Binaari|1–8000 tavua|heksadesimaalikoodattu Unicode-merkkijonomuoto `Binaari = 32000OCTET`|
|Bitti|0 tai 1|yksinkertainen Unicode-merkkijono Bitti = 0 / 1|
|Char|1 - 8000|Unicode-merkkijonomuoto, merkki = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET, n = 4 x (2 147 483 647)|
|Päivämäärä|0001-01-01 - 9999-12-31|VVVV-KK-PP merkkijonomuoto|
|PäiväysAika|1753-01-01 00:00:00.000 - 9999-12-31 23:59:59.997| Unicode VVVV-KK-PP tt:mm:ss[.nnn] merkkijonomuoto|
|DateTime2|0001-01-01 00:00:00.0000000 - 9999-12-31 23:59:59.9999999.| Unicode VVVV-KK-PP tt:mm:ss[.nnnnnnn] merkkijonomuoto|
|DateTimeOffset|0001-01-01 00:00:00.0000000 - 9999-12-31 23:59:59.9999999 koordinoidun maailmanajan (UTC) aikavyöhykkeellä| Unicode VVVV-KK-PP tt:mm:ss[.nnnnnnn] [{+|-}tt:mm] merkkijonomuoto|
|Desimaali|-1038 + 1 - 1038 – 1|Unicode-merkkijonomuoto `Decimal = [-] 0*38DIGIT [.0*38DIGIT]`|
|Kelluke|-1,79E+308 - -2,23E-308; 0; 2.23E-308 - 1.79E+308|Unicode-merkkijonomuoto|
|Kuva|tavusarja, joka vaihtelee välillä 0–231 – 1 (2 147 483 647)|heksadesimaalikoodattu Unicode-merkkijonomuoto|
|Int|-231 (-2 147 483 648) - 231 – 1 (2 147 483 647)|Unicode-merkkijonomuoto|

## Viitteet

 * [BCP-muoto – Microsoft](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

