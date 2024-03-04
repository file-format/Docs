{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPCACHE failas – HTML5 talpyklos manifesto failo formatas",
  "description": "Sužinokite, kas yra APPCACHE failas ir API, kurios gali kurti ir atidaryti APPCACHE failus.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcach-lte"
}
},
  "lastmod": "2022-08-05"
}

## Kas yra APPCACHE failas?

APPCACHE failas yra tekstinis failas, kuriame yra išteklių, kuriuos naršyklės turi saugoti talpykloje, kad būtų galima pasiekti žiniatinklio programas neprisijungus, sąrašas. Tai naudinga, kai nėra interneto ryšio. Esant tokiai situacijai, naršyklė naudoja neprisijungus pasiekiamus talpyklos išteklius, kad suteiktų prieigą prie žiniatinklio turinio. APPCACHE faile yra žiniatinklio išteklių, pvz., vaizdų (pavyzdžiui, **[PNG](/image/png/)**, **[WEBP](/image/webp/)** ir kt.), stiliaus lapų **([CSS])(/web/css/) )** ir scenarijaus failus (pvz., Javascript **[JS](/web/js/)** failus).

Programos, kurios gali **atidaryti APPCACHE failus**, apima žiniatinklio naršykles, pvz., Google Chrome, Safari ir Firefox.

## APPCACHE failo formatas – daugiau informacijos

APPCACHE failai yra paprasti tekstiniai failai, suteikiantys prieigą prie tinklalapių neprisijungus, kad būtų galima veikti be interneto ryšio. APPCACHE buvimas nurodo puslapį kaip pasiekiamą neprisijungus.

### Kaip pateikti nuorodą į APPCACHE failą?

Jūsų HTML puslapyje APPCACHE failas nurodomas taip.

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE manifesto failo struktūra

Paprastas APPCACHE manifesto failas atrodo taip.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Tai paprasčiausias pavyzdys, gali būti ir sudėtingesnių struktūrų.

## APPCACHE manifesto privalumai

Talpyklos sąsajos naudojimas suteikia žiniatinklio programoms šiuos privalumus.

 1. Naršymas neprisijungus – talpyklos sąsaja suteikia galutiniams vartotojams galimybę naršyti visą svetainę, kai jie neprisijungę
 1. Greitis – talpykla leidžia greitai pasiekti neprisijungus pasiekiamą turinį tiesiai iš disko
 1. Prieinamumas visą laiką – jei jūsų svetainė neveiks, naudotojai vis tiek turės prieigą prie žiniatinklio turinio ir galės naudotis neprisijungus

## Nuorodos

 * [AppCache manifesto vadovas pradedantiesiems](https://web.dev/appcache-beginner/)

