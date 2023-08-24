{
  "date" : "2021-03-30",
  "keywords" :[ "PMLZ", "Zipped Palm Markup Language File", "extension", "File", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru PMLZ, jazyku Palm Markup Language a rozhraních API, která mohou vytvářet a otevírat soubory PMLZ.",
  "title" :"PMLZ - Zipped Palm Markup Language File",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Co je soubor PMLZ?

Palm Inc představil typ souboru eBook; známý jako formát souboru PMLZ, což je komprimovaná verze formátu souboru [PML](/cs/ebook/pml/), proto jsou soubory s příponou .pmlz známé jako **Zipped Palm Markup Language File**. Soubor PMLZ je pouze kontejner zip souboru, který kompiluje soubory [PDB](/cs/programming/pdb/) za účelem vytvoření dokumentů pro **eReader** (známý jako zařízení pro čtení elektronických knih, jako je tablet). Soubor PML poskytuje rozvržení souboru PDB (obsahujícího různé datové soubory), který se zobrazí na zařízení Palm. Zatímco soubor PDB je databázový soubor, který používají různé aplikace, včetně Quicken, Pegasus, Microsoft Visual Studio a Palm Pilot. Stručně řečeno, PMLZ je komprimovaný kontejner souborů PML a PDB.


## Znalost jazyka Palm Markup Language
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
| \o | Blok Overstrike; uzavřít s \o |
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

