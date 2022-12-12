{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier HAML - Fișier cod sursă Haml",
  "description":"Aflați despre formatul de fișier HAML și despre API-urile care pot crea și deschide fișierul HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Ce este un fișier HAML?

Un fișier HAML este un fișier HTML cu limbaj de marcare abstracție care conține cod sursă scris în limbajul [Haml](https://haml.info/). Poate fi folosit ca înlocuitor pentru ERB (scripturi de șablon Ruby). Fișierul HAML conține codul sursă șablon pentru generarea HTML-ului unui document web. Fișierele ERB pot fi înlocuite prin simpla înlocuire a acestor fișiere din folderul aplicație/vizualizări în Haml prin schimbarea extensiei fișierului. Fișierele HAML pot fi deschise cu orice editor de text, cum ar fi Microsoft Notepad, Notepad++, Apple TextEdit,

## Format de fișier HAML

Fișierele HAML sunt fișiere sursă salvate pe disc ca fișiere text simplu. Conține cod scris în sintaxa HAML. HAML înlocuiește etichetele **<>** cu semnul **%** pentru a face codul mai simplu și mai ușor. Fișierele ERB pot fi înlocuite cu HAML, așa cum se arată în următorul exemplu simplu.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML Exemplu

Următorul este un exemplu Hello World de HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
care redă următoarea ieșire HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referințe

* [HAML - Github](https://github.com/haml/haml)

