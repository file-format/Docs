{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier APPCACHE - Format fișier HTML5 Cache Manifest",
  "description" :"Aflați despre ce este un fișier APPCACHE și API-urile care pot crea și deschide fișiere APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Ce este un fișier APPCACHE?

Un fișier APPCACHE este un fișier text care conține lista de resurse care urmează să fie stocate în cache de către browsere pentru acces offline la aplicațiile web. Acest lucru este util atunci când nu există conexiune la internet. Într-o astfel de situație, browserul utilizează resursele cache offline pentru a oferi acces la conținutul web. Fișierul APPCACHE conține resurse web, cum ar fi imagini (de exemplu **[PNG](/ro/image/png/)**, **[WEBP](/ro/image/webp/)** etc.), foi de stil **([ CSS])(/ro/web/css/)** și fișiere script (cum ar fi fișierele Javascript **[JS](/ro/web/js/)**).

Aplicațiile care pot **deschide fișierele APPCACHE** includ browsere web precum Google Chrome, Safari și Firefox.

## Format de fișier APPCACHE - Mai multe informații

Fișierele APPCACHE sunt fișiere text simple, care oferă acces offline la pagini web pentru a rula fără conexiune la internet. Prezența APPCACHE desemnează o pagină ca fiind disponibilă offline.

### Cum se face referire la un fișier APPCACHE?

În pagina dvs. HTML, un fișier APPCACHE este referit după cum urmează.

```
<html manifest="example.appcache">
  ...
</html>
```

## Structura unui fișier Manifest APPCACHE

Un simplu fișier manifest APPCACHE arată după cum urmează.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Acesta este cel mai simplu exemplu și pot fi prezente și structuri mai complexe.

## Avantajele APPCACHE Manifest

Utilizarea interfeței cache oferă aplicațiilor web următoarele avantaje.

1. Navigare offline - Interfața cache oferă utilizatorilor finali să vă răsfoiască întregul site atunci când sunt offline
1. Viteză - memoria cache permite accesul de mare viteză la conținut offline direct de pe disc
1. Accesibilitate tot timpul - În cazul în care site-ul dvs. se defectează, utilizatorii vor avea în continuare acces la conținutul web și vor putea obține experiența offline

## Referințe

* [Un ghid pentru începători pentru manifestul AppCache](https://web.dev/appcache-beginner/)

