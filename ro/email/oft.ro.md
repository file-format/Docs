{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - Fișier șablon de e-mail Microsoft Outlook",
  "description":"Aflați despre formatul de fișier OFT și despre API-urile care pot crea și deschide fișiere OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier OFT?

Fișierele cu extensia .oft sunt fișiere șablon care sunt create folosind Microsoft Outlook. Setul de aspect preformatat pentru șabloanele de mesaje este apoi folosit pentru a trimite e-mailuri cu informații comune, pentru a economisi timp. Astfel de fișiere pot fi generate prin crearea unui nou e-mail, adăugarea informațiilor necesare și apoi folosind meniul derulant Salvare ca șablon Office (.oft) din Microsoft Outlook. Utilizatorii pot deschide fișierele OFT făcând dublu clic pe ele și se va deschide în aplicația asociată pe acel sistem special.

## Structura fișierului OFT ##

Formatul de fișier .OFT utilizează la bază formatul de fișier [MSG](/ro/email/msg/). Singura diferență este că fișierele OFT au CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) ca clasă de stocare (WriteClassStg), în timp ce fișierele MSG folosesc CLSID_MailMessage ({00020D0B-0000000000000000000000000000000000000000000000000000000000000000000000000000000000) a

Formatul CFB_3 este baza fișierului MSG. Paradigma se bazează pe conceptele de stocare și fluxuri, destul de aproape de directoare și fișiere. Prin urmare, o diferență majoră în primul este întreaga ierarhie, ambalată într-un fișier distinct, numit fișier compus. Obiectele constituie fișierele de mesaje și constau dintr-o singură proprietate sau colecțiile acesteia. Această capacitate facilitează aplicațiile de a stoca date complexe și structurate într-un singur fișier. Acest format specifică, de asemenea, mai multe stocări, fiecare stocare reprezentând obiectul Message ca o componentă majoră. Aceste stocări conțin un număr de fluxuri reprezentând o proprietate a acelei componente. De asemenea, este posibilă imbricarea depozitului.

### Proprietăți OFT

La nivelul superior al fișierului .msg, stocările conțin fluxuri care stochează proprietăți în ele. Proprietățile pot fi clasificate după cum urmează:

* Proprietăți de lungime fixă
* Proprietăți de lungime variabilă
* Proprietăți cu valori multiple

Indiferent de categorie, o proprietate este fie etichetată, fie denumită. Cu toate acestea, sunt necesare informații de cartografiere adecvate pentru proprietățile numite, așa cum este specificat de stocarea lor de cartografiere.

### Depozite OFT

Stocările constituie componentele cheie ale obiectului Message. Formatul de fișier MSG indică următoarele stocări:

### Structura de nivel superior

Obiectul mesaj reprezintă întregul nivel superior al formatului de fișier Msg. În funcție de tipul, proprietățile, numărul de obiecte destinatare și atașament, un obiect mesaj poate avea diferite stocări de flux în fișierul său .MSG corespunzător.

#### Relația cu alte structuri

Formatul de fișier MSG/OFT are următoarele relații cu alte structuri:

* Baza .msg este formatul fișierului binar al fișierului compus.
* Proprietățile utilizate de Message and Attachment Object Protocol sunt utilizate de acest format.

## Referințe

* [[MS-OXMSG]: Format de fișier Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

