{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lär dig om AC-filformat och API:er som kan skapa och öppna ACCDB-filer.",
  "title" : "AC-filformat - Autoconf-skriptfil",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-sv",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Vad är AC fil?

AC-filen är Autoconf-skriptfilen. **Autoconf** är ett utökningsbart paket med M4-makron som producerar skalskript för att automatiskt konfigurera källkodspaket för programvara. Dessa skript kan anpassa paketen till många typer av UNIX-liknande system utan manuellt användaringripande. Autoconf skapar ett konfigurationsskript för ett paket från en mallfil som listar de operativsystemfunktioner som paketet kan använda, i form av M4-makroanrop.

Producing configuration scripts using Autoconf requires GNU M4. Du bör installera GNU M4 (minst version 1.4.6, även om 1.4.13 eller senare rekommenderas) innan du konfigurerar Autoconf, så att Autoconfs konfigureringsskript kan hitta det. Konfigurationsskripten som produceras av Autoconf är fristående, så deras användare behöver inte ha Autoconf (eller GNU M4).

## Hur öppnar man filen AC?

AC står för Automatic Configuration. Det är ett skript som genereras av GNU Autoconf som gör det möjligt att anpassa programvarans källkod till olika Posix-liknande system genom att testa för nödvändiga funktioner i paketet. Skriptet kallas en AC-fil.

## Huvudkomponenter i Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools är en samling relaterade paket som, när de används tillsammans, tar bort mycket av svårigheterna med att skapa bärbar programvara. Dessa verktyg, tillsammans med några relativt enkla uppströms-tillförda indatafiler, används för att skapa byggsystemet för ett paket.

**En grundläggande översikt över hur de viktigaste autotools-komponenterna passar ihop.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

I en enkel installation:

- Programmet `autoconf` producerar ett konfigureringsskript från antingen `configure.in` eller `configure.ac`.
- Programmet automake producerar en Makefile.in från en Makefile.am.
- Skriptet `configure` körs för att skapa en eller flera Makefile-filer från Makefile.in-filer.
- Programmet `make` använder Makefilen för att kompilera programmet.

## Referenser
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Grunderna i Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



