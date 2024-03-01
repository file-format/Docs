{
  "date": "2023-05-08",
  "keywords": [
"cc-tiedosto",
"mikä on cc-tiedosto",
"cc:n kääntäminen c++-kääntäjillä",
"kuinka avata cc-tiedosto",
"tiedosto",
"cc tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CC-tiedostomuoto - C++-lähdekooditiedosto",
  "description": "Opi CC-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata CC-tiedostoja.",
  "linktitle": "CC",
  "menu": {
    "docs": {
      "identifier": "programming-cc-fi",
      "parent": "programming"
}
},
  "lastmod": "2023-05-08"
}

## Mikä on CC-tiedosto?

CC-tiedosto on eräänlainen lähdekooditiedosto, joka sisältää C++-ohjelmointikielellä kirjoitetun koodin. Se voi sisältää joko kaiken yksittäiseen ohjelmaan tarvittavan koodin tai osan koodista, joka on osa suurempaa ohjelmointiprojektia, joka koostuu useista CC-tiedostoista. CC-tiedoston sisältämän koodin muokkaamiseen tai tarkastelemiseen kehittäjät käyttävät usein lähdekoodieditoria. Muokkauksen jälkeen he kääntävät koodin kääntäjällä muuntaakseen sen konekoodiksi, jonka tietokoneen käyttöjärjestelmä voi suorittaa ohjelman suorittamiseksi.

## CC-tiedostomuoto – lisätietoja

.cc-tiedostotunnistetta on käytetty C++-lähdekooditiedostoissa useiden vuosikymmenien ajan. C++-kielen kehitti 1970-luvun lopulla Bjarne Stroustrup, joka työskenteli tuolloin Bell Labsissa. Stroustrup halusi laajentaa C-ohjelmointikieltä tukemalla olio-ohjelmointikonsepteja, jotka hänen mielestään olivat välttämättömiä suurten ohjelmistojärjestelmien rakentamisessa.

C++:n ensimmäinen versio julkaistiin vuonna 1983, ja se saavutti nopeasti suosion kehittäjien keskuudessa, jotka arvostivat sen tehokkaita ominaisuuksia ja joustavuutta. Kun C++:n käyttö laajeni, tuli tarpeelliseksi luoda koodauskäytäntöjä ja tiedostojen nimeämiskäytäntöjä suurten koodikantojen järjestämisen ja hallinnan helpottamiseksi.

Google's C++ Style Guide which recommends using .cc file extension for C++ source code files, was first published in 2003. Siitä lähtien opasta on päivitetty säännöllisesti vastaamaan C++-kielen muutoksia ja laajemman ohjelmointiyhteisön kehityskäytäntöjä.

Nykyään .cc-tiedostotunniste on edelleen suosittu valinta C++-lähdekooditiedostoille, ja monet suositut kehitystyökalut ja -ympäristöt tunnistavat sen.

## Kuinka avata CC-tiedosto?

CC-tiedostojen avaamiseen ja muokkaamiseen voidaan käyttää monia lähdekoodieditoreja, mukaan lukien monikäyttöiset työkalut, kuten Microsoft Visual Studio Code ja Code Blocks. Nämä editorit tarjoavat hyödyllisiä ominaisuuksia, kuten syntaksin korostuksen ja automaattisen täydennyksen, joten ne ovat erinomainen valinta CC-tiedostojen käsittelyyn.

Voit myös avata CC-tiedostoja millä tahansa tekstieditorilla, esim. Notepadilla, Notepad++:lla jne.

## CC:n kääntäminen C++-kääntäjillä

CC-tiedoston kääntäminen C++-kääntäjällä sisältää useita vaiheita. Ensimmäinen askel on asentaa yhteensopiva C++-kääntäjä käyttöjärjestelmääsi ja kehitysympäristöäsi varten. Saatavilla on monia erilaisia kääntäjiä, mukaan lukien GCC, Clang ja Microsoft Visual C++.

Kun olet asentanut C++-kääntäjän, seuraava vaihe on avata pääte- tai komentokehote ja siirtyä hakemistoon, jossa CC-tiedosto sijaitsee. Täältä voit ajaa kääntäjän suorittamalla kääntäjän toimittaman komentorivityökalun. CC-tiedoston kääntämiskomento voi vaihdella käytettävän kääntäjän mukaan. Esimerkiksi, jos haluat kääntää CC-tiedoston GCC:n avulla, suoritat seuraavanlaisen komennon:

```
g++ -o myprogram myfile.cc
```

## Viitteet
* [GNU Compiler Collection](https://en.wikipedia.org/wiki/GNU_Compiler_Collection)


