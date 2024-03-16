{
  "date" : "2019-10-11",
  "keywords" :[ "soubor rtf", "formát souboru rtf", "co je soubor rtf", "soubor", "příklad rtf", "přípona souboru rtf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Rich Text Format",
  "description":"Další informace o formátu souborů RTF a rozhraních API, která mohou vytvářet a otevírat soubory RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor RTF?

Formát Rich Text Format (**RTF**) představený a zdokumentovaný společností Microsoft představuje metodu kódování formátovaného textu a grafiky pro použití v aplikacích. Tento formát usnadňuje výměnu dokumentů mezi platformami s jinými produkty společnosti Microsoft, čímž slouží účelu interoperability. Tato schopnost z něj činí standard přenosu dat mezi softwarem pro zpracování textu, a proto lze obsah přenášet z jednoho operačního systému do druhého bez ztráty formátování dokumentu. Specifikace formátu souborů jsou k dispozici od společnosti Microsoft k veřejnému stažení a lze na ně odkazovat z pohledu vývojáře.

## Stručná historie formátu souboru RTF ##

Formát souboru RTF prošel od svého zveřejnění několika revizemi. Jeho oficiální verze pro čtení/zápis byla publikována jako součást Microsoft Word 3.0 pro Macintosh se specifikacemi verze 1.0. Konečná verze specifikací, 1.9.1, byla publikována společností Microsoft v březnu 2008. Poté již nejsou provedena žádná další vylepšení specifikací. V současné době mají téměř všechny operační systémy více funkcí bohatých aplikací, které minimalizovaly/vymýtily používání formátu RTF.

## Specifikace formátu souboru RTF ##

RTF slouží jako standard přenosu dat mezi softwarem pro zpracování textu a přenosu obsahu z jednoho operačního systému do druhého. Toho je dosaženo pomocí řídicích slov, která byla zavedena aplikací Microsoft Office Word až do roku 2007. Standardní soubor RTF se skládá z ASCII pro reprezentaci formátovaného textu a se znaky, které nejsou ASCII, které jsou převedeny na příslušné hodnoty kódu. Novější verze aplikace Word mohou číst soubory RTF generované předchozími verzemi, zatímco starší verze ignorují řídicí slova a skupiny, kterým nerozumí.

### Pochopení základů RTF ###

Soubory RTF používají 7bitový prostý text ASCII, který se skládá z:

* kontrolní slova
* ovládací symboly a
* skupiny.

Ty fungují jako stavební kameny pro reprezentaci dat RTF jako srozumitelného kódování textu a znaků.

#### Kontrolní slovo ####

Ty představují speciálně formátovaný příkaz používaný k označení znaků pro zobrazení a nemohou být delší než 32 písmen. Řídicí slovo je definováno:

\<ASCII Letter Sequence> //<//Delimiter//> //

Každé řídicí slovo rozlišuje velká a malá písmena a začíná zpětným lomítkem. Sekvence písmen ASCII může obsahovat abecedy ASCII (a až z a A až Z). The<Delimite> označuje konec názvu kontrolního slova a může být jedním z následujících:

* Prostor. To slouží pouze k vymezení řídicího slova a při následném zpracování je ignorováno.
* Číslice nebo ASCII znaménko mínus, které označuje, že číselný parametr je spojen s řídicím slovem. Následující digitální sekvence je pak oddělena jakýmkoli jiným znakem než číslicí ASCII (běžně dalším řídicím slovem, které začíná zpětným lomítkem). Parametr může být kladné nebo záporné desetinné číslo. Rozsah hodnot pro číslo je nominálně –32768 až 32767, tj. 16bitové celé číslo se znaménkem. Malý počet řídicích slov nabývá hodnot v rozsahu −2 147 483 648 až 2 147 483 647 (32bitové celé číslo se znaménkem). Tato řídicí slova zahrnují **\binN**, **\revdttmN//**, **\rsidN** související řídicí slova a některé vlastnosti obrázku jako **\bliptagN**. Zde **N** znamená číselný parametr. Analyzátor RTF musí umožňovat až 10 číslic, kterým může předcházet znaménko mínus. Pokud je oddělovačem mezera, je zahozena, to znamená, že není zahrnuta do následného zpracování.
* Jakýkoli znak jiný než písmeno nebo číslice. V tomto případě oddělovací znak ukončuje řídicí slovo a není součástí řídicího slova. Například zpětné lomítko „\“, což znamená, že následuje nové řídicí slovo nebo řídicí symbol.

#### Ovládací symbol ####

Kontrolní symbol představuje zvláštní výskyt, který má specifický význam v závislosti na jeho obsahu. Skládá se ze zpětného lomítka následovaného speciálním znakem (neabecední znak) a nemá žádné oddělovače.

#### Skupina ####

Skupina se může skládat z textu, řídicích slov nebo řídicích symbolů uzavřených ve složených závorkách (**{ }**). Úvodní složená závorka (**{** ) označuje začátek skupiny a uzavírací složená závorka ( **}**) označuje konec skupiny. Každá skupina určuje text ovlivněný skupinou a různé atributy tohoto textu.

### Struktura souborů RTF ###

Soubor RTF má následující standardní syntaxi:

Formát Rich Text Format (**RTF**) představený a zdokumentovaný společností Microsoft představuje metodu kódování formátovaného textu a grafiky pro použití v aplikacích. Tento formát usnadňuje výměnu dokumentů mezi platformami s jinými produkty společnosti Microsoft, čímž slouží účelu interoperability. Tato schopnost z něj činí standard přenosu dat mezi softwarem pro zpracování textu, a proto lze obsah přenášet z jednoho operačního systému do druhého bez ztráty formátování dokumentu. Specifikace formátu souborů jsou k dispozici od společnosti Microsoft k veřejnému stažení a lze na ně odkazovat z pohledu vývojáře.

#### Záhlaví RTF ####

Záhlaví RTF má následující znázornění.

|Pole|Popis
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Tabulky záhlaví se musí objevit v tomto pořadí, pokud existují. Soubor RTF může obsahovat skupiny pro písma, styly, barvu obrazovky, obrázky, poznámky pod čarou, komentáře (anotace), záhlaví a zápatí, souhrnné informace, pole, záložky, vlastnosti formátování dokumentů, oddílů, odstavců a znaků, matematiku, obrazy a předměty. Pokud jsou v souboru zahrnuty písmo, soubor, styl, barva, revizní značka a skupiny souhrnných informací a vlastnosti formátování dokumentu, musí se objevit v záhlaví RTF, které předchází tělo RTF. Pokud není použit obsah kterékoli skupiny, lze skupinu vynechat. Každá skupina, která používá vlastnosti definované v jiné skupině, se musí objevit za skupinou, která tyto vlastnosti definuje. Například vlastnosti barvy a písma musí předcházet skupině stylů.

#### Verze RTF ####

Dokument RTF musí začínat těmito šesti znaky:

```
{\rtf1
```
kde 1 ukazuje číslo verze RTF.

#### Sada znaků ####

Po {\rtf1 by měl dokument deklarovat, jakou znakovou sadu používá. Způsob, jak deklarovat znakovou sadu, je pomocí jednoho z těchto příkazů:

`\ansi` - Dokument je ve znakové sadě ANSI, známé také jako kódová stránka 1252, obvyklé znakové sadě MSWindows.

`\mac` - Dokument je ve znakové sadě MacAscii, obvyklé znakové sadě ve starých (před 10) verzích Mac OS.

`\pc` - Dokument je na kódové stránce DOS 437, což je výchozí znaková sada pro MS-DOS. Písaři s dobrou svalovou pamětí si všimnou, že toto je znaková sada, která se stále používá pro interpretaci „Alt numerických“ kódů – tj. když podržíte Alt a na numerické klávesnici napíšete „130“, vytvoří se é, protože znak 130 v CP437 je é. To je asi jediné využití, které CP437 v dnešní době vidí.

`\pca` - Dokument je na kódové stránce DOS 850, známé také jako vícejazyčná kódová stránka MS-DOS.

#### Příkaz písma ####

Za definicí znakové sady následuje příkaz `\deffN`. To definuje, že číslo písma N je výchozí písmo pro tento dokument. Číslo písma N je odvozeno z tabulky písem. Příkaz `\deffN` je technicky volitelný, ale měl by tam být, aby byl na bezpečné straně jako běžný prolog, jako je následující výběr fontu 0 jako výchozího fontu.

`{\rtf1\ansi\deff0`

#### Tabulka písem ####

Všechna písma, která lze v dokumentu použít, jsou uvedena v tabulce písem, kde je každé písmo zastoupeno číslem písma. Dokument musí mít tabulku písem, i když některé programy budou fungovat i bez ní.

Syntaxe tabulky písem je {\fonttbl //...declarations//...}, ve které má každá deklarace tuto základní syntaxi:

`{\fnumber\familycommand Název písma;}`

Tabulka písem se čtyřmi deklaracemi je následující:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

V dokumentu s touto tabulkou písem by `{\f2 stuff}` vytisklo „věci“ v Courier New. Písmo nelze v dokumentu použít, dokud není uvedeno v tabulce písem.

### Konec dokumentu ###

Každý dokument RTF musí končit znakem }, aby se uzavřela skupina otevřená znakem {, který je prvním znakem v dokumentu. Za konečnou } nemůže následovat nic, možná kromě nového řádku.

## Reference ##

* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)
