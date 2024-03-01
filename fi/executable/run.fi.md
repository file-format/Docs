{
  "date" : "2023-01-31",
  "keywords" : ["run file", "what is a run file", "file", "how to open run file", "run file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi RUN-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata RUN-tiedostoja.",
  "title" : "RUN-tiedostomuoto - Linuxin suoritettava tiedosto",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run-fi",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Mikä on RUN-tiedosto?

.run-tiedostomuotoa käytetään yleisesti ohjelmistojen tai sovellusten asennusohjelmien jakeluun Linux-ympäristössä. Ohjelmiston asentaminen edellyttää, että tiedosto on suoritettava, mikä voidaan tehdä seuraavalla komennolla:

```bash
chmod +x file_name.run 
```

Sitten voit suorittaa tiedoston seuraavalla komennolla:

```bash
./file_name.run 
```

Asennusprosessi voi vaihdella riippuen tietystä tiedostosta ja ohjelmasta, jota yrität asentaa.

.run-tiedostomuoto on komentosarjan tyyppi, jota käytetään ohjelmistojen tai sovellusten asennusohjelmien jakamiseen Linux-ympäristössä. Se on itsenäinen paketti, joka sisältää kaiken ohjelmiston asentamiseen tarvittavan, mukaan lukien binaaritiedostot, kirjastot ja määritystiedostot.

On tärkeää huomata, että .run-tiedostot voivat sisältää myös haitallista koodia, joten on aina hyvä idea tarkistaa tiedoston lähde ja tarkistaa se virusten varalta ennen sen suorittamista.

Lisäksi jotkin .run-tiedostot saattavat vaatia pääkäyttäjän oikeuksia suorittaakseen ja asentaakseen, joten saatat joutua käyttämään sudo-komentoa suorittaaksesi tiedoston korotetuilla käyttöoikeuksilla:

```bash
sudo ./filename.run
```

## Kuinka avata RUN-tiedosto?

Jos haluat avata .run-tiedoston, sinun on tehtävä siitä suoritettava, mikä voidaan tehdä chmod-komennolla:

```bash
chmod +x filename.run 
```

Kun tiedosto on tehty suoritettavaksi, voit suorittaa sen kirjoittamalla:

```bash
./filename.run
```

.run-tiedoston suorittaminen ei ole sama asia kuin sen avaaminen tekstieditorissa. .run-tiedoston suorittaminen suorittaa sen käskyt, jotka voivat olla mitä tahansa ohjelman asentamisesta komentosarjan suorittamiseen. Jos haluat tarkastella .run-tiedoston sisältöä, sinun on avattava se tekstieditorissa, kuten nanossa tai vimissä:

```
nano filename.run
```
tai
```
vim filename.run
```

## Viitteet
* [Kuinka suorittaa .bin- ja .run-tiedostoja Ubuntussa](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)



