{
  "date" : "2019-12-09",
  "keywords" :[ "soubor zip", "formát souboru zip", "co je soubor zip", "soubor", "příklad zip", "přípona souboru zip", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"Co je soubor ZIP a rozhraní API, která mohou vytvářet a otevírat soubory ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Co je to soubor ZIP? ##

Soubor s příponou .zip je archiv, který může obsahovat jeden nebo více souborů nebo adresářů. Archiv může mít kompresi aplikovanou na zahrnuté soubory, aby se zmenšila velikost souboru ZIP. Formát souboru ZIP byl zveřejněn již v únoru 1989 Philem Katzem pro dosažení archivace souborů a složek. Formát byl součástí nástroje [PKZIP](https://www.pkware.com/pkzip), vytvořeného společností PKWARE, Inc. Hned po zpřístupnění [dostupných specifikací](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), mnoho společností učinilo souborový formát ZIP součástí svých softwarových nástrojů, včetně Microsoftu (od Windows 7), Apple (Mac OS X) a mnoha dalších.

## Stručná historie formátu souboru ZIP

Historie formátu souboru ZIP sahá až k případu soudního sporu vedeného společností System Enhancement Associates (SEA) proti společnosti PKWARE za použití jejího nástroje ARC bez povolení k její ochranné známce a autorských práv ke vzhledu produktu a uživatelskému rozhraní. Předtím Phil Katz přepsal zdrojový kód SEA a vydal PKXARC, ARC extraktor, a PKARC, souborový kompresor, jako freeware pro systémy založené na MS-DOS. Po prohraném soudním sporu už PKWARE nemohl používat nic, co by se týkalo ARC. Zde vznikla nová komprimace souborů pojmenovaná jako ZIP, která byla součástí nástroje PKZIP společnosti PKWARE, Inc.

Katz uvolnil specifikace formátu souboru ZIP do veřejné domény, přičemž si ponechal vlastnická práva na svůj nástroj pro kompresi a extrakci, tj. PKZIP. Kompresní systém ZIP byl (a je) schopen archivovat soubory ve složce pomocí algoritmu 32bitové cyklické kontroly redundance ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) pro kompresi souboru velikosti. Na rozdíl od ARC obsahovaly složky .ZIP adresářový soubor, který hrál roli kódové knihy kryptografa a obsahoval informace potřebné k vykreslení komprimovaných souborů.

## Podporované kompresní metody v ZIP

Podle specifikací formátu souboru .ZIP jsou podporovány následující metody komprese.

* Store - neznamená žádnou kompresi
* Zmenšit
* Redukce (To znamená kompresní faktory v rozsahu od úrovně 1 do úrovně 4)
* Implodovat
* Vyfouknout
*Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd verze I, Rev 1

DEFLATE je běžně používaná metoda komprese, což je bezztrátový algoritmus komprese data, který používá kombinaci kódování LZ77 a Huffman a je podrobně popsán v [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Specifikace formátu souboru ZIP

Soubory ZIP mají schopnost ukládat více souborů pomocí různých technik komprese a zároveň podporují ukládání souboru bez jakékoli komprese. Každý soubor je uložen/komprimován jednotlivě, což pomáhá jeho extrahování nebo přidávání nových, aniž by bylo nutné komprimovat nebo dekompresovat celý archiv.

### Celkový formát souboru ZIP

Každý soubor ZIP je strukturován následujícím způsobem:


| Formát souboru ZIP
---|
|Záhlaví místního souboru 1
| Data souboru 1
|Deskriptor dat 1
|Záhlaví místního souboru 2
| Data souboru 2
|Datový deskriptor 2
| ....
| ....
|Záhlaví místního souboru N
| Data souboru N
|Datový deskriptor N
|Záhlaví dešifrování archivu
|Archivujte další záznam dat
|Centrální adresář

Formát souboru ZIP používá pro účely archivace 32bitový algoritmus CRC. Aby bylo možné vykreslit komprimované soubory, archiv ZIP má na svém konci adresář, který uchovává záznam obsažených souborů a jejich umístění v archivním souboru. Hraje tedy roli kódování pro zapouzdření informací nezbytných k vykreslení komprimovaných souborů. Čtečky ZIP používají adresář k načtení seznamu souborů bez čtení celého ZIP archivu. Formát uchovává duální kopie adresářové struktury, aby byla zajištěna větší ochrana před ztrátou dat.

Každý soubor v archivu ZIP je reprezentován jako samostatná položka, kde každá položka se skládá z hlavičky místního souboru následované daty komprimovaného souboru. Adresář na konci archivu obsahuje odkazy na všechny tyto položky souboru. Čtenáři souborů ZIP by se měli vyvarovat čtení záhlaví místních souborů a všechny druhy výpisů souborů by měly být načteny z adresáře. Tento adresář je jediným zdrojem platných záznamů souborů v archivu, protože soubory lze přidávat i ke konci archivu. Pokud tedy čtenář čte lokální hlavičky ZIP archivu od začátku, může číst i neplatné (smazané) záznamy a také ty, které nejsou součástí Adresáře odstraňovaného z archivu.

Pořadí položek souborů v centrálním adresáři se nemusí shodovat s pořadím položek souborů v archivu.

### Položky souboru ZIP

Záznamy v souboru ZIP jsou uspořádány za sebou, přičemž každý záznam se skládá z:

* Záhlaví místního souboru
* Volitelná doplňková datová pole
* Uživatelská data (volitelně komprimovaná/volitelně šifrovaná)

Záhlaví místního souboru každé položky představuje informace o souboru, jako je komentář, velikost souboru a název souboru. Další datová pole (volitelná) mohou obsahovat informace o možnostech rozšiřitelnosti formátu ZIP.

#### Záhlaví místního souboru

Záhlaví místního souboru má specifickou strukturu polí sestávající z vícebajtových hodnot. Všechny hodnoty jsou uloženy v pořadí bajtů typu little-endian, kde délka pole počítá délku v bajtech. Všechny struktury v souboru ZIP používají 4bajtové podpisy pro každou položku souboru. Konec podpisu centrálního adresáře je 0x06054b50 a lze jej rozlišit pomocí vlastního jedinečného podpisu. Následuje pořadí informací uložených v záhlaví místního souboru.


|Offset|Bajty|Popis
---|---|---|
|0|4|Podpis záhlaví místního souboru # 0x04034b50 (čteno jako číslo little-endian)
|4|2|Verze potřebná k extrahování (minimum)
|6|2|Příznak bitu pro obecné použití
|8|2|Metoda komprese
|10|2|Uložit čas poslední úpravy
|12|2|Uložit datum poslední úpravy
|14|4|CRC-32
|18|4|Stlačená velikost
|22|4|Nekomprimovaná velikost
|26|2|Délka názvu souboru (n)
|28|2|Délka pole navíc (m)
|30|n|Název souboru
|30+n|m|Pole navíc

#### Záhlaví souboru centrálního adresáře


|Offset|Bajty|Popis
---|---|---|
|0|4|Podpis hlavičky souboru centrálního adresáře # 0x02014b50
|4|2|Verze od
|6|2|Verze potřebná k extrahování (minimum)
|8|2|Příznak bitu pro obecné použití
|10|2|Metoda komprese
|12|2|Uložit čas poslední úpravy
|14|2|Uložit datum poslední změny
|16|4|CRC-32
|20|4|Stlačená velikost
|24|4|Nekomprimovaná velikost
|28|2|Délka názvu souboru (n)
|30|2|Délka pole navíc (m)
|32|2|Délka komentáře souboru (k)
|34|2|Číslo disku, kde soubor začíná
|36|2|Atributy interního souboru
|38|4|Atributy externích souborů
|42|4|Relativní posun záhlaví lokálního souboru. Toto je počet bajtů mezi začátkem prvního disku, na kterém se soubor vyskytuje, a začátkem záhlaví místního souboru. To umožňuje softwaru číst centrální adresář k nalezení pozice souboru uvnitř souboru ZIP.
|46|n|Název souboru
|46+n|m|Pole navíc
|46+n+m|k|Komentář souboru

#### Konec záznamu centrálního adresáře


|Offset|Bajty|Popis
---|---|---|
|0|4|Konec podpisu centrálního adresáře # 0x06054b50
|4|2|Číslo tohoto disku
|6|2|Disk, na kterém začíná centrální adresář
|8|2|Počet záznamů centrálního adresáře na tomto disku
|10|2|Celkový počet záznamů centrálního adresáře
|12|4|Velikost centrálního adresáře (bajty)
|16|4|Posun začátku centrálního adresáře vzhledem k začátku archivu
|20|2|Délka komentáře (n)
|22|n|Komentář

## Reference

* [Specifikace formátu souboru ZIP PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struktura souboru PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
