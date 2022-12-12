{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier de limbaj de marcare a dispozitivului portabil",
  "description":"Aflați despre formatul de fișier HDML și despre API-urile care pot crea și deschide fișiere HDML.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Ce este un fișier HDML?

Un fișier cu extensia .hdml (Handheld Device Markup Language) este un limbaj de marcare pentru crearea de pagini web pentru dispozitive electronice portabile, cum ar fi computere portabile, smartphone-uri și dispozitive de afișare a informațiilor. Se spune că HDML este o extensie a limbajului [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language). HDML este similar cu HTML, dar pentru dispozitive wireless și portabile care au ecrane mici, cum ar fi PDA, telefoane mobile și așa mai departe. A fost înlocuit cu WML pentru care a acționat ca o influență importantă.

## Format de fișier HDML - Mai multe informații

HDML este un limbaj de marcare pentru dispozitivele portabile care se bazează pe etichete de marcare similare cu HTML. HDML a fost trimis la W3C pentru standardizare, dar nu a devenit niciodată un standard. Specificațiile sale de format de fișier sunt, totuși, disponibile pe [site-ul W3](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) pentru referință. [Sintaxa pentru limbajul HDML](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) este disponibilă pentru referință de către dezvoltatori și poate fi folosită pentru dezvoltarea de exemple de aplicații.

## Elemente HDML

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

