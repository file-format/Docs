{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","fișier mhtml", "format fișier mhtml", "tip fișier mhtml", "fișier", "tip", "ce este un fișier mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML – fișier HTML MIME",
  "description":"Aflați despre formatul de fișier MHTML și despre API-urile care pot crea și deschide fișiere MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier MHTML?

Fișierele cu extensia MHTML reprezintă un format de arhivă a paginii web care poate fi creat de un număr de aplicații diferite. Formatul este cunoscut ca format de arhivă deoarece salvează codul web **[HTML](/ro/web/html/)** și resursele asociate într-un singur fișier. Aceste resurse includ orice legat de pagina web, cum ar fi imagini, applet-uri, animații, fișiere audio și așa mai departe. Fișierele MHTML pot fi deschise într-o varietate de aplicații, cum ar fi Internet Explorer și Microsoft Word. Microsoft Windows folosește formatul de fișier MHTML pentru înregistrarea scenariilor de probleme observate în timpul utilizării oricărei aplicații pe Windows care ridică probleme. Formatul de fișier MHTML codifică conținutul paginii similar cu specificațiile definite în mesaj/rfc822, care este specificații legate de e-mail cu text simplu. Specificațiile reale ale formatului sunt detaliate în [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Format de fișier MHTML

MHTML este cunoscut și sub denumirea de Encapsulation MIME a documentelor HTML agregate pentru capacitatea sa de a codifica paginile web HTML împreună cu resursele sale într-o singură arhivă web. Conform specificațiilor RFC 2557, un document agregat este un mesaj codificat MIME care conține o resursă rădăcină (obiect), precum și alte resurse legate de acesta prin intermediul URI-urilor. Astfel de alte resurse pot fi reprezentarea de imagini inline, foi de stil, applet-uri etc. În plus, acestea pot fi rădăcina altor documente multimedia. Specificațiile complete ale documentului pentru formatul de fișier MHTML sunt detaliate în [RFC 2557](https://tools.ietf.org/html/rfc2557) și ar trebui să fie consultate pentru orice tip de dezvoltare a aplicației pentru citirea/scrierea acestui format de fișier. Standardul specifică că părțile corpului la care se face referire pot fi identificate fie printr-un Content-ID, fie printr-o Content-Location.

### Anteturi de conținut MIME

Un antet de conținut MIME, Content-Location, este definit pentru a rezolva referințele URI la resurse din alte părți ale corpului. Acest antet poate apărea în orice titlu de mesaj sau conținut.

### Antet Conținut-Locație

O locație de conținut este o reprezentare a unui URI care etichetează conținutul unei părți a corpului unde este plasat. Valoarea sa poate fi un URI absolut sau relativ. Poate fi folosit pentru a eticheta o resursă care nu poate fi recuperată de către unii sau toți destinatarii unui mesaj. Un singur mesaj poate avea un singur antet Content-Location. Exemplu de structură în mai multe părți/înrudite care conține părți ale corpului cu ambele etichete Content-Location și Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI-uri ale agregatelor MHTML

URI-ul agregatului MHTML este diferit de cel al URI-ului său rădăcină. Câmpul de antet Content-Location ar trebui să se aplice întregului agregat dacă este utilizat în antetul unui antet cu mai multe părți/înrudit. În mod similar, setul de resurse extrase poate fi diferit de setul de resurse extrase folosind locațiile de conținut ale părților sale atunci când URI-ul care se referă la agregatul MHTML este folosit pentru a extrage acest agregat. De exemplu, preluarea unui agregat MHTML poate returna o versiune veche, în timp ce preluarea URI-ului rădăcină și a obiectelor sale conectate în linie poate returna o versiune mai nouă.

## Referințe

* [Encapsularea MIME a documentelor agregate - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Format de fișier MHTML - După Wikipedia](https://en.wikipedia.org/wiki/MHTML)

