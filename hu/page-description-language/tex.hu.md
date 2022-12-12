{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TEX fájlformátum",
  "description":"További információ a TEX fájlformátumról és az API-król, amelyek TEX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a TEX fájl? ##

A **TeX** egy olyan nyelv, amely programozást, valamint jelölési funkciókat tartalmaz, amelyeket dokumentumok szedésére használnak. Donald Knuth, a Stanford Egyetem munkatársa ennek a találékony szedőrendszernek a megalkotója. Világszerte a TeX a szerzők és kiadók legjobb választása a kiváló minőségű műszaki dokumentumok elkészítéséhez. A TeX kiemelkedő munkát végez az összetett matematikai kifejezések formázásában. A TeX egy kiváló minőségű fotószedővel együtt versenyez a legjobb hagyományos szedőrendszerek eredményeivel. Ezért a legklasszabb digitális tipográfiai rendszernek tekinthető.

A TeX bemeneti fájlok ASCII-kódon alapulnak, így lehetővé teszik a kéziratok megosztását az írók, kiadói vezetők és kritikusok között. Számítástechnikai környezetek széles választéka, szinte minden modern platform és sok régebbi platform támogatja a TeX-et. Ezenkívül a TeX egy ingyenes szoftver, amely a fogyasztók széles köre számára elérhető. Sok UNIX-telepítés a UNIX troff-ot és a TeX-et egyaránt használja formázási rendszerként különböző célokra. A többi szedési feladatot a LaTeX, a ConTeXt és más makrócsomagok formájában rendkívüli módon hajtják végre.

## Rövid története ##

A TeX-et Donald Knuth tervezte és írta 1978-ban. Guy Steele, a Massachusetts Institute of Technology-tól felülvizsgálta a TeX bemenetét/kimenetét, hogy az Inkompatibilis operációs rendszer, például az Időmegosztási Rendszer (ITS) alatt fusson. A TeX első verzióját a Stanford WAITS operációs rendszere alatt fejlesztették ki programozási nyelven (SAIL), és tesztelték PDP-10-en. Knuth bevezette az írástudó programozás ötletét a fejlett verziókhoz. A Literate programozás egy módja annak, hogy lefordítható forráskódot és betűkészletet (TeX-ben) állítsunk elő kereszthivatkozásos dokumentációhoz az eredeti fájl felhasználásával. A TeX ezen fejlett verzióinak fejlesztéséhez használt nyelvet WEB-nek hívják, amely DEC PDP-10 Pascal programok keveréke a hordozhatóság biztosítása érdekében.

A TeX átdolgozott új verziója 1982-ben jelent meg, és a TeX82 nevet kapta. A fő változás az eredeti elválasztási algoritmus lecserélése a Frank Liang által újonnan írt algoritmusra. A különböző platformokon való hordozhatóság biztosítása érdekében a TeX82 a lebegőpontos használata helyett fixpontos aritmetikát és egy valódi, teljes programozási nyelvet használ. 1989-ben megjelent a TeX és a Metafont új verziója. Tehát a TeX 3.0-s verziója 8 bites bevitelt tesz lehetővé, így 256 különböző karaktert tesz lehetővé a szövegben. A 3-as verzió után a frissítéseket a tizedesjegy végéhez egy extra számjegy hozzáadásával jelöljük, pl. a TeX jelenlegi verziója 3.14159265. Ez a verzió legutóbbi frissítése: 2014. 12. 1..

## TeX bemenet ##

A TEX-be bemeneti fájl elkészíthető egy szövegszerkesztővel közönséges szöveg használatával. A tipikus szövegszerkesztővel ellentétben ez a bemeneti fájl nem engedélyez minden láthatatlan vezérlőkaraktert. Egy fájl beágyazható egy másik fájlba, amely makródefiníciókat és kiegészítő definíciókat tartalmaz, amelyek javítják a TeX képességeit. Ha a TeX-telepítéshez makrófájlok is tartoznak, a TeX helyi információi bemutatják a makrófájlok használatát. A TeX szabványos formája makrók és más, sima TEX néven ismert definíciók kombinációját integrálja.

Az összes karakter és szimbólum méretének pontos ismerete alapján kiszámítja a betűk soronkénti és a sorok oldalankénti optimális elrendezését. A dokumentum feldolgozása során egy .dvi fájl készül, ahol a „dvi” az „eszközfüggetlen” kifejezést jelenti. Eszköz-illesztőprogramok szükségesek a dvi kiterjesztésű dokumentum nyomtatásához vagy előnézetéhez. Manapság a dvi generálást megkerüli egy általánosan használt pdf-TeX. A TeX telepítésen belül nem áll rendelkezésre előzetes betűtípus-ismeret, ezért a helyi TeX környezet részét képező külső fontfájlokat használják a dokumentumok információinak megszerzésére.

## Szedési rendszer ##

Körülbelül 300 primitív (parancs) érthető meg az alap TeX rendszerrel. A primitívek alacsony szintű parancsok, ezért egy gyakori felhasználó ritkán használja őket közvetlenül, és a legtöbb funkciót formátumfájlok hajtják végre. Ezek a formátumú fájlok a TeX előre betöltött memóriaképei, amelyeket nagy makrógyűjtemények betöltése követ. A nyelv eredeti alapértelmezett formátuma, azaz a sima TeX körülbelül 600 parancsot ad hozzá.

A kapcsos zárójelekkel csoportosított fordított perjel a TeX parancsok kezdetét jelzi. Mivel a TeX makró és token alapú nyelv, a TeX szinte minden szintaktikai jellemzője megváltoztatható futás közben, beleértve a felhasználó által meghatározottakat is, kivéve a nem bővíthető tokeneket, amelyek ezután végrehajtásra kerülnek. Maga a bővítés gyakorlatilag problémamentes. Néhány parancsnak olyan argumentum után kell jönnie, amely segít megmagyarázni egy parancs funkcióját. Például a \vskip parancs arra utasítja a TEX-et, hogy ugorjon le/fel az oldalon, majd egy argumentum következik, amely meghatározza, hogy mennyi helyet kell kihagyni.

## Verziók ##

A LaTeX a leggyakrabban használt formátum, amelyet eredetileg Leslie Lamport fejlesztett ki. A LaTeX különböző dokumentumstílusokat integrál fájlokhoz, levelekhez, könyvekhez és diákhoz, valamint hivatkozásokat és automatikus számozást kínál a különböző szakaszokhoz és matematikai kifejezésekhez. Az AMS-TeX egy másik népszerű formátum, amelyet az American Mathematical Society fejlesztett ki.

Az AMS-TeX sokkal felhasználóbarátabb parancsokat kínál, amelyeket a naplók újradefiniálhatnak, hogy illeszkedjenek a helyi stílusukhoz. A LaTeX kihasználhatja az AMS-TeX előnyeit az AMS "csomagok" használatával, amelyeket ezután AMS-LaTeX-nek neveznek. A ConTeXt egy másik Hans Hagen által írt formátum, amelyet főleg asztali publikáláshoz használnak.

A TeX szoftver számos olyan funkciót kínál, amelyek létrehozása idején nem, vagy gyengébb minőségűek voltak más szedőrendszerekben. Ennek a nyelvnek néhány innovatív tulajdonsága érdekes algoritmusokon alapul, amelyek Knuth tanítványainak téziseiből származnak. Míg más szedőprogramok most a TeX hasznos funkcióit építik be programjaikba.

## Hivatkozások ##

* [TeX betűszedő rendszer](https://en.wikipedia.org/wiki/TeX)

