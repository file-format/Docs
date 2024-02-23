{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Dowiedz się o formacie pliku AC i interfejsach API, które umożliwiają tworzenie i otwieranie plików ACCDB.",
  "title" : "Format pliku AC — plik skryptu Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-pl",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## .AC opcja № 1

Plik AC to plik skryptu Autoconf. **Autoconf** to rozszerzalny pakiet makr M4, które tworzą skrypty powłoki w celu automatycznej konfiguracji pakietów kodu źródłowego oprogramowania. Skrypty te mogą dostosować pakiety do wielu rodzajów systemów typu UNIX bez ręcznej interwencji użytkownika. Autoconf tworzy skrypt konfiguracyjny dla pakietu na podstawie pliku szablonu, który zawiera listę funkcji systemu operacyjnego, z których może korzystać pakiet, w formie wywołań makr M4.

Producing configuration scripts using Autoconf requires GNU M4. Powinieneś zainstalować GNU M4 (co najmniej wersję 1.4.6, chociaż zalecana jest wersja 1.4.13 lub nowsza) przed skonfigurowaniem Autoconf, aby skrypt konfiguracyjny Autoconf mógł go znaleźć. Skrypty konfiguracyjne tworzone przez Autoconf są samodzielne, więc ich użytkownicy nie muszą mieć Autoconfa (ani GNU M4).

## Jak otworzyć plik AC?

AC oznacza konfigurację automatyczną. Jest to skrypt wygenerowany przez GNU Autoconf, który umożliwia dostosowanie kodu źródłowego oprogramowania do różnych systemów typu Posix poprzez testowanie niezbędnych funkcji w pakiecie. Skrypt nazywa się plikiem AC.

## Główne komponenty Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools to zbiór powiązanych pakietów, które używane razem eliminują wiele trudności związanych z tworzeniem oprogramowania przenośnego. Narzędzia te, wraz z kilkoma stosunkowo prostymi plikami wejściowymi dostarczonymi z zewnątrz, są używane do tworzenia systemu kompilacji pakietu.

**Podstawowy przegląd łączenia głównych komponentów Autotools.**

!{{HIPERLINK1}}

W prostej konfiguracji:

- Program `autoconf` tworzy skrypt konfiguracyjny z `configure.in` lub `configure.ac`.
- Program `automake` tworzy plik Makefile.in z pliku Makefile.am.
- Uruchamiany jest skrypt `configure` w celu utworzenia jednego lub większej liczby plików Makefile z plików Makefile.in.
- Program `make` używa pliku Makefile do kompilacji programu.

## Bibliografia
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Podstawy Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



