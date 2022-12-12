{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Limbajul de definire a raportului pe partea client",
  "keywords" :[ "rdlc", "limbaj de definiție a raportului", "format mkv", "XSD", "partea client a limbajului de definiție a raportului"],
  "description":"Aflați despre formatul de fișier RDLC, care este o reprezentare XML a unei definiții de raport SQL Server Reporting Services.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Ce este un fișier RDLC? ##

RDLC înseamnă Report Definition Language Client side. De fapt, este o extensie a fișierului de raport creat folosind tehnologia de raportare Microsoft. Versiunea SQL Server 2005 a Report Designer este utilizată pentru a crea aceste fișiere. Controlul **ReportViewer** din partea clientului poate executa direct rapoartele RDLC.

## Fișiere RDL VS RDLC
|Fișiere .rdl |Fișiere .rdlc|
---|---|
|Fișierele RDL sunt create de versiunea SQL Server 2005 a Report Designer|Fișierele RDLC sunt create de versiunea Visual Studio 2005 a Report Designer|
|Se folosește în SQL Server Reporting Services|Se folosește în Visual Studio|
|Este un raport de la distanță|Este un raport local|
|Este nevoie de o instanță Reporting Services pentru a o rula|Nu este nevoie de o instanță Reporting Services|

## Crearea fișierelor de definiție a raportului client (.rdlc).
Controlul ReportViewer este utilizat pentru a rula fișiere de definire a raportului client (.rdlc) folosind capacitatea de procesare încorporată a controlului. Rapoartele clientului că rulați în modul de procesare local pot fi create cu ușurință în proiectul dvs. de aplicație. Următoarele sunt abordările pentru crearea raportului:

- Utilizați **Report Wizard** pentru a crea o nouă definiție de raport pentru client (.rdlc).

- Creați un nou fișier de definire a raportului client (.rdlc) utilizând Visual Studio.

- Generați o definiție de raport în mod programatic.


Puteți previzualiza un raport numai rulând-l într-un control **ReportViewer**. Vă rugăm să rețineți că puteți deschide și edita definiția raportului în orice moment, apoi puteți construi sau implementa aplicația pentru a verifica rezultatele.

## Referințe ##

- [Crearea fișierelor de definiție a raportului client (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

