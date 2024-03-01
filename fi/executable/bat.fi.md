{
  "date": "2021-06-24",
  "keywords": [
"bat tiedosto",
"mikä on bat-tiedosto",
"tiedosto",
"bat tiedosto esimerkki",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi BAT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BAT-tiedostoja.",
  "title": "BAT - Erätiedostomuoto",
  "linktitle": "BAT",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ba-fit"
}
},
  "lastmod": "2021-06-24"
}

## Mikä on BAT-tiedosto?
BAT-tiedosto tunnetaan erätiedostona, joka toimii DOS:n ja kaikkien Windows-versioiden kanssa cmd.exe-tiedoston alla. Se koostuu sarjasta tekstimuotoisia rivikomentoja, jotka komentorivitulkki suorittaa eri tehtävien suorittamiseksi, kuten ylläpitoapuohjelmien suorittamiseksi Windowsissa tai tavanomaisten ohjelmien käynnistämiseksi. Erätiedosto voi sisältää minkä tahansa komennon, jonka tulkki voi hyväksyä vuorovaikutteisesti, ja käyttää koodirakennetta, joka mahdollistaa ehdollisen haarautumisen ja silmukan komentosarjatiedostoon kirjoitetulla tavalla.
## BAT-tiedostomuoto
BAT-tiedostomuoto on yksinkertaisesti skripti, joka on sisällytetty automatisoimaan luonteeltaan toistuvia komentosarjoja. Termiä erä käytetään eräkäsittelyyn, sitä voidaan pitää ei-vuorovaikutteisena suorituksena. Siksi erätiedosto ei välttämättä käsittele usean tiedon erää. Vanhassa levykäyttöjärjestelmässä (DOS) erätiedosto ajettiin komentorivikäyttöliittymässä kirjoittamalla tiedoston nimi ja tunniste .bat. Aikaisempi Microsoftin graafiseen käyttöliittymään perustuva käyttöjärjestelmä, kuten Microsoft Windows, oli riippuvainen DOS:sta. Käyttäjien oli käytettävä DOS:ia suorittaakseen tyypillisiä toimintoja, kuten Windowsin korjaamista, optimointia tai uudelleenasennusta. Myöhemmin Microsoft esitteli Windows NT:n, joka ei ollut riippuvainen DOS-käyttöjärjestelmästä. Siksi erätiedostot voidaan ajaa käyttämällä komentokehotetta tai **cmd.exe** nykyaikaisissa Microsoft-käyttöjärjestelmissä.
### Erätiedoston parametrit
Komentorivi tukee useita erikoismuuttujia, kuten **%0, %1 - %9**, jotta voidaan viitata erätyön nimeen ja polkuun sekä yhdeksään kutsuparametriin erätyön sisällä. Olemattomat parametrit korvataan merkkijonolla, jonka pituus on nolla. Niitä voidaan kuitenkin käyttää samalla tavalla kuin ympäristömuuttujia, mutta niitä ei tallenneta ympäristöön. Microsoft ja IBM kutsuvat näitä muuttujia korvausparametreiksi, kun taas Novell, Digital Research ja Caldera ottivat käyttöön termin korvaavat muuttujat.

Tässä on joitain hyödyllisiä erätiedostokomentoja:
| Komento | Kuvaus |
------|------------|
| VER | Tämä eräkomento näyttää käyttämäsi MS-DOS-version. |
|ASSOC| Tämä on eräkomento, joka liittää laajennuksen tiedostotyyppiin (FTYPE), näyttää olemassa olevat yhteydet tai poistaa yhteyden. |
|CD| Tämä eräkomento auttaa tekemään muutoksia toiseen hakemistoon tai näyttää nykyisen hakemiston. |
|CLS| Tämä eräkomento tyhjentää näytön. |
|KOPIOINTI| Tätä eräkomentoa käytetään tiedostojen kopioimiseen paikasta toiseen. |
|DEL| Tämä eräkomento poistaa tiedostoja, ei hakemistoja. |
|DIR| Tämä eräkomento luettelee hakemiston sisällön. |
|PÄIVÄMÄÄRÄ| Tämä eräkomento auttaa löytämään järjestelmän päivämäärän. |
|ECHO| Tämä eräkomento näyttää viestejä tai ottaa komentojen kaiun käyttöön tai poistaa sen käytöstä. |
|POISTU| Tämä eräkomento poistuu DOS-konsolista. |
|MD| Tämä eräkomento luo uuden hakemiston nykyiseen sijaintiin. |
|SIIRTO| Tämä eräkomento siirtää tiedostoja tai hakemistoja hakemistojen välillä. |
|PATH| Tämä eräkomento näyttää tai asettaa polkumuuttujan. |
|TAUKO| Tämä eräkomento kehottaa käyttäjää ja odottaa syöterivin syöttämistä. |
|PROMPT| Tällä eräkomennolla voidaan muuttaa tai nollata cmd.exe-kehote. |
|RD| Tämä eräkomento poistaa hakemistoja, mutta hakemistojen on oltava tyhjiä ennen kuin ne voidaan poistaa. |
|REN| Nimeää tiedostoja ja hakemistoja uudelleen |
|REM| Tätä eräkomentoa käytetään erätiedostojen huomautuksiin, mikä estää huomautuksen sisällön suorittamisen. |
|START| Tämä eräkomento käynnistää ohjelman uudessa ikkunassa tai avaa asiakirjan. |
|AIKA| Tämä eräkomento asettaa tai näyttää ajan. |
|TYYPPI| Tämä eräkomento tulostaa tiedoston tai tiedostojen sisällön tulosteeseen. |
|VOL| Tämä eräkomento näyttää taltioiden nimet. |
|ATTRIB| Näyttää tai asettaa nykyisen hakemiston tiedostojen attribuutit |
|CHKDSK| Tämä eräkomento tarkistaa levyn mahdollisten ongelmien varalta. |
|VALINTA| Tämä eräkomento tarjoaa käyttäjälle luettelon vaihtoehdoista. |
|CMD| Tämä eräkomento kutsuu toisen komentokehotteen esiintymän. |
|COMP| Tämä eräkomento vertaa kahta tiedostoa tiedoston koon perusteella. |
|MUUNNA| Tämä eräkomento muuntaa taltion FAT16- tai FAT32-tiedostojärjestelmästä NTFS-tiedostojärjestelmään. |
|DRIVERQUERY| Tämä eräkomento näyttää kaikki asennetut laiteohjaimet ja niiden ominaisuudet. |
|LAAJENNA| Tämä eräkomento purkaa tiedostot pakatuista .cab-kaappitiedostoista. |
|ETSI| Tämä eräkomento etsii merkkijonoa tiedostoista tai syötteestä ja tulostaa vastaavat rivit. |
|FORMAT| Tämä eräkomento alustaa levyn käyttämään Windowsin tukemaa tiedostojärjestelmää, kuten FAT, FAT32 tai NTFS, mikä korvaa levyn aiemman sisällön. |
|OHJE| Tämä eräkomento näyttää luettelon Windowsin toimittamista komennoista. |
|IPCONFIG| Tämä eräkomento näyttää Windowsin IP-kokoonpanon. Näyttää määritykset yhteyden mukaan ja kyseisen yhteyden nimen. |
|LABEL| Tämä eräkomento lisää, asettaa tai poistaa levytunnisteen. |
|LISÄÄ| Tämä eräkomento näyttää tiedoston tai tiedostojen sisällön näyttö kerrallaan. |
|NET| Tarjoaa erilaisia verkkopalveluita käytetystä komennosta riippuen. |
|PING| Tämä eräkomento lähettää ICMP/IP kaiku-paketteja verkon yli määritettyyn osoitteeseen. |
|SAMMUTA| Tämä eräkomento sammuttaa tietokoneen tai kirjaa ulos nykyisen käyttäjän. |
|LAJITTELU| Tämä eräkomento ottaa syötteen lähdetiedostosta ja lajittelee sen sisällön aakkosjärjestyksessä A:sta Z:hen tai Z:sta A:han. Se tulostaa tulosteen konsoliin. |
|SUBST| Tämä eräkomento määrittää asemakirjaimen paikalliseen kansioon, näyttää nykyiset tehtävät tai poistaa tehtävän. |
|SYSTEMINFO| Tämä eräkomento näyttää tietokoneen ja sen käyttöjärjestelmän kokoonpanon. |
|TASKKILL| Tämä eräkomento päättää yhden tai useamman tehtävän. |
|TEHTÄVÄLISTA| Tämä eräkomento luettelee tehtävät, mukaan lukien tehtävän nimi ja prosessitunnus (PID). |
|XCOPY| Tämä eräkomento kopioi tiedostoja ja hakemistoja edistyneemmällä tavalla. |
|PUU| Tämä eräkomento näyttää puun kaikista nykyisen hakemiston alihakemistoista millä tahansa rekursio- tai syvyystasolla. |
|FC |Tämä eräkomento näyttää todelliset erot kahden tiedoston välillä. |
|DISKPART |Tämä eräkomento näyttää ja määrittää levyosioiden ominaisuudet. |
|TITLE |Tämä eräkomento määrittää konsoli-ikkunassa näkyvän otsikon. |
|SET | Näyttää luettelon nykyisen järjestelmän ympäristömuuttujista. |

## Esimerkki BAT-tiedostosta
Eräkomentosarjat tallennetaan yleensä yksinkertaisina tekstitiedostoina; sisältää komentoja, jotka suoritetaan järjestyksessä. Nämä tiedostot tallennetaan .bat-tunnisteella; tunnistetaan ja suoritetaan **Command Interpreter** -ohjelmistolla. Tämä ohjelmisto on saatavilla Microsoft Windowsissa nimellä **cmd.exe**.

Tässä on esimerkki eräkomentosarjasta, joka poistaa kaikki tiedostot nykyisestä hakemistosta:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Viitteet 

* [Batch Script - Pikaopas](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)

* [Erätiedosto - Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


