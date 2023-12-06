{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier MASTER - Format fișier de pagină principală ASP.NET",
  "description" :"Aflați despre formatul fișierului MASTER și API-urile pentru a crea și deschide fișiere MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Ce este un fișier MASTER?

Un fișier MASTER este un fișier șablon de pagină web principal creat cu ASP.NET. Este folosit ca punct de plecare pentru crearea mai multor pagini care au același aspect și setări ca fișierul MASTER. Fișierul șablon MASTER include setări pentru antet, meniuri de navigare, subsol, font și informații despre stil. Utilizarea unui fișier MASTER ajută la crearea rapidă a mai multor pagini web.

Puteți deschide un fișier MASTER utilizând Microsoft Visual Studio 2022 și versiuni ulterioare.

## Format de fișier MASTER - Mai multe informații

Un fișier MASTER este creat și salvat în format de fișier HTML și este similar cu orice alt fișier de pagină web. Este împărțit în secțiuni editabile și needitabile. Secțiunile editabile sunt cele care pot fi modificate pentru a satisface cerințele utilizatorului. Secțiunile care nu pot fi editate sunt incolore când fișierul MASTER este deschis în Microsoft Visual Studio.

Paginile principale constau din două piese, adică pagina principală în sine și una sau mai multe pagini de conținut.

### Pagina MASTER

Pagina master are extensia .master și este realizată în ASP.NET. Are un aspect predefinit care cuprinde text static, etichete HTML și controale pe partea serverului. În paginile obișnuite .aspx, este utilizată directiva @ Page. În cazul fișierelor .master, aceasta este înlocuită cu directiva @ Master.

### Pagini de conținut

O pagină de conținut reprezintă conținutul pentru comenzile substituenților paginii master. Acestea sunt pagini .aspx care sunt de fapt codul din spatele paginii master. Paginile de conținut sunt legate folosind directiva @ Page prin includerea unui atribut MasterPageFile care indică pagina principală care va fi utilizată, așa cum se arată mai jos.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referințe

* [Prezentare generală a paginilor principale ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

