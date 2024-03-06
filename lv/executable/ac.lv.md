{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Uzziniet par AC failu formātu un API, kas var izveidot un atvērt ACCDB failus.",
  "title" : "AC faila formāts — Autoconf skripta fails",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-lv",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Kas ir maiņstrāvas fails?

AC fails ir Autoconf skripta fails. **Autoconf** ir paplašināma M4 makro pakotne, kas veido čaulas skriptus, lai automātiski konfigurētu programmatūras pirmkoda pakotnes. Šie skripti var pielāgot pakotnes daudzu veidu UNIX līdzīgām sistēmām bez lietotāja manuālas iejaukšanās. Autoconf izveido pakotnes konfigurācijas skriptu no veidnes faila, kurā ir uzskaitīti operētājsistēmas līdzekļi, kurus pakotne var izmantot M4 makro izsaukumu veidā.

Producing configuration scripts using Autoconf requires GNU M4. Pirms Autoconf konfigurēšanas jāinstalē GNU M4 (vismaz versija 1.4.6, lai gan ieteicama 1.4.13 vai jaunāka versija), lai Autoconf konfigurācijas skripts to varētu atrast. Autoconf radītie konfigurācijas skripti ir autonomi, tāpēc to lietotājiem nav nepieciešams Autoconf (vai GNU M4).

## Kā atvērt AC failu?

AC apzīmē automātisko konfigurāciju. Tas ir GNU Autoconf ģenerēts skripts, kas ļauj pielāgot programmatūras pirmkodu dažādām Posix līdzīgām sistēmām, pārbaudot pakotnē nepieciešamās funkcijas. Skriptu sauc par maiņstrāvas failu.

## Galvenās automātisko rīku sastāvdaļas

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools ir saistītu pakotņu kolekcija, kuras, lietojot kopā, novērš daudzas grūtības, kas saistītas ar pārnēsājamas programmatūras izveidi. Šie rīki kopā ar dažiem salīdzinoši vienkāršiem iepriekš piegādātiem ievades failiem tiek izmantoti, lai izveidotu pakotnes veidošanas sistēmu.

** Pamata pārskats par to, kā galvenie automātisko rīku komponenti sader kopā.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

Vienkāršā iestatījumā:

- Programma autoconf izveido konfigurēšanas skriptu no configure.in vai configure.ac.
- Programma automake izveido Makefile.in no Makefile.am.
- Tiek palaists skripts configure, lai izveidotu vienu vai vairākus Makefile failus no Makefile.in failiem.
- Programma make izmanto Makefile, lai kompilētu programmu.

## Atsauces
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Autotools pamati](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



