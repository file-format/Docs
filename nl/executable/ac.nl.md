{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Leer meer over de AC-bestandsindeling en API's waarmee ACCDB-bestanden kunnen worden gemaakt en geopend.",
  "title" : "AC-bestandsindeling - Autoconf-scriptbestand",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-nl",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Wat is een AC-bestand?

AC-bestand is het Autoconf-scriptbestand. **Autoconf** is een uitbreidbaar pakket van M4-macro's die shell-scripts produceren om softwarebroncodepakketten automatisch te configureren. Deze scripts kunnen de pakketten aanpassen aan vele soorten UNIX-achtige systemen zonder handmatige tussenkomst van de gebruiker. Autoconf maakt een configuratiescript voor een pakket op basis van een sjabloonbestand waarin de functies van het besturingssysteem worden vermeld die het pakket kan gebruiken, in de vorm van M4-macro-aanroepen.

Producing configuration scripts using Autoconf requires GNU M4. U dient GNU M4 te installeren (minstens versie 1.4.6, hoewel 1.4.13 of hoger wordt aanbevolen) voordat u Autoconf configureert, zodat het configuratiescript van Autoconf het kan vinden. De configuratiescripts die door Autoconf worden geproduceerd, staan op zichzelf, dus hun gebruikers hoeven niet over Autoconf (of GNU M4) te beschikken.

## Hoe open je een AC-bestand?

AC staat voor Automatische Configuratie. Het is een script gegenereerd door GNU Autoconf waarmee de softwarebroncode kan worden aangepast aan verschillende Posix-achtige systemen door te testen op noodzakelijke functies in het pakket. Het script wordt een AC-bestand genoemd.

## Belangrijkste Autotools-componenten

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools is een verzameling verwante pakketten die, wanneer ze samen worden gebruikt, een groot deel van de problemen wegnemen die gepaard gaan met het maken van draagbare software. Deze tools worden, samen met een paar relatief eenvoudige, upstream-aangeleverde invoerbestanden, gebruikt om het bouwsysteem voor een pakket te creëren.

**Een basisoverzicht van hoe de belangrijkste autotools-componenten in elkaar passen.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

In een eenvoudige opstelling:

- Het programma `autoconf` produceert een configuratiescript van `configure.in` of `configure.ac`.
- Het programma `automake` produceert een Makefile.in van een Makefile.am.
- Het `configure`-script wordt uitgevoerd om een of meer Makefile-bestanden te produceren uit Makefile.in-bestanden.
- Het `make` programma gebruikt de Makefile om het programma te compileren.

## Referenties
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [De basisprincipes van Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



