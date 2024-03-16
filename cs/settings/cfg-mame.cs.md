{
"datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg soubor",
"konfigurační soubor cfg mame",
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
"title": "Formát souboru CFG - konfigurační soubor MAME",
  "description":"Další informace o formátu konfiguračního souboru CFG MAME a rozhraních API, která mohou vytvářet a otevírat soubory CFG.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame",
      "parent": "settings"
}
},
"lastmod": "27.09.2023"
}

## Co je soubor CFG?

Soubor CFG je konfigurační soubor klávesnice XML používaný emulátory arkádových videoher MAME. Je to klíčová součást pro přizpůsobení ovládacích prvků klávesnice a klávesových zkratek tak, aby vyhovovaly preferencím hráče. Tyto soubory ukládají mapování a nastavení, která určují, jak klávesnice při hraní hry spolupracuje s emulátorem. Úpravou tohoto souboru mohou uživatelé přizpůsobit svůj herní zážitek přiřazením konkrétních kláves na klávesnici akcím ve hře, jako je vkládání mincí, spuštění, pohyb a různé další funkce.

## Konfigurační soubor MAME

MAME, což je zkratka pro **Multiple Arcade Machine Emulator**, je softwarová aplikace, která vám umožňuje emulovat a hrát arkádové hry na vašem počítači. MAME používá konfigurační soubory k přizpůsobení svého chování a nastavení. Tyto konfigurační soubory jsou obvykle umístěny ve složce `cfg` v adresáři MAME.

Zde jsou hlavní konfigurační soubory, se kterými se můžete setkat při nastavování a konfiguraci MAME:

1. **mame.ini:** Toto je hlavní konfigurační soubor pro MAME. Obsahuje globální nastavení, která platí pro všechny hry. Tento soubor najdete v kořenovém adresáři vaší instalace MAME.

1. **default.cfg:** Tento soubor ukládá výchozí nastavení pro všechny hry, které nemají vlastní konfigurační soubory. Používá se jako záložní pro nastavení specifická pro hru.

1. **game-specific.cfg:** Tyto soubory slouží k uložení nastavení pro jednotlivé hry. Obvykle jsou pojmenovány podle souboru ROM pro hru, které odpovídají. Například pokud máte hru s názvem "pacman.zip", konfigurační soubor pro ni bude "pacman.cfg."

Zde jsou některá běžná nastavení, která můžete najít v konfiguračním souboru MAME.

1. **rompath:** Určuje adresář, kde jsou umístěny ROM vaší arkádové hry.

1. **cfg_directory:** Určuje adresář, kde jsou uloženy konfigurační soubory specifické pro hru.

1. **nvram_directory:** Určuje adresář, ve kterém jsou uloženy soubory NVRAM (non-volatile RAM). NVRAM ukládá nejvyšší skóre a další data specifická pro hru.

1. **adresář_artwork:** Určuje adresář, kde jsou uloženy soubory uměleckých děl (jako jsou rámečky, výřezy a letáky).

1. **samplepath:** Určuje adresář, kde jsou umístěny ukázkové zvukové soubory.

1. **cheatpath:** Určuje adresář, kde jsou umístěny cheatové soubory.

Můžete také nakonfigurovat různá další nastavení, jako jsou možnosti videa a zvuku, ovládací prvky a vstupní zařízení. Chcete-li tato nastavení upravit, otevřete konfigurační soubor v textovém editoru a proveďte potřebné změny.

## MAMA

MAME, což je zkratka pro **"Multiple Arcade Machine Emulator,"** je softwarová aplikace určená k emulaci a replikaci hardwaru historických arkádových strojů a arkádových herních konzolí. Umožňuje uživatelům hrát rozsáhlou knihovnu klasických arkádových her na moderních počítačích a dalších kompatibilních zařízeních. MAME je projekt s otevřeným zdrojovým kódem a stal se oblíbeným emulátorem pro zachování a užívání bohaté historie arkádového hraní.

1. **Emulace:** Primárním účelem MAME je přesně emulovat hardware arkádových strojů, včetně jejich centrálních procesorových jednotek (CPU), zvukových čipů, grafických čipů a vstupních zařízení. Tato úroveň přesnosti zajišťuje, že se hry chovají co nejblíže původnímu arkádovému zážitku.

1. **Kompatibilita:** MAME podporuje širokou škálu ROM arkádových her, což z něj činí jeden z nejkomplexnějších dostupných emulátorů arkád. Může spouštět hry z různých arkádových platforem včetně klasických her ze 70., 80., 90. let a dokonce i některé novější arkádové tituly.

1. **Zachování:** Jedním z hlavních poslání MAME je zachovat historii arkádového hraní. Přesnou emulací arkádového hardwaru pomáhá MAME předcházet ztrátě klasických her a zajišťuje, aby je budoucí generace mohly prožít tak, jak byly původně zamýšleny.

1. **Frond-endy:** Mnoho uživatelů využívá front-end aplikace, které poskytují grafické rozhraní pro správu a spouštění her prostřednictvím MAME. Tyto front-endy usnadňují procházení rozsáhlé knihovny her MAME.

## Jak otevřít soubor CFG?

Programy, které otevírají nebo odkazují na soubory CFG

- MAME (zdarma) (Windows)
- ExtraMAME (zkušební verze)
- MacMAME (MAC)

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
* [MAMA](https://en.wikipedia.org/wiki/MAME)

