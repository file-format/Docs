{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME-tiedosto - Mikä on .time-tiedosto? Aika, jolloin tiedosto luotiin Linuxissa",
  "description" : "Opi TIME-tiedostosta ja selvitä aika, jolloin tiedosto luotiin Linuxissa",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-fi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Mikä on TIME-tiedosto?

TIME-tiedostomuotoa käytti verkkojärjestelmä nimeltä LIGHT, joka auttoi käyttäjiä tallentamaan, järjestämään ja jakamaan elämäänsä. Pohjimmiltaan se tallensi kokoelman viestejä ja edusti kansiota käyttäjän elämäsivulla järjestelmässä.

## Kuinka selvittää, milloin tiedosto luotiin Linuxissa

Linuxissa voit käyttää `stat`-komentoa selvittääksesi, milloin tiedosto on luotu. Näin voit tehdä sen:

Avaa pääte ja kirjoita seuraava komento:

```
stat <file_path>
```

Korvaa `<file_path> ` sinua kiinnostavan tiedoston polulla. Esimerkki:

```
stat /path/to/your/file.txt
```

Tämä komento näyttää erilaisia tietoja tiedostosta, mukaan lukien sen luomisajan. Etsi rivi, joka alkaa sanoilla Birth tai File:. Syntymäaika osoittaa, milloin tiedosto luotiin tiedostojärjestelmässä.

Tässä on esimerkki siitä, miltä tulos saattaa näyttää:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Tässä esimerkissä Syntymäaika osoittaa, milloin tiedosto luotiin.

