{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Přečtěte si o formátu souborů Unreal Static Meshes VPK a rozhraních API, která mohou vytvářet a otevírat soubory VPK.",
  "title" : "Soubor VPK - Unreal Static Meshes File",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-cs",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Co je soubor VPK?

Soubor .vpk je formát souboru používaný **Source Engine**, herním enginem vyvinutým společností Valve Corporation. Soubory VPK se používají k balení herního obsahu, jako jsou modely, textury a zvuky, a běžně se používají ve hrách jako Team Fortress 2, Left 4 Dead a Counter-Strike: Global Offensive. Soubory lze otevřít a extrahovat pomocí různých nástrojů, jako je GCFScape a VPK Tool.

## Formát souboru VPK – Další informace

Soubory VPK se ukládají na disk jako binární soubory. Jeden soubor vpk může být součástí balíčku VPK nebo může fungovat jako nezávislý nezpracovaný soubor VPK. Informace, které lze uložit do souboru VPK, zahrnují mapy, materiály, obsah hry a choreografické scény.

### Jak vytvořit soubor VPK?

Existuje několik způsobů, jak vytvořit soubor .vpk, v závislosti na dostupných nástrojích.

1. `Použití nástroje VPK:` Toto je nástroj příkazového řádku, který lze použít k vytváření a extrahování souborů VPK. Soubor VPK lze vytvořit pomocí následujícího příkazu:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Tím se vytvoří soubor VPK ze zadaného adresáře a uloží se jako zadaný výstupní soubor.

1. `Použití Hammer Editoru:` Hammer Editor je nástroj, který je součástí Source SDK, který lze použít k vytváření a úpravám úrovní pro hry, které používají Source engine. Zahrnuje také možnost vytvářet soubory VPK kliknutím pravým tlačítkem myši na složku na kartě Systém souborů a výběrem možnosti Vytvořit VPK

1. `Pomocí tvůrce VPK od Valve:` Toto je nástroj vyvinutý společností Valve, který se používá k balení a distribuci herního obsahu. Tento nástroj lze použít k vytváření souborů VPK a také je to oficiální nástroj pro vytváření souborů VPK.

## Reference

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [Zdroje pro vývojáře VPK](https://developer.valvesoftware.com/wiki/GCF)

