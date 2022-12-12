{
  "date" : "2019-10-11",
  "keywords" :[ "soubor odg", "formát souboru odg", "co je soubor odg", "soubor", "příklad odg", "přípona souboru odg", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru ODG",
  "description":"Další informace o formátu souboru ODG a rozhraních API, která mohou vytvářet a otevírat soubory ODG.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor ODG?

Formát souboru ODG používá aplikace Draw Apache OpenOffice k ukládání prvků výkresu jako vektorový obrázek. Řídí se specifikacemi formátu souborů založenými na XML, které jsou uvedeny v Advancement of Structural Information Standards (OASIS). ODG představuje kresby jako vektorové obrázky pomocí bodů, čar a křivek. Kromě OpenOffice, LibreOffice a další aplikace poskytují podporu pro práci se souborovým formátem ODG. Mezi další formáty podporované OpenOffice patří například [ODT](/cs/textový procesor/odt/), ODF, [ODP](/cs/prezentace/odp/) a [ODS](/cs/tabulkový procesor/ods/).


## Specifikace formátu souboru ODG

Formát souboru ODG je založen na formátu OpenDocument, což je strukturovaný formát dokumentu XML s dobře definovaným schématem.
Každá strukturální komponenta formátu OpenDocument je reprezentována prvkem, který má přidružené atributy. Struktura založená na XML je společná pro všechny typy dokumentů, jako je textový dokument, tabulkový procesor nebo soubor výkresu. Dokument může obsahovat různé styly. Souborová struktura OpenDocument se skládá z následujících prvků.
* Kořen dokumentu
* Metadata dokumentu
* Typy prvků těla a dokumentů
* Nastavení aplikace
* Skripty
* Prohlášení o vzhledu písma
* Styly
* Styly a rozvržení stránek

## Kořeny dokumentu ##

Kořenový prvek dokumentu obsahuje celý dokument a je primárním prvkem souboru ve formátu OpenDocument. Stejné typy kořenových prvků dokumentu jsou použitelné pro všechny typy dokumentů, jako je text, dokumenty, tabulky a výkresové dokumenty.

### Kořenové prvky ###
Jediný dokument XML je reprezentován svým vlastním kořenovým prvkem. Pět různých podporovaných kořenových prvků je následujících.

`<office:document> ` - Kompletní kancelářský dokument v jediném XML dokumentu.
`<office:document-content> ` - Obsah dokumentu a automatické styly použité v obsahu.
`<office:document-styles> ` - Styly použité v obsahu dokumentu a automatické styly použité v samotných stylech.
`<office:document-meta> ` - Metainformace dokumentu, jako je autor nebo čas poslední akce uložení.
`<office:document-settings> ` - Nastavení specifická pro aplikaci, jako je velikost okna nebo informace o tiskárně.

### Metadata dokumentu ODG ###
OpenDocument obsahuje všechny prvky metadat v \<office:meta> živel. Tyto obecné informace o dokumentu jsou obsaženy na začátku dokumentu a aplikace mohou aktualizovat více instancí stejných prvků.

### Typy prvků těla a dokumentů ###
Tělo dokumentu označuje typ obsahu obsaženého v dokumentu pomocí prvku typu dokumentu. Jedná se o tyto typy dokumentů:
* textové dokumenty
* výkresové dokumenty
* prezentační dokumenty
* tabulkové dokumenty
* grafové dokumenty
* obrazové dokumenty

### Nastavení aplikace ###
Nastavení pro kancelářské aplikace představují různá nastavení, která souvisí s konfigurací dokumentu nebo vizuálním vzhledem dokumentu. Každá kategorie je reprezentována znakem `<config:config-item-set> `. Příklady takových kategorií nastavení zahrnují:
* Nastavení dokumentu, např. výchozí tiskárna
* Nastavení zobrazení, např. úroveň přiblížení

### Skripty ###
Je běžné, že dokument obsahuje několik skriptů. Každý skript v souboru OpenDocument je reprezentován znakem `<office:script> ` prvek. Tyto prvky skriptu jsou obsaženy v jediném `<office:scripts> ` prvek. Skripty neaktualizují dokument, když se dokument načítá.
### Prohlášení o vzhledu písma ###

Deklarace fontu obsahuje informace o fontech používaných autorem dokumentu. Tyto informace pomáhají najít tato písma v jiných systémech.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Styly ###
Následující styly jsou podporovány formátem OpenDocument.

"Běžné styly" - XML reprezentace takových stylů se označují jako styly
`Automatické styly` – Obsahuje vlastnosti formátování, které jsou v zobrazení uživatelského rozhraní dokumentu přiřazeny objektu, jako je odstavec.
„Styly hlavní“ – běžný styl, který obsahuje informace o formátování a další obsah, který se zobrazí s obsahem dokumentu, když je styl aplikován. Příkladem vzorového stylu jsou vzorové stránky.

## Reference ##
* [Formát otevřených dokumentů OASIS pro aplikace Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [Formát OpenDocument – Wikipedie](https://en.wikipedia.org/wiki/OpenDocument)

