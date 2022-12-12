{
  "date" : "2020-03-16",
  "keywords" :[ "Soubor IFC", "Formát", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souborů IFC a rozhraních API, která mohou vytvářet a otevírat soubory IFC.",
  "title" :"Formát souboru IFC",
  "linktitle" : "IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor IFC?

Soubory s příponou IFC odkazují na formát souborů Industry Foundation Classes (IFC), který zavádí mezinárodní standardy pro import a export stavebních objektů a jejich vlastností. Tento formát souboru poskytuje interoperabilitu mezi různými softwarovými aplikacemi. Specifikace pro tento formát souboru jsou vyvinuty a udržovány společností buildingSMART International jako její datový standard. Konečným cílem formátu souborů IFC je zlepšit komunikaci, produktivitu, dodací lhůty a kvalitu v průběhu životního cyklu budovy.

Díky zavedeným standardům pro běžné objekty ve stavebnictví snižuje ztráty informací při přenosu z jedné aplikace do druhé. IFC může uchovávat data pro geometrii, výpočty, množství, facility management, cenotvorbu atd. pro mnoho různých profesí (architekt, elektro, HVAC, konstrukce, terén atd.).

## Stručná historie ##

Iniciativu IFC převzal v roce 1994 Autodesk na podporu integrovaného vývoje aplikací a zahrnoval společnosti jako Honeywell, Butler Manufacturing a AT&T. V roce 1995 bylo členství otevřeno pro kohokoli a název byl změněn na International Alliance for Interoperability. Záměrem neziskové organizace bylo publikovat Industry Foundation Class (IFC) jako model produktu AEC. V roce 2005 byl název znovu změněn a buildSMART jej nyní udržuje.

## Formát souboru IFC ##

Formát souboru IFC prošel v minulosti několika změnami, aby dosáhl specifikace formátu souboru v4. Čas od času došlo k několika drobným změnám, které byly součástí specifikací jako dodatky. Následuje seznam různých verzí specifikací souborů, které byly zveřejněny v minulosti.

* IFC4 Add2 (2016) IFC4 Add1 (2015)
* IFC4 (březen 2013) ifcXML2x3 (červen 2007)
* IFC2x3 (únor 2006) ifcXML2 pro IFC2x2 add1 (RC2)
* IFC2x2 Addendum 1 (červenec 2004)ifcXML2 pro IFC2x2 (RC1)
* IFC 2x2IFC 2x Dodatek 1ifcXML1 pro IFC2x a
* IFC2x Dodatek 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Nejnovější verze specifikací formátu souborů IFC jsou vždy k dispozici na webových stránkách buildingSMART a vývojáři by je měli konzultovat pro jakýkoli typ aplikací, které plánují vyvíjet. V době psaní tohoto článku jsou specifikace verze 4 nejnovější dostupné online.

### Formáty datových souborů IFC ###

Formát souboru IFF podporuje výměnu dat mezi aplikacemi pomocí různých formátů, jak je uvedeno níže:

**IFC:** Toto je výchozí formát výměny IFC a používá fyzickou strukturu souborů STEP podle ISO 10303-21. Tento formát souboru má příponu .ifc a je nejčastěji používaným formátem IFC.

**IFC-XML:** Je to verze IFC ve formátu souboru XML, kterou lze generovat přímo odesílající aplikací podle struktury ISO 10303-28, také nazývané STEP-XML. Formát souboru IFC-XML je považován za vhodný pro interoperabilitu mezi nástroji XML. Ve srovnání s formátem souborů IFC je IFC-XML o 300–400 % větší.

**IFC-ZIP:** Je to [ZIP](/cs/compression/zip/) komprimovaná verze IFC nebo IFC-XML, kde jeden z těchto souborů leží v hlavním adresáři zip archivu. Tento formát komprimuje soubor .ifc dolů o 60–80 % a soubor .ifc XML o 90–95 %.

### Architektura IFC ###

Specifikace IFC zahrnuje termíny, koncepty a položky specifikace dat, které pocházejí z použití v oborech, řemeslech a profesích odvětví stavebnictví a správy budov. Termíny a koncepty používají jednoduchá anglická slova, datové položky ve specifikaci dat se řídí konvencí pojmenování.

názvy datových položek pro typy, entity, pravidla a funkce začínají předponou „Ifc“ a pokračují anglickými slovy podle konvence pojmenování CamelCase (bez podtržítka, první písmeno ve slově velké); názvy atributů v rámci entity se řídí konvencí pojmenování CamelCase bez předpony; definice sady vlastností, které jsou součástí tohoto standardu, začínají předponou "Pset_" a pokračují anglickými slovy v konvenci pojmenování CamelCase; definice sady množství, které jsou součástí tohoto standardu, začínají předponou "Qto_" a pokračují anglickými slovy podle konvence pojmenování CamelCase.

Architektura datového schématu IFC definuje čtyři koncepční vrstvy, každé jednotlivé schéma je přiřazeno právě jedné koncepční vrstvě.

**Vrstva zdrojů** — nejnižší vrstva zahrnuje všechna jednotlivá schémata obsahující definice zdrojů, tyto definice neobsahují globálně jedinečný identifikátor a nelze je používat nezávisle na definici deklarované ve vyšší vrstvě;

**Základní vrstva** — další vrstva obsahuje schéma jádra a schémata rozšíření jádra, obsahující nejobecnější definice entit, všechny entity definované na základní vrstvě nebo výše nesou globálně jedinečné id a volitelně informace o vlastníkovi a historii;

**Vrstva interoperability** — další vrstva obsahuje schémata obsahující definice entit, které jsou specifické pro obecný produkt, proces nebo specializaci zdrojů používanou v několika disciplínách, tyto definice se obvykle používají pro výměnu mezi doménami a sdílení konstrukčních informací;

**Vrstva domény** — nejvyšší vrstva obsahuje schémata obsahující definice entit, které jsou specializací produktů, procesů nebo zdrojů specifických pro určitou disciplínu, tyto definice se obvykle používají pro výměnu a sdílení informací v rámci domény.

## Reference ##

* [Industry Foundation Classes – podle Wikipedie](https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

