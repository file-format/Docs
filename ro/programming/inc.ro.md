{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Extensie de fișier INC - Ce este un fișier INC?",
  "description":"Aflați despre INC Include formatul de fișier și API-urile care pot crea și deschide fișiere INC.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Ce este un fișier INC?

Un fișier INC este un fișier include care este utilizat de codul sursă al programului software pentru a face referire la informațiile antetelor. Este similar cu [formatul de fișier .h](/ro/programming/h/) și conține declarații, funcții, anteturi sau macrocomenzi care pot fi reutilizate de fișierele de cod sursă, cum ar fi C++. Fișierele INC sunt utilizate de o varietate de limbaje de programare precum C, [C++](/ro/programming/cpp/), Pascal, [PHP](/ro/programming/php/) și [Java](/ro/programming/java/). Editorii de text precum Microsoft Notepad, Notepad++ și TextEdit pot fi utilizați pentru a deschide fișiere INC.

## Format de fișier INC - Mai multe informații

Un fișier INC este salvat ca fișier text simplu cu toate declarațiile incluse conform sintaxei declarației. Un fișier INC poate face referire și la alte fișiere INC. Odată creat, fișierul INC devine parte a proiectului și poate fi referit din fișiere sursă, cum ar fi C++. Acesta poate fi referit prin mai multe fișiere sursă pentru a evita orice duplicare.

## Conținutul fișierului INC

Fișierele INC pot include următoarele informații.

**`Variabile`** - În cazul programării orientate pe obiecte (OOP), un fișier antet de clasă conține definiții ale tuturor variabilelor la nivel de clasă care sunt accesibile prin fișierele codului sursă de implementare

**`Declarația metodelor`** - Toate declarațiile metodelor sunt incluse în fișierele antet .h pentru a fi accesibile în mai multe fișiere de implementare.

**`Non-Inline Function Definitions`** - Fișierele antet pot conține, de asemenea, definiții ale unei metode non-inline.

## Dezavantajul utilizării fișierului INC în PHP

PHP sunt scripturi pe server care rulează pe server și returnează rezultatele către paginile web care apelează. Dacă un fișier PHP face referire la un fișier INC și serverul nu este configurat pentru a analiza fișiere .inc (ceea ce este foarte comun), un utilizator poate vizualiza codul sursă php în fișierul .inc vizitând directorul URL. Deci, trebuie să fiți atenți când utilizați fișiere INC ca fișiere include în PHP.

## Referințe

* [Folosirea INC în PHP](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

