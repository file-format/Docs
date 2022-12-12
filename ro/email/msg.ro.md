{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG – Format de e-mail Microsoft Outlook",
  "description":"Aflați despre formatul de fișier MSG și despre API-urile care pot crea și deschide fișiere MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier MSG?

MSG este un format de fișier folosit de [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) și Exchange pentru a stoca mesaje de e-mail , contact, programare sau alte sarcini. Astfel de mesaje pot conține unul sau mai multe câmpuri de e-mail, cu expeditorul, destinatarul, subiectul, data și corpul mesajului, sau informații de contact, detalii despre întâlnire și una sau mai multe specificații de activitate. Proprietățile care constituie obiectul Message, inclusiv, sunt, de asemenea, o parte a fișierului MSG. Fișierul MSG are anteturi, corpul mesajului principal și hyperlink-uri ca text simplu ASCII. Fișierele MSG sunt potrivite și cu programele care au nevoie de Interfața de programare a aplicațiilor de mesagerie (MAPI) de la Microsoft.

## Structura fișierelor MSG

Formatul CFB_3 este baza fișierului MSG. Paradigma se bazează pe conceptele de stocare și fluxuri, destul de aproape de directoare și fișiere. Prin urmare, o diferență majoră în primul este întreaga ierarhie, ambalată într-un fișier distinct, numit fișier compus. Obiectele constituie fișierele de mesaje și constau dintr-o singură proprietate sau colecțiile acesteia. Această capacitate facilitează aplicațiile de a stoca date complexe și structurate într-un singur fișier. Acest format specifică, de asemenea, mai multe stocări, fiecare stocare reprezentând obiectul Message ca o componentă majoră. Aceste stocări conțin un număr de fluxuri reprezentând o proprietate a acelei componente. De asemenea, este posibilă imbricarea depozitului.

## Proprietăți Mapi

La nivelul superior al fișierului .msg, stocările conțin fluxuri care stochează proprietăți în ele. Proprietățile pot fi clasificate după cum urmează:

* Proprietăți de lungime fixă
* Proprietăți de lungime variabilă
* Proprietăți cu valori multiple

Indiferent de categorie, o proprietate este fie etichetată, fie denumită. Cu toate acestea, sunt necesare informații de cartografiere adecvate pentru proprietățile numite, așa cum este specificat de stocarea lor de cartografiere.

## Depozite

Stocările constituie componentele cheie ale obiectului Message. Formatul de fișier MSG indică următoarele stocări:

## Structura de nivel superior

Obiectul mesaj reprezintă întregul nivel superior al formatului de fișier MSG. În funcție de tipul, proprietățile, numărul de obiecte destinatare și atașament, un obiect mesaj poate avea diferite stocări de flux în fișierul său .MSG corespunzător.

### Relația cu alte structuri

Formatul de fișier Msg are următoarele relații cu alte structuri:

* Baza .msg este formatul fișierului binar al fișierului compus.
* Proprietățile utilizate de Message and Attachment Object Protocol sunt utilizate de acest format.

## Scenarii pentru a evita formatele MSG

Obiectul mesaj poate fi partajat între clienți sau magazine de mesaje care utilizează sistemul de fișiere .msg. Există puține circumstanțe în care stocarea unui obiect Message în formatul de fișier .msg nu ar fi adecvată. De exemplu:

* În cazul menținerii unei arhive independente mari, este mai bine să utilizați un format cu funcții complete în care vizualizările pot fi redate mai precis.
* Dacă receptorul este necunoscut, este posibil ca formatul să nu fie acceptat de receptor și să fie livrat privat sau irelevant.

## Exemplu de fișier MSG

Pentru a vă face o idee despre cum arată un fișier MSG, puteți descărca un [exemplu de fișier MSG](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) și îl puteți deschide pe computer pentru a-și vizualiza conținutul.

## Referințe

* [[MS-OXMSG]: Format de fișier Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

