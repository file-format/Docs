{
"datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg soubor",
"cfg soubor značkovacího jazyka wesnoth",
"co je soubor cfg",
"jak otevřít soubor cfg",
"soubor",
"přípona souboru cfg",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru CFG - Wesnoth Markup Language File",
  "description":"Další informace o formátu souboru CFG Wesnoth Markup Language File a rozhraní API, která mohou vytvářet a otevírat soubory CFG.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
}
},
"lastmod": "27.09.2023"
}

## Co je soubor CFG?

Soubor CFG je také známý jako **„Wesnoth Markup Language“ (WML)**. Jedná se o vlastní značkovací jazyk používaný především ve hře „Battle for Wesnoth“, což je tahová strategická hra. WML se používá k definování a přizpůsobení různých aspektů hry, včetně scénářů, kampaní, jednotek a dalších. Pro moddery a vývojáře je to způsob, jak vytvářet obsah pro hru.

Je napsán ve formátu, který připomíná kombinaci XML a jednoduchého skriptování. Zde je přehled některých běžných prvků a struktur, které můžete najít v souboru WML:

1. **Tagy:** WML používá značky k definování různých prvků ve hře. Štítky jsou uzavřeny v lomených závorkách. Například:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Atributy:** V rámci značek můžete definovat atributy pro určení vlastností nebo hodnot spojených s prvkem. Ve výše uvedeném příkladu jsou atributy „type“ a „hitpoints“.
    










3. **Arrays a Arrays of Arrays:** Můžete vytvářet pole dat a dokonce pole polí pro definování seznamů jednotek, typů terénu nebo jiných herních prvků.
    










4. **Podmíněné příkazy:** WML podporuje podmíněné příkazy pro řízení toku hry. Například:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Smyčky:** Pomocí smyček můžete procházet seznamy položek nebo opakovaně provádět akce.
    










6. **Zahrnuje:** Do hlavního souboru WML můžete zahrnout další soubory WML a uspořádat a modularizovat svůj obsah.
    










7. **Ovládače událostí:** Můžete definovat obslužné rutiny událostí, které spouštějí akce, když ve hře nastanou určité události.
    











Zde je zjednodušený příklad souboru WML, který definuje vlastní jednotku:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## Bitva o Wesnoth

"The Battle for Wesnoth" je populární a open source tahová strategická hra. Je k dispozici pro více platforem, včetně Mac, Windows, Linux a dalších. Hra, kterou vyvinula oddaná komunita dobrovolníků, je známá svou hlubokou a poutavou hratelností a také bohatým fantasy světem.

Klíčové vlastnosti „The Battle for Wesnoth“ zahrnují:

1. **Fantasy prostředí:** Hra se odehrává ve fantasy světě s různými rasami, včetně lidí, elfů, trpaslíků, orků a dalších. Tradice a vyprávění hry jsou nedílnou součástí její přitažlivosti.
    










2. **Tahová strategie:** Hra je tahová, kde si hráči naplánují a provedou své tahy na šestiúhelníkových mřížkách. Kombinuje taktický boj se strategickým rozhodováním.
    










3. **Kampaně:** Hra nabízí širokou škálu kampaní pro jednoho hráče, z nichž každá má svůj vlastní příběh, postavy a výzvy. Hráči mohou prozkoumat různé příběhy a scénáře.
    










4. **Multiplayer:** „Wesnoth“ podporuje online hru pro více hráčů, což umožňuje hráčům soutěžit proti sobě ve strategických bitvách. Režimy pro více hráčů zahrnují kooperativní hru a kompetitivní zápasy.

## Jak otevřít soubor CFG?

Soubory CFG, které jsou běžně spojovány s jazykem Wesnoth Markup Language (WML) používaným ve hře „The Battle for Wesnoth“, lze snadno upravovat pomocí libovolného standardního textového editoru. Tyto soubory obsahují lidsky čitelný kód napsaný ve WML, který definuje různé aspekty hry, včetně scénářů, jednotek a kampaní.

I když můžete k úpravě souborů CFG použít jakýkoli textový editor, některé pokročilé textové editory jako Emacs a Vi mají k dispozici pluginy pro zvýraznění syntaxe WML. Tyto pluginy poskytují užitečné barevné kódování a formátování, aby uživatelům usnadnily rozlišování různých prvků a struktur v kódu WML.

Programy, které otevírají nebo odkazují na soubory CFG, zahrnují

- The Battle for Wesnoth (zdarma) pro (Windows, MAC, Linux)
- Microsoft Poznámkový blok

## Jiné soubory CFG

Zde jsou další typy souborů, které používají příponu souboru **.cfg**.

**Nastavení**
- [CFG - Celestia Configuration File](/cs/settings/cfg-celestia/)
- [CFG - Soubor připojení serveru Citrix](/cs/settings/cfg-citrix/)
- [CFG - Konfigurační soubor MAME](/cs/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/cs/settings/cfg-lightwave/)

**Hra**
- [CFG - Wesnoth Markup Language File](/cs/game/cfg-wesnoth/)
- [CFG - Konfigurační soubor MUGEN](/cs/game/cfg-mugen/)
- [CFG - konfigurační soubor zdrojového enginu](/cs/game/cfg-sourceengine/)

**Systém a různé**
- [CFG - Soubor CFG](/cs/system/cfg/)
– [CFG – konfigurační soubor modelu Cal3D](/cs/misc/cfg-cal3d/)

## Reference
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
