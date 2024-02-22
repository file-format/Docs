{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Přečtěte si o formátu souboru MCR a rozhraních API, která mohou vytvářet a otevírat soubory MCR.",
  "title": "MCR - Formát souboru regionu Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-csr"
}
},
  "lastmod": "2022-12-14"
}

## Co je soubor MCR?

Formát souboru Minecraft MCR je datový formát používaný Minecraftem k ukládání kousků terénu ze světa Minecraft. Je založen na formátu NBT (Named Binary Tag), který byl vyvinut vývojáři populárního open-source herního enginu Minecraft Forge. Typ souboru MCR byl představen na úplném začátku a později byl nahrazen [MCA file format](/game/mca/).

## Formát souboru MCR

Formát souboru MCR je strukturován jako řada pojmenovaných binárních značek, z nichž každá obsahuje specifický typ dat. Značka nejvyšší úrovně je značka Úroveň, která obsahuje všechna data pro jednu úroveň hry. V rámci tagu Level existuje několik dalších pojmenovaných tagů, které ukládají různé typy dat, jako je tag Data, který ukládá informace o herním světě, a tagy Entities a TileEntities, které ukládají data o herním světě. herní objekty a dlaždicové entity ve světě, resp.

## Co je uvnitř formátu souboru MCR?

Ve formátu souboru Minecraft MCR je region 32x32 bloková oblast herního světa. Formát MCR rozděluje herní svět na regiony, aby bylo možné efektivněji spravovat data a umožnit rychlejší načítání a ukládání herních úrovní. Každá oblast je uložena v samostatném souboru a formát souboru MCR používá systém souřadnic k identifikaci polohy každé oblasti v herním světě. Souřadnice oblasti jsou určeny blokovými souřadnicemi v levém dolním rohu oblasti. Například oblast se souřadnicemi (-1,0) by byla umístěna o jednu oblast vlevo a nula oblastí níže od počátku herního světa.

## Specifikace formátu souboru MCR

Specifikace formátu souboru MCR jsou veřejně dostupné. Specifikace formátu NBT, na kterém je formát MCR založen, jsou k dispozici na webu Minecraft Forge. Kromě toho [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) také obsahuje podrobné informace o formátu souboru MCR, včetně jeho struktury a různých typů dat, které podporuje.

### Komprimovaná data v souborech MCR

Formát souboru Minecraft MCR podporuje kompresi. Formát souboru MCR je založen na [NBT format](https://minecraft.fandom.com/wiki/NBT_format), který umožňuje ukládat data v komprimované podobě. To pomáhá zmenšit velikost souborů MCR a zefektivnit jejich přenos a ukládání. Toto je důležitá vlastnost formátu souboru MCR, protože umožňuje hráčům sdílet velká data terénu Minecraft World s ostatními.

## Reference

* [Světový editor pro Minecraft](https://www.mcedit.net/)

* [O Minecraftu](https://www.minecraft.net/)

* [Formát souboru regionu](https://minecraft.fandom.com/wiki/Region_file_format)

* [Formát NBT](https://minecraft.fandom.com/wiki/NBT_format)


