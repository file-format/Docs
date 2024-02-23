{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Aflați despre formatul fișierului AC și despre API-urile care pot crea și deschide fișiere ACCDB.",
  "title" : "Format Fișier AC - Fișier Script Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-ro",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Ce este un fișier AC?

Fișierul AC este fișierul script Autoconf. **Autoconf** este un pachet extensibil de macrocomenzi M4 care produc scripturi shell pentru a configura automat pachetele de cod sursă software. Aceste scripturi pot adapta pachetele la multe tipuri de sisteme asemănătoare UNIX fără intervenția manuală a utilizatorului. Autoconf creează un script de configurare pentru un pachet dintr-un fișier șablon care listează caracteristicile sistemului de operare pe care le poate folosi pachetul, sub formă de apeluri macro M4.

Producing configuration scripts using Autoconf requires GNU M4. Ar trebui să instalați GNU M4 (cel puțin versiunea 1.4.6, deși se recomandă 1.4.13 sau o versiune ulterioară) înainte de a configura Autoconf, astfel încât scriptul de configurare al lui Autoconf să îl poată găsi. Scripturile de configurare produse de Autoconf sunt autonome, astfel încât utilizatorii lor nu trebuie să aibă Autoconf (sau GNU M4).

## Cum se deschide fișierul AC?

AC înseamnă Configurare automată. Este un script generat de GNU Autoconf care permite ca codul sursă al software-ului să fie adaptat la diferite sisteme de tip Posix prin testarea caracteristicilor necesare din pachet. Scriptul se numește fișier AC.

## Componentele majore ale Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools este o colecție de pachete conexe care, atunci când sunt utilizate împreună, înlătură o mare parte din dificultatea pe care o implică crearea de software portabil. Aceste instrumente, împreună cu câteva fișiere de intrare relativ simple furnizate de amonte, sunt folosite pentru a crea sistemul de compilare pentru un pachet.

**O prezentare generală de bază a modului în care componentele principale ale uneltelor auto se potrivesc.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Într-o configurare simplă:

- Programul `autoconf` produce un script de configurare fie din `configure.in`, fie din `configure.ac`.
- Programul `automake` produce un Makefile.in dintr-un Makefile.am.
- Scriptul `configure` este rulat pentru a produce unul sau mai multe fișiere Makefile din fișierele Makefile.in.
- Programul `make` folosește Makefile pentru a compila programul.

## Referințe
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Elementele de bază ale Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



