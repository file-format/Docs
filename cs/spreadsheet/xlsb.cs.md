{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "soubor", "přípona", "formát souboru", "Binární tabulkový soubor Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souboru, abyste věděli, co je soubor XLSB a rozhraní API, která je mohou vytvářet a otevírat.",
  "title" :"Co je soubor XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Co je soubor XLSB?

Formát souboru XLSB určuje formát binárního souboru aplikace Excel, což je kolekce záznamů a struktur, které určují obsah sešitu aplikace Excel. Obsah může zahrnovat nestrukturované nebo polostrukturované tabulky čísel, text nebo čísla i text, vzorce, externí datová připojení, grafy a obrázky. Na rozdíl od [XLSX](/cs/spreadsheet/xlsx/) (který je založen na formátu souboru Open XML), XLSB představuje binární soubor sešitu aplikace Excel. Soubory XLSB lze číst a zapisovat rychleji, což je činí užitečnými pro práci s velkými soubory. XLSB se k ukládání sešitů používá jen zřídka, protože XLSX (a dříve [XLS](/cs/spreadsheet/xls/)) jsou nejběžnější uživatelem vybrané formáty souborů pro ukládání sešitů. Lze jej otevřít pomocí sady Microsoft Office 2007 a vyšší.

## Specifikace formátu souboru XLSB ##

Specifikace formátu souboru pro formát souboru XLSB byly zveřejněny již v roce 2008 jako verze 1.0. Od té doby byly specifikace několikrát revidovány a nejnovější verze specifikací (v 10.0) byla zveřejněna v dubnu 2018. Specifikace jsou veřejně dostupné společností Microsoft jako [[MS-XLSB] – specifikace formátu binárního souboru Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) a měl by se s ním kdokoli seznámit při čtení nebo zápisu souborů ve formátu XLSB.

## Struktura souboru XLSB ##

Soubor XLSB je balíček, který se skládá z kolekce částí. Tyto části obsahují informace o obsahu sešitu, včetně dat sešitu a struktury balíčku. Některé části obsahují informace uložené pomocí binárních záznamů, některé jako XML, zatímco jiné obsahují informace uložené jako binární proud bajtů. Každý binární záznam obsahuje nula nebo více strukturovaných polí, která obsahují data sešitu.

#### Balíček ####

Balíček XLSB je archiv [ZIP](/cs/compression/zip/), který musí obsahovat právě jednu část sešitu. Tato část musí být cílem vztahu v této části vztahu balíčku. Část sešitu je výchozí částí dokumentu XLSB.

#### Část ####

Část je proud bajtů, který má přidružený typ obsahu, který určuje povahu a typ obsahu uloženého v části. Některé části ukládají informace v binárním formátu, zatímco jiné ukládají informace jako XML. Část [výčet součástí](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) dokumentu specifikací uvádí platné části, typy obsahu a povinné/volitelné vztahy mezi všechny díly v balení.

#### Vztah ####

Zdroj a cílový zdroj jsou spojeny vztahem. Vztahy mohou být:

**Vztah k balíčku:** kde cíl je část a zdroj je balíček jako celek

**Vztah mezi částmi:** kde cíl je součást a zdroj je součástí balíčku

**Explicitní vztah:** kde je zdroj odkazován z obsahu zdrojové části odkazem na hodnotu atributu ID prvku vztahu

**implicitní vztah** je vztah, který není explicitní

**Vnitřní vztah:** kde cíl je součástí balíčku

**Externí vztah:** kde cíl je externí zdroj, který není součástí balíčku

#### Záznam ####

Záznam je základní stavební blok používaný k ukládání informací o funkcích v sešitu. Každý binární záznam je sekvence bajtů s proměnnou délkou. Binární záznam se skládá ze tří částí:

* typ záznamu
* rekordní velikost a
* data záznamu, která jsou specifická pro daný typ záznamu.

**Typ záznamu:** Typ záznamu zobrazuje typ záznamu specifikovaný záznamem. Specifikuje také strukturu dat záznamu specifických pro tento záznam. Platné typy záznamů jsou uvedeny v části [Výčet záznamů](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) dokumentu se specifikacemi. Typ záznamu musí být jeden nebo dva bajty a musí být větší nebo roven 128 a menší než 16384.

**Velikost záznamu:** Velikost záznamu určuje počet bajtů, který určuje celkovou velikost dat záznamu. Tato hodnota MUSÍ být jeden až čtyři bajty. Tato hodnota MUSÍ být jeden bajt, pokud je horní bit v dolním bajtu roven 0; jinak MUSÍ být tato hodnota větší než jeden bajt. Pokud je počet bajtů větší než jeden bajt, horní bit v každém následujícím bajtu určuje, zda se použije další bajt. Pokud je horní bit druhého bajtu roven 1, pak tato hodnota MUSÍ použít další třetí bajt. Pokud je horní bit třetího bajtu roven 1, pak tato hodnota MUSÍ použít další čtvrtý bajt. Vysoký bit čtvrtého bajtu MUSÍ být ignorován. Hodnota se skládá ze sedmi nízkých bitů každého bajtu dohromady. Nízké, nejméně významné bity jsou obsaženy v prvním bajtu a každý následující bajt obsahuje bity vyššího řádu než předchozí bajt.

**Data záznamu:** Složka dat záznamu obsahuje pole, která odpovídají konkrétnímu typu záznamu a tvoří zbytek záznamu. Pořadí a struktura polí pro daný typ záznamu uvedených ve Výčtu záznamů je specifikována v odpovídající části pro daný typ záznamu v Záznamech. Celková velikost datové složky záznamu MUSÍ být rovna velikosti záznamu. Pole v komponentě dat záznamu mohou obsahovat jednoduché hodnoty, pole hodnot, struktury několika polí, pole polí a pole struktur.

#### Příklad záznamu XLSB ####

Následující typ záznamu a velikost záznamu určují záznam **BrtCommentText** o velikosti 200 bajtů:

11111101 00000100 11001000 00000001 [Pole záznamů]

První bajt je 11111101, což určuje nízkou hodnotu 125 a typ záznamu vyžaduje druhý bajt. Druhý bajt je 00000100 a určuje vysokou hodnotu 4 * 128, což se rovná 512. Hodnota typu záznamu je 125 + 512 nebo 637, což odpovídá typu záznamu **BrtCommentText**. Další bajt je 11001000, což určuje nízkou hodnotu 72 a že velikost záznamu vyžaduje druhý bajt. Druhý bajt je 00000001, udává vyšší hodnotu 1 * 128 a že velikost záznamu nevyžaduje další bajt. Velikost záznamu je 72 + 128 nebo 200, což udává celkovou velikost složky dat záznamu v bajtech. Pole v komponentě dat záznamu jsou specifikována **BrtCommentText**.

## Reference ##

* [[MS-XLSB] – formát binárního souboru Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

