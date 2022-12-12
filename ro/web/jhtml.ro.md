{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","fișier jhtml", "format fișier jhtml", "tip fișier jhtml", "fișier", "tip", "ce este un fișier jhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML – fișier HTML Java",
  "description":"Aflați despre formatul de fișier JHTML și despre API-urile care pot crea și deschide fișiere JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## Ce este un fișier JHTML?

Un fișier cu extensia .jhtml este un fișier [HTML](/ro/web/html/) cu cod [Java](/ro/programming/java/) care este executat pe server atunci când un client solicită această pagină într-un browser. Serverul procesează cererile, execută funcțiile Java conținute în funcție și returnează pagina în browser-ul clientului. Obiectele Java încorporate în paginile JHTML rulează pe server pentru a gestiona solicitările pentru pagini de acest tip. Fișierele JHTML pot accesa, de asemenea, informații din baza de date folosind conexiunea JDBC (Java [Database](/ro/database/) Connectivity). Fișierele JHTML pot fi deschise în orice editor de text și vizualizate în browsere web precum Google Chrome, Firefox și Safari.

## Format de fișier JHTML

JHTML este o tehnologie proprietară a ATG și poate fi creată utilizând Editorul de documente Dynamo ATG (Art Technology Group). Fișierele JHTML sunt scrise în format text simplu folosind codul standard HTML și Java. Acestea conțin etichete HTML standard pe lângă etichetele proprietare care fac referire la obiecte Java. Când o astfel de pagină este solicitată de către utilizator, serverul HTTP redirecționează cererea către un server de aplicații Java. Pagina JHTML este convertită mai întâi în fișierul .java și compilată pentru a genera un fișier [.class](/ro/programming/class/) care este executat ca servlet. Acest lucru generează un flux de date standard HTTP și HTML care este returnat înapoi browserului solicitant pentru a fi afișat utilizatorului. Acest lucru este util pentru a rula interogări legate de baza de date pe server și pentru a returna rezultatul acumulat finalizat în browserul clientului.

## Referințe

* [Structura globală a documentului HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

