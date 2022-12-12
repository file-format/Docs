{
  "date" : "2019-10-11",
  "keywords" :[ "psb fájl", "psb fájlformátum", "mi az a psb fájl", "fájl", "psb példa", "psb fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB – Photoshop Big Image File Format",
  "description":"További információ a PSB fájlformátumról és az API-król, amelyek PSB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PSB fájl?
Az Adobe Photoshop két formátumban menti a fájlokat. A 30 000 x 30 000 képpont méretű fájlok mentése PSD kiterjesztéssel, a PSD-nél nagyobb fájlok pedig 300 000 x 300 000 képpontig a „Photoshop Big” néven ismert PSB kiterjesztéssel. Pontosabban, a PSB-fájlok mérete elérheti a 4 EB-t (több mint 4,2 milliárd GB-ot), a képek magassága és szélessége akár 300 000 pixel is lehet. A PSD-k viszont legfeljebb 2 GB-osak lehetnek, a képméret pedig 30 000 pixel.

A PSB a Photoshop nagyformátumú formátumaként is ismert, és támogatja a Photoshop összes funkcióját, például a rétegeket, effektusokat és szűrőket. A Photoshop képes konvertálni a PSB fájlokat [PSD](/hu/image/psd/), [JPG](/hu/image/jpeg/) formátumba. , [PNG](/hu/image/png/), [EPS](/hu/page-description-language/eps/), [GIF](/hu/image/gif/) és más formátumok is. A Photoshop nagyméretű dokumentumformátuma akkor érhető el, ha a Photoshop beállításai párbeszédpanel fájlkezelő paneljének funkciója engedélyezve van.

## Fájlformátum információ ##

A Photoshop fájlformátum öt nagy részre van osztva, sok hosszjelölővel a szakaszok közötti mozgáshoz.

|Fájlformátum
---|
|Fájlfejléc
|Szín mód adatai
| Képforrások
|Réteg- és maszkinformáció
|(((
Képadatok
)))

### Fájlfejléc ###

A fájlfejléc fix hosszúságú, 26 bájt, és a kép alapvető tulajdonságait tartalmazza.

BYTE aláírás [4] – '8BPS'-nek felel meg.

WORD-verzió [2] – Verziószám, PSD # 1, PSB # 2.

BYTE Fenntartva [6] – Fenntartva és mindig nulla.

WORD Channels [2] – A kép színcsatornáinak száma, beleértve az alfa csatornákat. Értéke 1 és 56 között van.

HOSSZÚ sorok [4] – A kép magassága pixelben, 1-30 000 PSD, 1-300 000 PSB.

HOSSZÚ oszlopok [4] – A kép szélessége pixelben, 1-30 000 PSD, 1-300 000 PSB.

WORD Depth [2] – A bitek száma csatornánként. A támogatott értékek: 1,8,16 és 32.

WORD Mode [2] – A fájl színmódja.

#### Mód leírása ####


|Mód|Leírás
---|---|
|0|Bittérkép (monokróm)
|1|Szürkeárnyalatos
|2|Indexelt
|3|RGB
|4|CMYK
|7|Többcsatornás
|8|Duotone (féltónus)
|9|Labor

### Színmód adatok ###

A fájlfejléc szakasz után a színmód adatok szakasz következik. A blokk egy LONG számmal kezdődik, amely megadja a blokk hosszát bájtokban. A színmód adatok szerkezete a következő:

4 bájt – A következő színadatok hossza.

Változó – Színadatok

Ha a mód mező értéke a fejrészben nem Indexed Color vagy dutone, akkor a blokk hossza 0 lesz, és a hosszmező után nem lesz adat.

Az indexelt színes képek esetében a hossza 768 bájt, amely 256 színpalettát tartalmaz. Duotónus esetén az adatok képernyőparamétereket és egyéb kapcsolódó információkat tartalmaznak.

### Képforrások ###

A színmód adatszakasz után a harmadik blokk a képi erőforrás rész. Az első négy bájt egy LONG szám, amely meghatározza a blokk hosszát, majd egy sor erőforrás blokk következik. A kép-erőforrás blokk felépítése a következő:

BYTE típus [4] – Aláírás '8BIM'

WORD ID [2] – Képforrás-azonosító. Van egy lista az erőforrás-azonosítókról, amely a hivatkozási hivatkozásról látható.

BYTE Név [Változó] – Név: Pascal karakterlánc páros hosszúsággal. ***

LONG Size [4] – A következő erőforrásadatok tényleges mérete.

BYTE adatok [Változó} – Erőforrás adatok. Párnázott, hogy egyenletes legyen.

Az alábbiakban röviden ismertetünk néhány forrásformátumot:

**Rács és segédvonalak erőforrásformátuma:** A rács és segédvonalak információi az erőforrásblokkban tárolódnak. Ezek az erőforrásblokkok 16 bájtos rácsot és útmutató fejlécet tartalmaznak, amelyet 5 bájtos útmutató információs blokkok követnek.

**Miniatűr erőforrás formátuma:** A bélyegképek információi a kép erőforrás blokkjában tárolódnak az előnézeti megjelenítéshez, amely 28 bájtos fejlécből és RGB JFIF miniatűrből áll.

**Színmintavevők erőforrásformátuma:** A színmintavevők információi egy 8 bájtos fejléccel rendelkező képerőforrás-blokkban tárolódnak, amelyet egy változó hosszúságú színmintavevő információs blokk követ.

### Réteg- és maszkinformáció ###

A negyedik blokk egy réteg és maszk információs blokk, és a rétegekről és a maszkokról tartalmaz információkat. A rendszer először a réteginformációkat tárolja, majd a maszkinformációkat.

**Réteginformáció:** A fóliainformáció LONG értékkel kezdődik, amely a réteginformáció hosszát mutatja. Ezt követően van egy WORD értékszám, amely a követendő rétegrekordok számát mutatja.

[8] – a rétegek hossza

[2] – Rétegszám

[Változó] – Információ az egyes rétegekről.

[Változó] – Csatorna képadatai.** **

**Maszk információ:** A maszk szerkezete a következő formátumú:


|Adatstruktúra|Mező neve| Leírás
---|---|---|
|SZÓ| Overlay Color Space| (Nincs dokumentálva)
|BYTE[8]| Színes összetevők| 4x2 bájtos színösszetevők
|SZÓ| Opacitás| 0#átlátszó, 1#átlátszatlan
|BYTE| Kedves| 0#fordított, 1#védett, 128#tárolt érték használata
|BYTE| párnázat| nullára állítva

### Képadatok ###

Az utolsó rész a kép pixel adatait tartalmazza. A képadatok sorozatok sorozataként kerülnek tárolásra síkban, azaz először az összes piros adatot, majd az összes zöld adatot stb. A WORD az egyes sorok elején mutatja az egyes pásztázási sorokhoz tartozó méretet bájtokban.

[2] – Tömörítési módszer:

[Változó] – A képadatok síkbeli sorrendben, pl. RRRR, GGGG, BBBB stb.

Tömörítési módszerek:

0 – Raw Képadatok

1 – RLE tömörített

2 – Zip előrejelzés nélkül

3 – Cipzár előrejelzéssel

## Hivatkozási szám

* [PSB fájlformátum – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

