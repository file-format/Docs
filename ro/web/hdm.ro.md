{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier HDM - Fișier limbaj de marcare a dispozitivului portabil",
  "description":"Aflați despre formatul de fișier HDM și despre API-urile care pot crea și deschide fișiere HDM.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Ce este un fișier HDM?

Un fișier HDM este un fișier de pagină web cu limbaj de marcare care este creat în limbajul HDML (Handheld Device Markup Language). Conține etichete de marcare similare cu limbajul [HTML](/ro/web/html/), dar este conceput pentru dispozitive electronice portabile, cum ar fi smartphone-urile și PDA-urile. [Specificațiile formatului fișierului HDML](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) au fost trimise la W3C pentru standardizare, dar nu au putut deveni un standard. HDM se bazează pe specificațiile de format de fișier [HDML](/ro/web/hdml/) disponibile pe site-ul web W3.

## Format de fișier HDM - Mai multe informații

Fișierul HDM constă din etichete de marcare care sunt redate pe site-ul web proiectat vizual pe dispozitive portabile. Fișierele HDM sunt copiate pe dispozitive utilizând protocolul HDTP (Handheld Device Transport Protocol) în loc de protocolul HTTP care este utilizat pentru paginile HTML.

## Elemente de fișiere HDML

Urmează o serie de elemente care oferă un mediu de rulare pentru HDML și sunt denumite agent de utilizator.

|Element|Descriere|
---|---|
|Carduri|Acesta este elementul fundamental al HDML și afișează și permite utilizatorului să interacționeze cu carduri de informații. |
|Decks|Cartile HDML sunt grupate in pachete. Un pachet HDML este similar cu o pagină HTML prin faptul că este identificat prin URL [RFC1738] și este unitatea de conținut solicitată de la un server și stocată în cache de agentul utilizator.|
|Acțiuni|Acțiunile pot fi de tip PREV, SOFT1-SOFT8 și HELP. Acestea sunt abstracte și sunt acceptate în interfața cu utilizatorul într-un mod specific pentru agentul utilizatorului.|
|Activități|O activitate este ca un grup de carduri înrudite care îndeplinesc o funcție logică. Acestea se pot întinde pe una sau mai multe punți. Modelul de navigare și stare HDML este structurat în jurul activităților.|
|Navigație bazată pe istoric|Agentul utilizator păstrează un istoric al cardurilor afișate utilizatorului. Fiecare card care este accesat este adăugat la istoricul cardului. Agentul utilizator permite utilizatorului să navigheze cu ușurință înapoi la cardul anterior din istoric.|

## Referințe

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [Specificații HDML - Școli W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

