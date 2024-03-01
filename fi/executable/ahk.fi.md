{
  "date": "2022-04-25",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi AHK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata AHK-tiedostoja.",
  "title": "AHK-tiedostomuoto - AutoHotkey-skriptitiedosto",
  "linktitle": "AHK",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ah-fik"
}
},
  "lastmod": "2022-04-25"
}

## Mikä on AHK-tiedosto?

AHK-tiedosto on AutoHotkey-ohjelmistosovelluksella luotu komentosarjatiedosto, jota käytetään tehtävien automatisointiin Microsoft Windowsissa. Se sisältää ohjeet tehtävien automatisoimiseksi pikanäppäimillä, joita voidaan käyttää välittömien toimien suorittamiseen. Tiedoston suorittaa AutoHotkey ja kaikki toiminnot suoritetaan peräkkäin. AHK-tiedostot ovat riittävän tehokkaita monimutkaisten tehtävien suorittamiseen pikanäppäimillä määritettyjen pikanäppäimien avulla. AHK-tiedostoja voidaan avata tekstieditoreilla, kuten Microsoft Notepad ja Notepad++.

## AHK tiedostomuoto

AHK-tiedostot tallennetaan levylle tekstitiedostoina ja sisältävät koodirivejä, jotka voidaan suorittaa AutoHotkey-toiminnolla. AutoHotkey on ilmainen, avoimen lähdekoodin komentosarjakieli, jonka avulla käyttäjät voivat luoda yksinkertaisista monimutkaisiin komentosarjoja suorittaakseen toimintoja, kuten lomakkeiden täyttöjä, automaattista napsautusta, makrojen suorittamista jne. AHK-tiedosto voi suorittaa vähintään yhden toiminnon ja sitten poistua .

Saatavilla on työkaluja, joilla AHK voidaan muuntaa [Exe](/executable/exe/)-tiedostoiksi.

### AHK Esimerkki

Seuraava esimerkki käyttää Win+Z-näppäintä Microsoft Notepadin suorittamiseen tai tuo sen eteen, jos se on jo käynnissä.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Kuinka luon AHK-tiedoston?

Seuraavien vaiheiden avulla voidaan luoda AHK-tiedosto. Nämä olettavat, että AutoHotkey on jo asennettu koneeseen.

* Napsauta hiiren kakkospainikkeella työpöytääsi.

* Etsi valikosta "Uusi".

* Napsauta "AutoHotkey Script" "Uusi"-valikon sisällä.

* Anna skriptille uusi nimi.

* Etsi äskettäin luotu tiedosto työpöydältäsi ja napsauta sitä hiiren kakkospainikkeella.

* Napsauta "Muokkaa komentosarjaa".

* Ikkunan olisi pitänyt avautua, luultavasti Muistio.

* Tallenna tiedosto.


## Viitteet

* [AutoHotkey](https://www.autohotkey.com/)

* [Erätiedosto - Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)


