{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om AC filformat og API'er, der kan oprette og åbne ACCDB filer.",
  "title" : "AC-filformat - Autoconf Script-fil",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-da",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Hvad er en AC fil?

AC-filen er Autoconf-scriptfilen. **Autoconf** er en udvidelsesbar pakke af M4-makroer, der producerer shell-scripts til automatisk at konfigurere softwarekildekodepakker. Disse scripts kan tilpasse pakkerne til mange slags UNIX-lignende systemer uden manuel brugerindblanding. Autoconf opretter et konfigurationsscript til en pakke fra en skabelonfil, der viser de operativsystemfunktioner, som pakken kan bruge, i form af M4-makrokald.

Producing configuration scripts using Autoconf requires GNU M4. Du bør installere GNU M4 (mindst version 1.4.6, selvom 1.4.13 eller nyere anbefales) før du konfigurerer Autoconf, så Autoconfs konfigurationsscript kan finde det. Konfigurationsscripts produceret af Autoconf er selvstændige, så deres brugere behøver ikke at have Autoconf (eller GNU M4).

## Hvordan åbner jeg filen AC?

AC står for Automatic Configuration. Det er et script genereret af GNU Autoconf, der gør det muligt at tilpasse softwarekildekoden til forskellige Posix-lignende systemer ved at teste for nødvendige funktioner i pakken. Scriptet kaldes en AC-fil.

## Vigtigste autoværktøjskomponenter

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools er en samling af relaterede pakker, som, når de bruges sammen, fjerner meget af de vanskeligheder, der er forbundet med at skabe bærbar software. Disse værktøjer, sammen med et par relativt simple upstream-leverede inputfiler, bruges til at skabe byggesystemet til en pakke.

**En grundlæggende oversigt over, hvordan de vigtigste autotools-komponenter passer sammen.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

I en simpel opsætning:

- `autoconf`-programmet producerer et konfigurationsscript fra enten `configure.in` eller `configure.ac`.
- `automake`-programmet producerer en Makefile.in fra en Makefile.am.
- `configure`-scriptet køres for at producere en eller flere Makefile-filer fra Makefile.in-filer.
- `make`-programmet bruger Makefilen til at kompilere programmet.

## Referencer
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Grundlæggende om Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



