{
  "date": "2023-03-07",
  "keywords": [
"reg tiedosto",
"mikä on reg-tiedosto",
"tiedosto",
"reg tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "REG-tiedostomuoto - Windowsin rekisteritiedosto",
  "description": "Opi REG-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata REG-tiedostoja.",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg-fi",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## Mikä on REG-tiedosto?

REG-tiedosto on tiedostomuoto, jota käytetään Windowsin rekisteritietojen tuontiin tai vientiin. Windowsin rekisteri on hierarkkinen tietokanta, joka tallentaa Windows-käyttöjärjestelmän ja asennettujen sovellusten asetukset ja asetukset. Rekisteri sisältää tietoja, kuten käyttäjäasetukset, sovellusasetukset, laitteiston ja ohjelmiston kokoonpanotiedot ja paljon muuta.

REG-tiedostolla on yleensä .reg-tiedostotunniste, ja se on pelkkä tekstitiedosto, joka sisältää sarjan rekisterimerkintöjä ja arvoja tietyssä muodossa. Muoto koostuu otsikkoosasta, joka identifioi tiedoston rekisteritiedostona, ja sen jälkeen sarjan avain- ja arvopareja, jotka edustavat rekisterimerkintöjä.

## REG-tiedostomuoto - lisätietoja

Tässä on esimerkki reg-tiedostomuodosta:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Tiedoston ensimmäinen rivi määrittää rekisterieditorin version. Seuraavat rivit sisältävät rekisterimerkinnät avainpolun muodossa, jota seuraa arvon nimi ja arvotiedot. Tässä esimerkissä reg-tiedosto sisältää kaksi merkintää: yksi, joka lisää ohjelman nimeltä Example.exe Windowsin käynnistysluetteloon, ja toinen, joka asettaa Piilotettu-arvon Windowsin Resurssienhallinnan lisäasetuksissa true.

Reg-tiedostoja voidaan luoda ja muokata tekstieditorilla, kuten Notepadilla. Niitä käytetään usein varmuuskopiointi- ja palautustarkoituksiin sekä useiden tietokoneiden määrittämiseen samoilla rekisteriasetuksilla.

## Tuo tai vie Windowsin rekisteri

REG-tiedosto on tiedostotyyppi, jota käytetään tietojen tuomiseen tai viemiseen Windowsin rekisteristä. Windowsin rekisteri on hierarkkinen tietokanta, joka tallentaa Windows-käyttöjärjestelmän ja asennettujen sovellusten asetukset ja asetukset. Rekisteri sisältää tietoja, kuten käyttäjäasetukset, sovellusasetukset, laitteiston ja ohjelmiston kokoonpanotiedot ja paljon muuta.

Reg-tiedostoja voidaan käyttää rekisterimerkintöjen luomiseen tai muokkaamiseen, ja niitä käytetään usein varmuuskopiointi- ja palautustarkoituksiin sekä useiden tietokoneiden määrittämiseen samoilla rekisteriasetuksilla. Voit lisätä uuden rekisterimerkinnän Windowsin rekisteriin reg-tiedoston avulla seuraavasti:

1. Luo uusi tekstitiedosto tekstieditorilla, kuten Notepadilla.
2. Kirjoita rekisterimerkintä oikeassa muodossa. Muoto koostuu otsikkoosasta, joka identifioi tiedoston rekisteritiedostona, ja sen jälkeen sarjan avain- ja arvopareja, jotka edustavat rekisterimerkintöjä. Tässä on esimerkki:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Tämä luo uuden avaimen nimeltä Example Ohjelmisto-avaimen alle nykyiseen käyttäjän rekisterirakenteeseen ja asettaa Setting1-arvon arvoksi Arvo1.

3. Tallenna tiedosto .reg-tiedostotunnisteella.
4. Lisää uusi rekisterimerkintä Windowsin rekisteriin kaksoisnapsauttamalla .reg-tiedostoa.

Sinua pyydetään vahvistamaan, että haluat lisätä merkinnän rekisteriin. Kun olet vahvistanut, uusi merkintä lisätään rekisteriin, ja voit vahvistaa sen Rekisterieditori-työkalulla.

## Viitteet
* [Windows Registry](https://en.wikipedia.org/wiki/Windows_Registry)


