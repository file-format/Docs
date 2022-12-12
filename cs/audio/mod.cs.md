{
  "date" : "2021-08-04",
  "keywords" :[ "mod", "mp3", "soubor", "rozšíření", "formát", "co je formát souboru mod", "hudba", "formát souboru mod", "mod vs MP3", "specifikace formátu souboru mod"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru MOD a rozhraních API, která mohou vytvářet, převádět a otevírat soubory MOD.",
  "title" :"MOD - soubor hudebního modulu",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-04"
}

## Co je soubor MOD?
Soubor s příponou .mod je soubor hudebního modulu vytvořený pomocí standardního formátu hudebního modulu, který je založen na **formátu modulu Amiga** vyvinutém Karstenem Obarskim a vydaným se softwarem **Ultimate Soundtracker** pro Commodore. Amiga systém. Podobně jako soubor [MIDI](/cs/audio/mid/) se skládá z notových vzorů a zvukových vzorků, které představují různé nástroje, které jsou přehrávány podle not. Soubory MOD se používají zejména ve videohrách jako hudba na pozadí a v subkultuře počítačového umění **demoscene**.

## Formát souboru MOD

MOD je počítačový formát souborů, jehož základní funkcí je reprezentovat hudbu a byl to první modulový souborový formát. Soubory MOD používají příponu souboru .mod, kromě **Amigy**, která čte záhlaví souboru, aby určila typ souboru, takže se nespoléhá na přípony souborů. Soubor MOD se skládá ze sady různých nástrojů ve formě samplů, několika vzorů určujících, jak a kdy se vzorky mají hrát, a seznamu vzorů, které se mají hrát v jakém pořadí.

### Specifikace formátu souboru MOD

Vzor souboru MOD je ve skutečnosti navržen v uživatelském rozhraní sekvenceru jako tabulka s jedním sloupcem na kanál, takže tato tabulka má čtyři sloupce (jeden pro každý kanál Amiga hardwaru. Každý sloupec má 64 řádků).

Buňka v tabulce může způsobit, že na kanálu jejího sloupce dojde k jedné z následujících akcí, když nastane čas jejího řádku:

- Spustit nástroj hrát novou notu v tomto kanálu při dané hlasitosti, případně s aplikovaným speciálním efektem
- Změňte hlasitost nebo speciální efekt aplikovaný na aktuální notu
- Změna toku vzoru; skok na konkrétní skladbu nebo pozici patternu nebo smyčku uvnitř patternu
- Nedělat nic; jakákoli existující nota hrající na tomto kanálu bude i nadále hrát

Nástroj je jeden vzorek spolu s volitelnou specifikací, která část vzorku může být opakována, aby se udržela pevná nota.

### Načasování
Minimální časový rámec byl 0,02 sekundy v původním souboru MOD nebo interval „vertikálního zatemnění“ (VSync), protože původní software používal časování VSync monitoru běžícího na 50 Hz (pro PAL) nebo 60 Hz (pro NTSC). pro načasování.

## Reference

* [MOD (formát souboru) – podle Wikipedie](https://en.wikipedia.org/wiki/MOD_(formát_souboru))

