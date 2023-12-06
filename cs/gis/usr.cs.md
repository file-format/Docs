{
"datum": "2023-08-03",
  "keywords": [
"usr",
"usr soubor",
"co je soubor usr",
"jak otevřít soubor usr",
"soubor",
"přípona souboru usr",
"rozšíření"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formát souboru USR - datový soubor GPS Lowrance",
  "description":"Další informace o formátu USR a rozhraních API, která mohou vytvářet a otevírat soubory USR.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## Co je soubor USR?

Přípona souboru ".usr" také souvisí se zařízeními Lowrance GPS. Zejména se používá pro ukládání dat GPS ve formátu známém jako „Formát uživatelských dat“ (formát USR), který používají zařízení Lowrance GPS.

Při použití jednotky Lowrance GPS můžete uložit své trasové body, trasy a trasy jako soubory „.usr“. Tyto soubory obvykle obsahují informace, jako je zeměpisná šířka, délka, nadmořská výška, časové razítko a další údaje související s vašimi aktivitami GPS.

Zde jsou některá běžná použití souborů .usr se zařízeními Lowrance GPS:

- **Trasové body:** Trasové body jsou konkrétní místa vyznačená na GPS, jako jsou orientační body, oblíbená rybářská místa nebo zajímavá místa. Tato místa můžete uložit jako soubory .usr a lze je importovat, exportovat nebo sdílet s ostatními uživateli Lowrance GPS.

- **Trasy:** Trasy představují zaznamenanou dráhu vašich pohybů GPS. Své záznamy trasy můžete uložit jako soubory .usr, což vám umožní později prohlížet a analyzovat své trasy nebo je sdílet s ostatními.

- **Trasy:** Trasy jsou předdefinované cesty, které můžete vytvořit a uložit do zařízení GPS. Tyto trasy lze také uložit jako soubory .usr pro budoucí použití nebo sdílení.

Ke správě souborů .usr na vašem zařízení Lowrance GPS obvykle používáte software jako Lowrance „Insight Planner“ nebo „Lowrance GPS Utility“ pro import, export a manipulaci s vašimi GPS daty.

## Formát souboru USR – Další informace

V zařízeních Lowrance iFinder GPS se soubory .usr vytvářejí a ukládají na paměťovou kartu MultiMediaCard (MMC) vloženou do zařízení. Tyto soubory obsahují uživatelská data, jako jsou trasové body, trasy a trasy.

Chcete-li přenést soubory .usr z MMC do počítače, postupujte takto:

- **Vyjměte MMC:** Opatrně vyjměte MultiMediaCard (MMC) ze zařízení Lowrance iFinder GPS.

- **Vložte MMC do počítače:** K vložení paměťové karty do slotu pro čtečku karet v počítači použijte vhodnou čtečku karet MMC.

- **Vyhledejte soubory .usr:** Jakmile počítač rozpozná MMC, měli byste mít přístup k souborům v něm uloženým. Hledejte soubory .usr, které obsahují vaše GPS data.

- **Konverze pomocí GPSBabel:** Chcete-li převést soubory .usr do jiného formátu GPS, můžete použít GPSBabel, což je bezplatný nástroj s otevřeným zdrojovým kódem pro práci s různými formáty souborů GPS. GPSBabel podporuje širokou škálu vstupních a výstupních formátů, což vám umožňuje převádět soubory .usr do formátů kompatibilních s jiným GPS softwarem nebo zařízeními.

GPSBabel si můžete stáhnout z oficiálních stránek (http://www.gpsbabel.org/) a nainstalovat do svého počítače. Po instalaci můžete k provedení převodu použít rozhraní příkazového řádku softwaru nebo grafické uživatelské rozhraní (je-li k dispozici).

Pokud například chcete převést soubory .usr do formátu GPX, můžete použít příkaz jako:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Výše uvedený příkaz dává pokyn GPSBabel, aby načetl vstupní soubor "input.usr" ve formátu Lowrance USR a zapsal výstupní soubor "output.gpx" ve formátu GPX.

- **Import/použití převedených souborů:** Po převodu budete mít data GPS v novém formátu (např. GPX), který můžete použít s jiným softwarem GPS nebo zařízeními, která tento formát podporují.

## Jak otevřít soubor USR?

Mezi programy, které otevírají nebo odkazují na soubory USR

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Reference
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)

