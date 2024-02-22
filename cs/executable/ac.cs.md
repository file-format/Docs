{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Přečtěte si o formátu souborů AC a rozhraních API, která mohou vytvářet a otevírat soubory ACCDB.",
  "title" : "Formát AC souboru - Autoconf Script File",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-cs",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Co je soubor AC?

AC soubor je soubor skriptu Autoconf. **Autoconf** je rozšiřitelný balíček maker M4, který vytváří skripty shellu pro automatickou konfiguraci balíčků zdrojového kódu softwaru. Tyto skripty mohou přizpůsobit balíčky mnoha druhům systémů podobných UNIXu bez ručního zásahu uživatele. Autoconf vytvoří konfigurační skript pro balíček ze souboru šablony, který uvádí funkce operačního systému, které může balíček používat, ve formě volání maker M4.

Producing configuration scripts using Autoconf requires GNU M4. Před konfigurací Autoconf byste měli nainstalovat GNU M4 (alespoň verze 1.4.6, ačkoli se doporučuje 1.4.13 nebo novější), aby jej konfigurační skript Autoconf mohl najít. Konfigurační skripty produkované Autoconf jsou samostatné, takže jejich uživatelé nemusí mít Autoconf (nebo GNU M4).

## Jak otevřít soubor AC?

AC je zkratka pro Automatic Configuration. Je to skript generovaný GNU Autoconf, který umožňuje přizpůsobení zdrojového kódu softwaru různým systémům podobným Posix testováním nezbytných funkcí v balíčku. Skript se nazývá AC soubor.

## Hlavní součásti Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools je sbírka souvisejících balíčků, které při společném použití odstraňují většinu obtíží spojených s vytvářením přenosného softwaru. Tyto nástroje spolu s několika relativně jednoduchými vstupními soubory dodanými od uživatele se používají k vytvoření systému sestavování balíčku.

**Základní přehled toho, jak do sebe hlavní součásti autotools zapadají.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

V jednoduchém nastavení:

- Program `autoconf` vytváří konfigurační skript buď z `configure.in` nebo `configure.ac`.
- Program `automake` vytváří Makefile.in z Makefile.am.
- Spustí se skript `configure`, aby vytvořil jeden nebo více souborů Makefile ze souborů Makefile.in.
- Program `make` používá ke kompilaci programu Makefile.

## Reference
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Základy Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



