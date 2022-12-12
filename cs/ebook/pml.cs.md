{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "rozšíření", "formát", "eKniha", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru PML, jazyku Palm Markup Language a rozhraních API, která mohou vytvářet a otevírat soubory PML.",
  "title" :"PML - Palm Markup Language File",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Co je soubor PML?

Palm Inc představil souborový formát PML, což je zkratka pro Palm Markup Language File. Jeho účelem je vytvářet dokumenty pro eReader, což je zařízení pro čtení elektronických knih podobné tabletovému počítači. Soubor PML poskytuje rozložení souboru [PDB](/cs/ebook/pdb/) (obsahujícího různé datové soubory) k zobrazení na zařízení Palm.

## Technické detaily souborů PML

Struktura souborů PML se skládá ze značek pro vytvoření nastavení elektronické knihy, včetně odstavců, nadpisů, odsazení a odkazů. Umožňuje také formátování značek, jako je tučné písmo, velká písmena a horní index. Vývojáři mohou do elektronických knih také přidávat obrázky.

### Značkovací jazyk Palm
Následující tabulka uvádí příkazy PML:

|Příkaz|Popis|
---|---|
| \p | Nová stránka |
| \x | Nová kapitola; také způsobí zalomení nové stránky. Název kapitoly (a případné kódy stylů) uzavřete pomocí \x a \x |
| \Xn | Nová kapitola, odsazená n úrovní (n mezi 0 a 4 včetně) v dialogu Kapitola; nezpůsobuje přerušení stránky. Název kapitoly (a jakékoli kódy stylů) uzavřete pomocí \Xn a \Xn |
| \Cn="Název kapitoly" | Vložte "Název kapitoly" do seznamu kapitol s úrovní n (jako \Xn). Text se na stránce nezobrazí a nevynutí zalomení stránky. Někdy může být užitečné vložit značku kapitoly například na začátek úvodu ke kapitole. |
| \c | Vycentrovat tento blok textu; zavřete \c na začátku řádku |
| \r | Textový blok zarovnat vpravo; zavřete \r na začátku řádku |
| \i | Kurzívou blok; zavřít s \i |
| \u | Blok podtržení; zavřít \u |
| \o | Blok Overstrike; zavřít s \o |
| \v | Neviditelný text; zavřít pomocí \v (lze použít pro komentáře) |
| \t | Blok odsazení. Začněte na začátku řádku, zavřete \t na konci řádku |
| \T="50 %" | Odsadí zadané procento šířky obrazovky, v tomto případě 50 %. Pokud je aktuální pozice výkresu již za zadaným umístěním obrazovky, bude tento tag ignorován. |
| \w="50 %" | Vložte vodorovné pravidlo dané šířky obrazovky v procentech, v tomto případě 50 %. Tato značka způsobuje zalomení řádku před a za ní. Pravidlo je vycentrováno. Znak procenta je povinný. |
| \n | Přepněte na "normální" font, který je určen uživatelem |
| \s | Přepnout na stdFont; zavřete pomocí \s pro návrat k normálnímu písmu |
| \b | Přepnout na tučné písmo; zavřete pomocí \b pro návrat k normálnímu písmu (zastaralé; místo toho použijte \B) |
| \l | Přepnout na velké písmo; zavřete pomocí \l pro návrat k normálnímu písmu |
| \B | Označte text jako tučný. Na rozdíl od značky \b \B nemění písmo, takže můžete mít velký tučný text. Nemůžete kombinovat \ba \B ve stejném souboru PML. |
| \Sp | Označte text jako horní index. Nemělo by se míchat s jinými styly, jako je tučné písmo, kurzíva atd. Text v horním indexu uzavřete pomocí \Sp. |
| \Sb | Označte text jako dolní index. Nemělo by být kombinováno s jinými styly, jako je tučné písmo, kurzíva atd. Text v dolním indexu uzavřete pomocí \Sb. |
| \k | Udělejte uzavřený text na malá písmena; zavřít \k. Jakékoli znaky uzavřené ve značkách \k (včetně znaků s diakritikou) jsou velká a jsou vykresleny s menší bodovou velikostí než běžná velká písmena. |
| \\ | Představuje jedno zpětné lomítko |
| \aXXX | Vložte jiný znak než ASCII, jehož kód Windows-1252 je desítkové XXX. Podrobnosti naleznete v tabulce znaků PML. |
| \UXXXX | Vložte jiný znak než ASCII, jehož kód Unicode je hexadecimální XXXX. Podrobnosti viz Rozšířená tabulka znaků PML. |
| \m="název obrázku.png" | Vložte pojmenovaný obrázek. Viz část Obrázky níže. |
| \q="#linkanchor"Nějaký text\q | Odkazujte na kotvu odkazu, která je na jiném místě v dokumentu. Řetězec za specifikací kotvy a před koncovým \q je při prohlížení dokumentu podtržen nebo jinak zobrazen jako odkaz. |
| \Q="linkanchor" | Zadejte kotvu odkazu v dokumentu. |
| \- | Vložte měkkou pomlčku. Měkká pomlčka se zobrazí pouze v případě, že je nutné zalomit slovo přes řádek. |
| \Fn="poznámka1"1\Fn | Propojte „1“ s poznámkou pod čarou, jejíž název je poznámka pod čarou1, označenou na konci dokumentu PML. Viz část Poznámky pod čarou a postranní panely níže. |
| \Sd="sidebar1"sidebar\Sd | Propojte text "Postranní panel" s postranním panelem, jehož název je sidebar1, označený na konci dokumentu PML. Viz část Poznámky pod čarou a postranní panely níže. |
| \I | Označit jako referenční položku indexu. Uzavřete položku indexu (a jakékoli kódy stylů) pomocí \I a \I.|
 


## Reference

* [Palm Markup Language – od MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader – By MobileRead](https://en.wikipedia.org/wiki/E-reader)

