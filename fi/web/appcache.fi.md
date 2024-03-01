{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPCACHE-tiedosto – HTML5-välimuistin manifestitiedostomuoto",
  "description": "Opi mikä on APPCACHE-tiedosto ja API:t, jotka voivat luoda ja avata APPCACHE-tiedostoja.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcach-fie"
}
},
  "lastmod": "2022-08-05"
}

## Mikä on APPCACHE-tiedosto?

APPCACHE-tiedosto on tekstitiedosto, joka sisältää luettelon resursseista, jotka selaimet tallentavat välimuistiin verkkosovellusten offline-käyttöä varten. Tämä on hyödyllistä, kun Internet-yhteyttä ei ole. Tällaisessa tilanteessa selain käyttää offline-välimuistiresursseja tarjotakseen pääsyn verkkosisältöön. APPCACHE-tiedosto sisältää verkkoresursseja, kuten kuvia (esim. **[PNG](/image/png/)**, **[WEBP](/image/webp/)** jne.), tyylisivuja **([CSS])(/web/css/) )** ja komentosarjatiedostot (kuten Javascript **[JS](/web/js/)** -tiedostot).

Sovelluksia, jotka voivat **avata APPCACHE-tiedostoja**, ovat verkkoselaimet, kuten Google Chrome, Safari ja Firefox.

## APPCACHE-tiedostomuoto - lisätietoja

APPCACHE-tiedostot ovat yksinkertaisia tekstitiedostoja, jotka tarjoavat offline-käytön verkkosivuille ilman Internet-yhteyttä. APPCACHE:n olemassaolo määrittää sivun olevan käytettävissä offline-tilassa.

### Kuinka viitata APPCACHE-tiedostoon?

HTML-sivullasi viitataan APPCACHE-tiedostoon seuraavasti.

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE-luettelotiedoston rakenne

Yksinkertainen APPCACHE-luettelotiedosto näyttää seuraavalta.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Tämä on yksinkertaisin esimerkki, ja olemassa voi olla myös monimutkaisempia rakenteita.

## APPCACHE Manifestin edut

Välimuistirajapinnan käyttö antaa verkkosovelluksille seuraavat edut.

 1. Offline-selaaminen – välimuistin käyttöliittymä antaa loppukäyttäjille mahdollisuuden selata koko sivustoasi, kun he ovat offline-tilassa
 1. Nopeus - välimuisti mahdollistaa nopean pääsyn offline-sisältöön suoraan levyltä
 1. Koko ajan saavutettavuus – Jos sivustosi kaatuu, käyttäjät pääsevät edelleen verkkosisältöön ja voivat saada offline-kokemuksen

## Viitteet

 * [AppCache Manifestin aloittelijaopas](https://web.dev/appcache-beginner/)

