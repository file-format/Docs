{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi SAV-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata SAV-tiedostoja.",
  "title" : "SAV - SPSS-datatiedosto",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav-fi",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Mikä on SAV-tiedosto?
SAV-tiedosto on yhteiskuntatieteiden tilastopaketin (SPSS) luoma tietotiedosto, joka on markkinatutkijoiden, terveystutkijoiden, tutkimusyritysten, hallituksen, koulutustutkijoiden, markkinointiorganisaatioiden ja tiedonloujien laajasti käyttämä sovellus tilastoanalyysiin. SAV, joka on tallennettu omaan binäärimuotoon ja koostuu tietojoukosta sekä tietojoukkoa edustavasta sanakirjasta, tallentaa tiedot riveihin ja sarakkeisiin.

## SAV-tiedostomuoto
SAV-tiedostomuodosta on tullut suhteellisen vakaa, mutta emme voi sanoa sitä staattiseksi. Taakse- ja eteenpäinyhteensopivuus on valinnaisesti saatavilla tarvittaessa, mutta sitä ei ylläpidetä kunnolla. SAV-tiedoston tiedot on luokiteltu seuraaviin osiin:

### Tiedoston otsikko
Se koostuu 176 tavusta. Ensimmäiset 4 tavua osoittavat merkkijonon **$FL2** tai **$FL3** tiedostossa käytetyssä merkkikoodauksessa. Viimeiset kolme tavua edustavat sitä, että tiedoston tiedot on pakattu **ZLIB:llä**. Seuraava 60-tavuinen merkkijono alkaa **@(#) SPSS DATA FILE** ja määrittää myös tiedoston luoneen käyttöjärjestelmän ja SPSS-version. Otsikko jatkuu sitten kuusinumeroisilla kentillä, jotka sisältävät muuttujien lukumäärän havaintoa kohden ja numerokoodin pakkaamista varten, ja päättyy merkkitietoihin, jotka osoittavat luontipäivämäärän ja -ajan sekä tiedostotunnisteen.
### Muuttujakuvaajan tietueet
Tietue sisältää kiinteän kenttäjonon, joka luokittelee muuttujan tyypin ja nimen sekä SPSS:n käyttämät muotoilutiedot. Jokainen muuttujatietue voi valinnaisesti sisältää enintään 120 merkin pituisen muuttujatunnisteen ja enintään kolme puuttuvaa arvoa.
### Arvotunnisteet
The value labels are optional and stored in pairs of records with integer tags 3 and 4. Ensimmäisessä tietueessa, joka on tagi 3, on sarja kenttäpareja, joista jokainen sisältää arvon ja siihen liittyvän arvotunnisteen. Toinen tietue, joka on tagi 4, edustaa muuttujia, joita arvo-/tunnistejoukko koskee.
### Asiakirjat
Single or multiple records with integer tag 6. Valinnainen dokumentaatio. sisältää 80 merkin rivejä.
### Laajennustietueet
Single or multiple records with integer tag 7. Laajennustietueet tarjoavat tietoa, joka voidaan jättää huomiotta turvallisesti, mutta säilytettävä monissa tilanteissa mahdollistaa uudemmalla ohjelmistolla kirjoitettujen tiedostojen yhteensopivuuden säilyttämisen taaksepäin. Laajennustietueissa on kokonaislukujen alatyyppitunnisteet.
### Sanakirjan terminaattori
Only record with integer tag 999. Se erottaa sanakirjan havainnoista.
### Tietojen havainnot
Sen katsotaan olevan havaintojärjestyksessä, esim. ensimmäisen havainnon kaikki muuttuvat arvot, sen jälkeen kaikki toisen havainnon arvot jne. Tietueen muoto vaihtelee tiedoston otsikkotietueen pakkauskoodin mukaan. .sav-tiedoston dataosa voidaan purkaa:
- **koodi 0**: pakattu tavukoodilla
- **koodi 1**: pakattu ZLIB-pakkauksella
 






## Viitteet ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)


