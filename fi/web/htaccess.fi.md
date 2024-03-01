{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTACCESS-tiedosto - Apache HTACCESS -tiedostomuoto",
  "description": "Tiedostomuoto-opas oppiaksesi, mikä on HTACCESS-tiedosto",
  "linktitle": "HTACCESS",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htacces-fis"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on HTACCESS-tiedosto?

HTACCESS-tiedosto on Apache-määritystiedosto, joka mahdollistaa verkkosivuston eri kansioiden/hakemistojen asetusten muuttamisen. Se sisältää hakemistoon ja alihakemistoihin sovellettavia konfigurointiohjeita.

HTACCESS-tiedosto suorittaa useita tarkistuksia, kuten määrittää verkkosivuston hakemistosivun, listaa 404 (Sivua ei löydy) -virhesivun, suorittaa 301- tai 302-sivun uudelleenohjaukset, estää pääsyn tietystä IP-osoitteesta tai muista verkkosivustoista. Näin ollen .htaccess-tiedostojen käyttö hidastaa Apache HTTP -palvelimesi yleistä suorituskykyä.

## HTACCESS tiedostomuoto

HTACCESS-tiedostot tallennetaan levylle tekstitiedostomuodossa. Tämä tarkoittaa, että voit avata ja muokata näitä tiedostoja missä tahansa tekstieditorissa. Ei ole nimeä ennen . .htaccess-tiedostossa, mikä osoittaa, että se on kansiossa piilotettu tiedosto.

## HTACCESS-tiedoston yleiset käyttötavat

Viisi yleistä HTACCESS-tiedoston käyttötapaa ovat seuraavat.

### Mod_Rewrite

HTACCESS-tiedostoa voidaan käyttää määrittämään ja muuttamaan tapaa, jolla verkkosivuston URL-osoitteet ja verkkosivut näytetään käyttäjille.

### Todennus

Todennus voidaan saavuttaa .htaccessilla luomalla passowrd-tiedosto nimeltä .htpasswd. Näin sivuston vierailijat voivat antaa salasanan, jos he haluavat vierailla tietyssä verkkosivun osassa.

### Mukautetut virhesivut

Voit luoda mukautettuja virhesivuja, kuten 400 virheellinen pyyntö, 401 valtuutus vaaditaan, 403 kielletty sivu, 404 tiedostoa ei löydy ja 500 sisäinen virhe .htaccess-tiedostolla. Nämä kuitenkin hidastavat palvelimen suorituskykyä, koska nämä kaikki tarkistukset suoritetaan, kun sivuja avataan.

### MIME-tyypit

Apache HTACCESS -tiedostoja voidaan muokata sisältämään Multipurpose Internet Mail Extensions (MIME) -tyyppejä. Näin palvelimesi voi tukea sellaisten sovellustiedostojen toimittamista, joita sivusto ei tue.

### SSI

Server Side Includes (SSI) toimii erinomaisena ajansäästönä verkkosivustolla. SSI voidaan ottaa käyttöön lisäämällä hte seuraava koodi .htaccess-tiedostoosi.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Esimerkki Apache HTACCESS -tiedostosta

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Viitteet

* [Apache HTTP Server Tutorial: .htaccess files](https://httpd.apache.org/docs/current/howto/htaccess.html)

