{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Comhad APPCACHE - Formáid Chomhaid Manifest HTML5 Taisce",
  "description": "Foghlaim faoi cad is comhad APPCACHE ann agus APIanna ar féidir comhaid APPCACHE a chruthú agus a oscailt.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcach-gae"
}
},
  "lastmod": "2022-08-05"
}

## Cad is comhad APPCACHE ann?

Is comhad téacs é comhad APPCACHE ina bhfuil liosta na n-acmhainní atá le taisceadh ag brabhsálaithe le haghaidh rochtain as líne ar na feidhmchláir ghréasáin. Tá sé seo úsáideach nuair nach bhfuil aon nasc idirlín. Sa chás sin, úsáideann an brabhsálaí na hacmhainní taisce as líne chun rochtain a sholáthar ar inneachar an ghréasáin. Tá acmhainní gréasáin ar nós íomhánna i gcomhad APPCACHE (mar shampla **[PNG](/image/png/)**, **[WEBP](/image/webp/)**, etc.), stílbhileoga **([CSS])(/web/css/ )**, agus comhaid scripte (amhail comhaid Javascript **[JS](/web/js/)**).

Áirítear le feidhmchláir ar féidir leo **comhaid APPCACHE a oscailt** brabhsálaithe gréasáin ar nós Google Chrome, Safari, agus Firefox.

## Formáid Chomhaid APPCACHE - Tuilleadh Eolais

Is comhaid téacs simplí iad comhaid APPCACHE, a sholáthraíonn rochtain as líne ar leathanaigh ghréasáin chun iad a rith gan nasc idirlín. Ainmníonn láithreacht APPCACHE leathanach mar atá ar fáil as líne.

### Conas Tagairt a dhéanamh do chomhad APPCACHE?

I do leathanach HTML, déantar tagairt do chomhad APPCACHE mar seo a leanas.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struchtúr chomhad Manifest APPCACHE

Breathnaíonn comhad follasach simplí APPCACHE mar seo a leanas.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Is sampla simplí é seo agus is féidir struchtúir níos casta a bheith i láthair freisin.

## Buntáistí APPCACHE Manifest

Tugann úsáid comhéadan taisce na buntáistí seo a leanas d'fheidhmchláir ghréasáin.

 1. Brabhsáil As Líne - Tugann an comhéadan taisce deis do na húsáideoirí deiridh do shuíomh iomlán a bhrabhsáil nuair a bhíonn siad As Líne
 1. Luas - cuireann taisce ar chumas rochtain ardluais ar ábhar as líne go díreach ón diosca
 1. Inrochtaineacht an t-am ar fad - Sa chás go laghdaítear do shuíomh, beidh rochtain fós ag úsáideoirí ar an ábhar Gréasáin agus beidh siad in ann an taithí as líne a fháil

## Tagairtí

 * [Treoir do Thosaitheoirí ar AppCache Manifest](https://web.dev/appcache-beginner/)

