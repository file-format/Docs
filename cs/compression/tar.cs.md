{
  "date" : "2019-10-11",
  "keywords" :[ "soubor tar", "formát souboru tar", "co je soubor tar", "soubor", "příklad tar", "přípona souboru tar", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Unix Archive File Format",
  "description":"Zjistěte, co je soubor Tar a rozhraní API, která mohou vytvářet a otevírat soubory TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor TAR?

Soubory s příponou .tar jsou archivy vytvořené pomocí utility založené na Unixu pro shromažďování jednoho nebo více souborů. Více souborů je uloženo v nekomprimovaném formátu s podporou přidávání souborů a složek do archivu. Nástroj TAR na Unixu je založen na příkazech, ale takto vytvořené soubory jsou podporovány většinou systémů pro archivaci souborů na téměř všech operačních systémech. Poprvé byl vytvořen v roce 1979 AT&T Bell Laboratories a následné verze byly publikovány s postupem času.

## Formát souboru TAR

TAR je otevřený souborový formát s úplnými specifikacemi dostupnými pro vývojáře. Jeho struktura souborů byla standardizována v POSIX.1-1988 a později v POSIX.1-2001. Datové sady vytvořené tar uchovávají informace o parametrech souborového systému, jako jsou:

* Název
* Časová razítka
* Vlastnictví
* Oprávnění k přístupu k souborům
* Organizace adresářů

Soubor Tar nemá žádné magické číslo. Obsahuje řadu bloků, kde každý blok má BLOCKSIZE bajtů.

Každý archivovaný soubor je reprezentován blokem záhlaví, který soubor popisuje, následovaným nulou nebo více bloky, které udávají obsah souboru. Na konci archivního souboru jsou dva 512bajtové bloky vyplněné binárními nulami jako značka konce souboru. Rozumný systém by měl zapsat takovou značku konce souboru na konec archivu, ale při čtení archivu nesmí předpokládat, že takový blok existuje. Zejména GNU tar vždy vydá varování, pokud na něj nenarazí.

Bloky mohou být blokovány pro fyzické I/O operace. Každý záznam n bloků (kde n je nastaveno volbou blocking-factor = 512-size na tar) je zapsán jedinou operací "write()". Na magnetických páskách je výsledkem takového zápisu jeden záznam. Při zápisu do archivu by měl být poslední záznam bloků zapsán v plné velikosti, přičemž bloky za nulovým blokem obsahují všechny nuly. Při čtení archivu by měl rozumný systém správně zacházet s archivem, jehož poslední záznam je kratší než zbytek, nebo který obsahuje nesmyslné záznamy po nulovém bloku.

### Hlavička dehtu

Stejně jako jakákoli jiná záhlaví souborů obsahuje záznam záhlaví souboru tar metadata o souboru a je uveden v následující tabulce.


|Posun pole|Velikost pole (bajty)|Pole
---|---|---|
|0|100|Název souboru
|100|8|Režim souborů
|108|8|Číselné ID uživatele vlastníka
|116|8|Číselné ID uživatele skupiny
|124|12|Velikost souboru v bajtech (osmičkový základ)
|136|12|Čas poslední úpravy v numerickém formátu času Unix (osmičkové)
|148|8|Kontrolní součet pro záznam záhlaví
|156|1|Indikátor odkazu (typ souboru)
|157|100|Název propojeného souboru

Nepoužitá pole jsou vyplněna bajty NUL. Hlavička se skládá z 257 bajtů, která je doplněna bajty NUL, aby se naplnila na 512 bajtů záznamu.

## Reference ##

* [TAR – podle Wikipedie](https://en.wikipedia.org/wiki/Tar_(computing))
* [Základní formát TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

