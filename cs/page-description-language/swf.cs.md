{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "soubor", "přípona", "formát", "formát videa", "Co je soubor SWF", "formát souboru swf", "přehrávač souborů swf","jak otevřít soubor swf"] ,
  "title" :"Soubor SWF - Formát souboru filmu Shockwave Flash",
  "description":"Zjistěte, co je soubor SWF, a rozhraní API, která mohou vytvořit a ukázat, jak soubor SWF otevřít.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor SWF?

Soubor SWF je soubor animace vytvořený pomocí Adobe Flash. K vytvoření animace může obsahovat různé typy prvků, jako je text, vektorové obrázky, rastrové obrázky, akční skripty, objekty, jako jsou kruhy, čáry, čtverce a obdélníky. Soubory SWF uspořádají tyto multimediální položky do snímků, které lze přehrávat v různých snímcích za sekundu (fps). SWF znamená krátký webový soubor, ale je také známo, že má formát Shockwave.

Aplikace, které mohly *otevřít soubory SWF**, zahrnovaly Adobe Flash Player (nyní ukončený) a Eltima Elmedia Player.

## Formát souboru SWF – Další informace

Soubory SWF byly používány k ukládání jako binární soubory na disk. Formát souboru SWF byl použit k vývoji animací a her, které bylo možné vložit do webových stránek a hrát je také samostatně. Podporoval také videa a zvuky, které daly vývojářům spoustu možností pro vytváření interaktivních multimediálních aplikací. Soubory SWF lze přehrávat ve webových prohlížečích s nainstalovaným Adobe Shockwave. Adobe Flash byl ukončen v prosinci 2020 kvůli jeho nedostatkům a bezpečnostním problémům.

## Stručná historie formátu souboru SWF

Formát souboru SWF byl původně navržen společností FutureWave Software, aby zobrazoval animace se záměrem běžet na softwaru přehrávače na jakémkoli systému s pomalejším síťovým připojením při zachování malé velikosti souboru. V prosinci 1996 Macromedia vlastnila FutureWave a převedla na Macromedia Flash 1.0.

V roce 2005 společnost Macromedia koupila společnost Adobe, která v roce 2008 oznámila SWF jako součást svého projektu s otevřeným zdrojovým kódem. Během téhož roku společnost Adobe uvolnila kód pro oblíbené světové webové nástroje, které jim umožnily procházet a indexovat soubory SWF. Protože se však zdá, že se soubory SWF stávají standardním formátem pro publikování obsahu Flash na internetu, byl SWF revidován tak, aby znamenal Small Web Format.

## Struktura souboru SWF

Cesta je základním grafickým prvkem v SWF, což je sekvence segmentů základních prvků, od jednoduchých čar až po Bézierovy křivky. Tyto jednoduché prvky také pomáhají vytvářet další další primitiva, jako jsou krychle, elipsy a dokonce i texty. Grafická primitiva v SWF mají podobnost s grafickými prvky jiných formátů, jako je SVG a MPEG-4 BIFS.

Formát umožňuje také zobrazení seznamů a opětovné použití/přejmenování již definovaných prvků. Binární formát streamu SWF lze přirovnat k atomům QuickTime, který je podobný, pokud jde o značku, velikost a užitečné zatížení. Binární formát streamu umožňuje starším hráčům přeskočit nepodporovaný obsah. Přestože původní verze SWF byly omezeny na vektorovou grafiku a obrázky, nové verze umožňují také audio a video obsah.

Ve verzi 11 bylo představeno nové, nízkoúrovňové 3D API přehrávače Flash Player s názvem „Stage3D“. Toto API bylo navrženo jako protějšek OpenGL nebo Direct3D. Stage3D definuje barvy v nízkoúrovňovém jazyce zvaném Adobe Graphics Assembly Language (AGAL). Následuje několik základních datových typů formátu souboru SWF.

### Souřadnice

Souřadnice XY ve formátu souboru SWF jsou uloženy jako celá čísla a měřeny v jednotce zvané twip. Twip se skládá z 1/20 logického pixelu. Logický pixel a pixel obrazovky jsou stejné, když je soubor přehráván bez 100% změny měřítka.

### Typy celých čísel a pořadí bajtů

Ve formátu souboru SWF jsou povoleny typy celých čísel se znaménkem a bez znaménka 8, 16, 32 a 64 bitů. Pořadí bajtů typu Little-endian se používá k uložení celočíselných hodnot. Ačkoli v rámci bajtů, bitové pořadí je uloženo v big-endianu. Všechny celočíselné hodnoty by měly být zarovnány po bytech. Celá čísla se znaménkem jsou reprezentována pomocí tradičních bitových vzorů komplementu 2.

### Čísla s pevnou čárkou

Formát souboru SWF podporuje dva typy čísel s pevnou řádovou čárkou, tj. 32 a 16 bitů.

### Čísla s plovoucí desetinnou čárkou

SWF 8 a novější verze používají tři typy čísel s pohyblivou řádovou čárkou (FLOAT, FLOAT 16, DOUBLE), které jsou kompatibilní se standardem IEEE 754 typů s pohyblivou řádovou čárkou.

### Kódovaná celá čísla

Jeden typ kódovaného celého čísla je podporován SWF 9 a novější s proměnným počtem bajtů.

## Reference

* [formát souboru SWF](https://en.wikipedia.org/wiki/Swf)

