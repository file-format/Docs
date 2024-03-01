{
  "date": "2023-05-31",
  "keywords": [
"työpöytätiedosto",
"mikä on työpöytätiedosto",
"mitä työpöytätiedosto sisältää",
"esimerkki työpöytätiedostosta",
"kuinka avata työpöytätiedosto",
"mikä on työpöytätiedoston muoto",
"tiedosto",
"työpöydän tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "DESKTOP-tiedostomuoto - työpöydän syöttötiedosto",
  "description": "Opi DESKTOP-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata DESKTOP-tiedostoja.",
  "linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-05-31"
}

## Mikä on DESKTOP-tiedosto?

.desktop-tiedosto on määritystiedosto, jota Linux-työpöytäympäristöt käyttävät sovellusten pikakuvakkeiden ja käynnistysohjelmien määrittämiseen. Se tarjoaa metatietoja sovelluksesta, kuten sen nimen, kuvakkeen, suoritettavan komennon ja muita ominaisuuksia. Näitä tiedostoja käytetään yleensä luomaan pikakuvakkeita sovellusvalikoissa, työpöydän käynnistysohjelmissa tai paneeleissa Linux-pohjaisissa järjestelmissä.

## Mitä DESKTOP-tiedosto sisältää?

.desktop-tiedosto noudattaa tiettyä muotoa ja sisältää useita avainkenttiä:

- **[Desktop Entry]:** Tämä on .desktop-tiedoston pääosan otsikko.
- **Nimi:** Määrittää sovelluksen nimen.
- **Comment:** Provides brief description or comment about application.
- **Exec:** Määrittää komennon, joka suoritetaan sovellusta käynnistettäessä.
- **Kuvake:** Määrittää polun sovellukseen liittyvään kuvaketiedostoon.
- **Terminaali:** Määrittää, ajetaanko sovellus pääteikkunassa.
- **Tyyppi:** Määrittää merkinnän tyypin, kuten Sovellus tai Linkki.
- **Categories:** Specifies categories or groups under which the application should be displayed in the menu.
- **StartupNotify:** Määrittää, näyttääkö työpöytäympäristön käynnistysilmoitus sovellukselle.
- **NoDisplay:** Specifies whether application should be hidden from menus.
- **Toiminnot:** Määrittää lisätoiminnot, jotka voidaan suorittaa sovellukselle, kuten tietyn tiedoston avaaminen.

## Esimerkki DESKTOP-tiedostosta

Tässä on esimerkki .desktop-tiedostosta kuvitteelliselle tekstieditorille nimeltä MyTextEditor:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Tässä esimerkissä .desktop-tiedosto määrittää sovelluksen MyTextEditor siihen liittyvine ominaisuuksineen. Se sisältää myös kaksi lisätoimintoa, Avaa uusi ikkuna ja Avaa olemassa oleva tiedosto, joita voidaan käyttää sovelluksen käynnistysohjelman pikavalikosta.

Sijoittamalla .desktop-tiedoston tiettyihin hakemistoihin, kuten `/usr/share/applications` tai `~/.local/share/applications`, työpöytäympäristö tunnistaa sen ja näyttää sovelluksen vastaavasti valikoissa tai sallii sen käynnistämisen työpöytä.

## Kuinka avata DESKTOP-tiedosto?

Useat ohjelmistot voivat avata ja käsitellä .desktop-tiedostoja. Nämä ohjelmat ovat tyypillisesti tiedostonhallintaohjelmia tai työpöytäympäristöjä Linux-pohjaisissa järjestelmissä. Tässä muutamia esimerkkejä:

- **Nautilus (tiedostot):** GNOME-työpöytäympäristön oletustiedostonhallinta.
- **Nemo:** Cinnamon-työpöytäympäristön tiedostonhallinta.
- **Dolphin:** KDE Plasma -työpöytäympäristön oletustiedostonhallinta.
- **Thunar:** Xfce-työpöytäympäristön oletustiedostonhallinta.
- **KDE-valikkoeditori:** KDE Plasma -työpöytäympäristöön tarkoitettu työkalu, jonka avulla voit tarkastella ja muokata .desktop-tiedostoja.

Nämä tiedostonhallintaohjelmat ja työpöytäympäristöt tarjoavat graafisen käyttöliittymän .desktop-tiedostojen hallintaan. Niiden avulla voit tarkastella ja muokata .desktop-tiedostojen ominaisuuksia, luoda sovellusten käynnistysohjelmia ja järjestää pikakuvakkeita sovellusvalikoissa tai työpöydällä.

.desktop-tiedostot ovat pelkkiä tekstitiedostoja, joten voit myös avata ja muokata niitä valitsemallasi tekstieditorilla. Napsauta vain hiiren kakkospainikkeella .desktop-tiedostoa ja valitse Avaa sovelluksella tai Avaa toisella sovelluksella. Valitse tekstieditori asennettujen ohjelmien luettelosta.

## Mikä on DESKTOP-tiedoston muoto?

.desktop-tiedostomuoto noudattaa tiettyä rakennetta ja muotoa. Se on pelkkä tekstitiedosto, jossa on joukko avain-arvo-pareja, jotka on järjestetty osiin. Tässä on yleiskatsaus formaatista:

- **Osioiden otsikot:** Jokainen osio alkaa hakasulkeisiin ([]) suljetulla otsikolla. Ensisijaisen osan nimi on yleensä [Desktop Entry], joka sisältää sovelluksen tai käynnistysohjelman tärkeimmät metatiedot.
- **Avain-arvo-parit:** Jokaisessa osiossa määrität ominaisuudet käyttämällä avain-arvo-pareja. Muoto on Key=Arvo. Avain tunnistaa ominaisuuden ja arvo antaa vastaavat tiedot.
- **Ominaisuuden syntaksi:** Ominaisuusarvot voivat olla erityyppisiä, mukaan lukien merkkijonot, loogiset arvot, tiedostopolut tai luettelot. Kunkin ominaisuuden arvon muoto riippuu sen tyypistä.
- **Kommentit:** Voit sisällyttää kommentteja .desktop-tiedostoon käyttämällä #-symbolia. Kaikki, joka seuraa numeroa # verkossa, katsotaan kommentiksi ja jätetään huomiotta.

## Viitteet
* [Työpöytätiedostot](https://www.baeldung.com/linux/desktop-entry-files)


