{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "JSON", "Fișier arhivă"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - Format de fișier arhivă HTTP",
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier HAR și API-urile care pot crea și deschide fișierul HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Ce este un fișier HAR?

Un fișier cu fișier .har ([HTTP](/ro/web/http/) Archive) este un fișier de arhivă HTTP care stochează datele de sesiune transferate prin mai multe browsere (cum ar fi Chrome, Safari, IE, Firefox etc.) în [JSON](/ro/web/json/) format de fișier. Datele transferate pe internet între server și client (în acest caz browserul utilizatorului) conțin anteturi HTTP de solicitare și răspuns care sunt stocate în fișierul HAR. În plus, conține informații detaliate despre datele de performanță despre paginile web încărcate în browser. Fișierele HAR pot fi deschise în orice editor de text, cum ar fi Notepad pe sistemul de operare Microsoft Windows și TextEdit pe Apple MacOS.

## Format fișier HAR - Mai multe informații

Fișierele HAR stochează informații despre sesiune în fișier text simplu, folosind formatul JSON popular. Specificațiile pentru formatul fișierului HAR au fost produse de Web Performance Group al World Web Consortium (W3C), dar nu au putut fi publicate. Cu toate acestea, a definit cu succes un format de arhivare pentru tranzacțiile HTTP.

Pe lângă monitorizarea transferului informațiilor despre solicitare și răspuns, fișierele HAR sunt folosite de dezvoltatori pentru a înregistra performanța browserului web în ceea ce privește viteza de încărcare a paginii, durata de încărcare a conținutului, conținutul încărcat, interogările executate pentru a obține răspunsul de la browser și multe altele. .

## De ce să folosiți fișierele HAR?

Fișierele HAR pot fi utile în îmbunătățirea performanței unui site web prin evaluarea timpilor lungi de încărcare, a timpilor de randare a paginii și a timpilor de răspuns. Fișierele HAR pot fi analizate pentru a găsi orice astfel de probleme și pentru a rezolva orice probleme cu site-ul web pentru îmbunătățirea performanței.

## Cum se generează fișierul HAR?

Deci, cum se generează un fișier HAR? Ei bine, asta depinde de tipul de browser pe care îl utilizați pentru a genera un fișier HAR. În acest ghid, enumerăm pașii pentru browserul Google Chrome. Metodele de generare a fișierelor HAR folosind Safari, Firefox etc. pot fi căutate cu ușurință pe internet și urmărite.

### Pași pentru a genera fișierul HAR folosind Google Chrome

Următorii pași pot fi efectuati pe o pagină web în care se confruntă probleme.

1. Deschideți pagina web în Google Chrome unde a apărut problema.
1. Deschideți instrumentul de dezvoltare (inspectați elementul).
1. Mergeți în partea stângă a panoului pentru a începe înregistrarea fișierului. Există un mic buton rotund roșu în această secțiune.
1. Faceți clic pe „Șterge pictograma” pentru a șterge toate înregistrările de jurnal păstrate în browser.
1. Pentru a salva conținutul dorit, așa cum se arată mai sus, faceți clic dreapta și faceți clic pe „Salvare ca fișier HAR”

## Referințe

* [Format de fișier HAR - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))

