{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Přečtěte si o formátu souboru MCA a rozhraních API, která mohou vytvářet a otevírat soubory MCA.",
  "title": "MCA - Formát souboru Minecraft Anvil Region",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-csa"
}
},
  "lastmod": "2022-12-13"
}

## Co je soubor MCA?

Formát souboru oblasti Minecraft Anvil je formát pro ukládání dat, který se používá k ukládání kousků terénu ze světa Minecraft v populární videohře **Minecraft**. Svět Minecraftu se skládá z regionů, kde je každý region rozdělen na kousky. Formát souboru MCA umožňuje efektivní ukládání velkého množství herních dat, jako je umístění bloků a entit v určité části herního světa. Soubory MCA je třeba zkombinovat s jinými soubory MCA, aby se vytvořil celý svět.

Kromě ukládání herních dat zahrnuje formát souboru oblasti Anvil také podporu pro různé další typy dat, jako jsou data hráčů a metadata. To umožňuje efektivní ukládání všech informací potřebných k úplnému znovuvytvoření určitého kusu herního světa, včetně umístění bloků, entit a dalších herních objektů.

## Formát souboru MCA – Další informace

Formát souboru oblasti kovadliny je variantou formátu NBT (Named Binary Tag), což je hierarchická stromová struktura pro ukládání dat v binárním souboru. To umožňuje efektivní ukládání složitých datových struktur v kompaktním a snadno čitelném formátu.

### Bloky v souboru MCA

V Minecraftu je kus 16x16x16 bloková oblast herního světa, která je načtena do paměti a vykreslena na obrazovce hráče. Formát souboru oblasti kovadliny ukládá všechna data pro konkrétní blok do jediného souboru, který lze v případě potřeby rychle načíst do paměti. To umožňuje efektivní úložiště a rychlý přístup k herním datům, což je důležité pro zajištění plynulého a bezproblémového herního zážitku.

### Malá velikost souboru MCA

Jednou z klíčových vlastností formátu souboru Anvil region je jeho použití komprese. To umožňuje efektivní ukládání velkého množství dat, aniž by byla obětována kvalita dat nebo rychlost, s jakou k nim lze přistupovat. Toho je dosaženo pomocí různých technik, jako je komprese gzip a komprese dat bloků.

Komprimovaný formát souborů MCA z něj dělá důležitou součást herního systému pro ukládání a správu dat. Jeho efektivní využití komprese a podpora různých typů dat umožňuje efektivní ukládání a rychlý přístup k herním datům, což hráčům zajišťuje hladký a bezproblémový herní zážitek.

## Struktura formátu souborů MCA

Vnitřní struktura formátu souborů MCA se skládá z:
 * Záhlaví a a
 * Užitečné zatížení

### Záhlaví MCA

Záhlaví souboru oblasti MCA začíná 8KiB záhlavím, které je rozděleno do dvou 4KiB tabulek. První tabulka obsahuje offsety bloků v samotném souboru regionu, zatímco druhá tabulka poskytuje časové značky pro poslední aktualizace těchto bloků.

### Užitečné zatížení MCA

MCA Payload se skládá z bloků, kde každá data bloku začínají čtyřbajtovým polem délky (big-endian). Toto pole udává přesnou délku zbývajících dat bloku v bajtech. Data posledního bloku jsou vyplněna tak, aby byla násobkem délky 4096B. Minecraft nepřijímá soubory, kde poslední část není vycpaná.

## Jak otevřít soubory MCA

Soubory MCA můžete otevírat a upravovat pomocí programu MCEdit, což je bezplatný editor s otevřeným zdrojovým kódem pro Minecraft. Můžete [download MCEdit](https://www.mcedit.net/) z oficiální webové stránky a použít ji k otevření a zobrazení obsahu vašeho souboru oblasti Anvil.

Jakmile máte nainstalovaný MCEdit, můžete otevřít soubor oblasti Anvil podle následujících kroků:

 1. Spusťte MCEdit a klikněte na tlačítko Otevřít v levém horním rohu okna.

 1. V dialogovém okně Otevřený svět přejděte do umístění souboru oblasti Anvil a vyberte jej.

 1. Kliknutím na tlačítko Otevřít otevřete soubor v MCEdit.

 1. MCEdit načte soubor a zobrazí jeho obsah v hlavním okně. Poté můžete použít nástroje a funkce v MCEdit k zobrazení, úpravě a extrahování dat ze souboru oblasti Anvil.

## Reference

* [Světový editor pro Minecraft](https://www.mcedit.net/)

* [O Minecraftu](https://www.minecraft.net/)

* [Formát souboru regionu](https://minecraft.fandom.com/wiki/Region_file_format)


