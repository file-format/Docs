{
  "date" : "2019-10-11",
  "keywords" :[ "vrml fájl", "vrml fájlformátum", "mi az a vrml fájl", "fájl", "vrml példa", "vrml fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VRML fájlformátum",
  "description":"További információ a VRML fájlformátumról és az API-król, amelyek megnyithatnak és létrehozhatnak VRML fájlokat.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a VRML fájl?
A Virtual Reality Modeling Language (VRML) egy olyan fájlformátum, amely interaktív [3D](/hu/3d/) világobjektumokat ábrázol a világhálón (www). Használatát összetett jelenetek, például illusztrációk, definíciók és virtuális valóság prezentációk háromdimenziós ábrázolásában használják. A formátumot az [X3D](/hu/3d/x3d/) váltotta fel. Számos 3D modellező alkalmazás képes objektumokat és jeleneteket VRML formátumban menteni.

## VRML fájlformátum

A VRML egy szöveges fájlformátum, amely olyan információkat határoz meg, mint a 3D sokszög csúcsai és élei, valamint olyan információkat, mint a felület színe, UV-leképezett textúrák, fényesség, átlátszóság és így tovább. Képes statikus és animált objektumokat ábrázolni amellett, hogy hiperhivatkozásokat tartalmazhat más médiákra, például hangokra, filmekre és képekre. Ez lehetővé teszi a linkelt elemek megnyitását, amikor a felhasználó ezekre az objektumokra kattint.

A szokásos terminológiában használt TVRML-fájlokat "világoknak" nevezik, és .wrl kiterjesztéssel rendelkeznek. Ezeknek a fájloknak a szöveges jellege lehetővé teszi a fájlméret csökkentését tömörítési formátumok, például a gzip használatával, így kedvezőbbek az interneten történő gyors átvitelhez. A [VRML v 2.0] fájlformátum-specifikációi (http://gun.teipir.gr/VRML-amgem/spec/index.html) a fejlesztői referenciaként szolgálnak az ilyen fájlok olvasásához/írásához kompatibilis alkalmazások létrehozásához.

## Tervezési kritérium ##

A VRML célja és kialakítása a következő követelmények körül forog.

* **Authorability** – Lehetővé teszi alkalmazásgenerátorok és szerkesztők fejlesztését, valamint adatok importálását más ipari formátumokból
* **Teljesség** – Minden, a megvalósításhoz szükséges információt megad, és egy teljes szolgáltatáskészlettel foglalkozik a széles körű iparági elfogadottság érdekében
* **Összeállíthatóság** – A VRML elemeinek kombinált használatának lehetősége, és ezáltal lehetővé teszi az újrafelhasználhatóságot.
* **Bővíthetőség** – Új elemek hozzáadásának lehetősége.
* **Megvalósíthatóság** - Sokféle rendszeren implementálható.
* **Többfelhasználós potenciál** – Nem zárhatja ki a többfelhasználós környezetek megvalósítását.
* **Ortogonalitás** - A VRML elemeinek függetlennek kell lenniük egymástól, vagy a függőségeknek strukturáltnak és jól meghatározottaknak kell lenniük.
* **Teljesítmény** – Az elemeket úgy kell megtervezni, hogy a hangsúlyt az interaktív teljesítményre helyezzék különféle számítási platformokon.
* **Skálázhatóság** - A VRML elemeit végtelenül nagy kompozíciókhoz kell tervezni.
* **Szabványos gyakorlat** - Csak azokat az elemeket szabad szabványosítani, amelyek tükrözik a meglévő gyakorlatot, amelyek szükségesek a meglévő gyakorlat támogatásához, vagy amelyek szükségesek a javasolt szabványok támogatásához.
* **Jól felépített** - Egy elemnek jól definiált interfésszel és egyszerűen megfogalmazott, feltétel nélküli céllal kell rendelkeznie. Kerülni kell a többcélú elemeket és a mellékhatásokat.

## Hivatkozások ##

* [VRML – a Wikipédia által](https://en.wikipedia.org/wiki/VRML)
* [VRML v 2.0 fájlformátum specifikációi](http://gun.teipir.gr/VRML-amgem/spec/index.html)

