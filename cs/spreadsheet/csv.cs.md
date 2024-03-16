{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "soubor", "rozšíření", "formát souboru", "hodnoty oddělené čárkami", "tabulka" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru CSV a rozhraních API, která mohou vytvářet a otevírat soubory CSV.",
  "title" :"Formát souboru CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor CSV?

Soubory s příponou .csv (Comma Separated Values) představují prosté textové soubory, které obsahují záznamy dat s hodnotami oddělenými čárkami. Každý řádek v souboru CSV je nový záznam ze sady záznamů obsažených v souboru. Takové soubory jsou generovány, když je zamýšlený přenos dat z jednoho úložného systému do druhého. Protože všechny aplikace dokážou rozpoznat záznamy oddělené čárkou, import takových datových souborů do databáze se provádí velmi pohodlně. Téměř všechny tabulkové aplikace, jako je Microsoft Excel nebo OpenOffice Calc, umí importovat CSV bez velkého úsilí. Data importovaná z takových souborů jsou uspořádána v buňkách tabulky pro reprezentaci uživateli.

## Stručná historie ##

Následuje několik rychlých faktů o původu a historii formátu souboru CSV.

1972 - IBM Fortran (úroveň H prodloužený) kompilátor podporoval je pod OS/360

* 1978 – Seznam-řízený vstup/výstup byl podporován FORTRAN 77, který používal čárky a mezery pro oddělovače

* 2005 – CSV byl standardizován pomocí [RFC4180](https://tools.ietf.org/html/rfc4180) jako typ obsahu MIME.

* 2013 – nedostatky RFC4180 byly vyřešeny doporučením W3C

* 2015 – W3C vytvořilo první návrhy doporučení pro standardy CSV metadat, které začaly jako doporučení v prosinci 2015

## Převést soubory CSV ##

Soubory CSV lze převést do několika různých formátů souborů pomocí aplikací, které mohou tyto soubory otevřít. Microsoft Excel může například importovat data z formátu CSV a uložit je do XLS, [XLSX](/cs/spreadsheet/xlsx/), [PDF](/cs/pdf/), [TXT](/cs/word-processing/txt/) , XML a [HTML](/cs/web/html/) formáty souborů. Podobně ostatní desktopové i online služby poskytují možnost exportovat CSV soubory do HTML, ODS a [RTF](/cs/word-processing/rtf/).

## Formát souboru CSV ##

Formát souboru CSV je uveden v [RFC4180](https://tools.ietf.org/html/rfc4180). Definuje jakýkoli soubor jako vyhovující CSV, pokud:

* Každý záznam je umístěn na samostatném řádku, odděleném zalomením řádku (CRLF). Například:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* Poslední záznam v souboru může nebo nemusí mít konec řádku. Například:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* Jako první řádek souboru se může objevit volitelný řádek záhlaví se stejným formátem jako normální řádky záznamu. Tato hlavička bude obsahovat názvy odpovídající polím v souboru a měla by obsahovat stejný počet polí jako záznamy ve zbytku souboru (přítomnost nebo nepřítomnost řádku hlavičky by měla být indikována prostřednictvím volitelného parametru "hlavička" tohoto typ MIME). Například:
* název_pole, název_pole, název_pole CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* V záhlaví a v každém záznamu může být jedno nebo více polí oddělených čárkami. Každý řádek by měl obsahovat stejný počet polí v celém souboru. Mezery jsou považovány za součást pole a neměly by být ignorovány. Za posledním polem v záznamu nesmí následovat čárka. Například:
* aaa,bbb,ccc
* Každé pole může nebo nemusí být uzavřeno v uvozovkách (avšak některé programy, jako je Microsoft Excel, dvojité uvozovky vůbec nepoužívají). Pokud pole nejsou uzavřena dvojitými uvozovkami, pak se dvojité uvozovky nemusí objevit uvnitř polí. Například:\
* "aaa","bbb","ccc" CRLF
* zzz,yyy,xxx
* Pole obsahující zalomení řádků (CRLF), dvojité uvozovky a čárky by měla být uzavřena do dvojitých uvozovek. Například:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Jsou-li k uzavření polí použity dvojité uvozovky, pak dvojité uvozovky, které se objevují uvnitř pole, musí být uvozeny tak, že před ně budou uvedeny další dvojité uvozovky. Například:
* "aaa","b""bb","ccc"

Ve světle moderního použití však oddělovač není omezen pouze na čárku a může to být i středník, tabulátor nebo mezery. Aplikace jako Microsoft Excel poskytují možnost zadat oddělovací znak pro import záznamů ze souboru CSV.

## Reference

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV – Wikipedie](https://en.wikipedia.org/wiki/Comma-separated_values)

