{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PS fájlformátum",
  "description":"További információ a PS-fájlformátumról és az API-król, amelyek PS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a .PS fájl? ##

A PostScript (PS) egy általános célú oldalleíró nyelv, amelyet az asztali számítógépes és elektronikus publikálásban használnak. A PostScript (PS) fő célja a kétdimenziós grafikai tervezés megkönnyítése. A legtöbb nyelv külön fordítási szakaszt igényel a kód végrehajtása előtt, míg a Post Script (PS) formátum támogatja a futásidejű, egyenes értelmezést. Korai változata az Adobe képalkotó modell szabályait követve határozza meg a grafikus formákat, a különböző szövegmegjelenítéseket és a modellezett képeket nyomtatott vagy megjelenített oldalakon. A PS egyik programja képes dokumentumleírást kommunikálni a kompozíció és a nyomtatási rendszer között, így az eszköz független és magas szinten marad. Ezen túlmenően ez a program képes szabályozni a szöveg és a grafika megjelenését a kijelzőn.

A PostScript oldalleírás az eszköz PostScript értelmezőjének segítségével renderelhető, megjeleníthető nyomtatón és egyéb kimeneti eszközön. Mivel a karakterek, grafikus alakzatok és képek nyomtatására vonatkozó parancsokat az értelmező hajtja végre, az adott eszközön a magas szintű PostScript leírás alacsony szintű raszteres adatformátummá alakul. Általában a különféle alkalmazások, például az illusztrátorok, a dokumentum-összeállítási rendszerek és a számítógéppel segített tervezés (CAD) automatizáltak PostScript oldalleírások generálására. Általában a programozóknak PostScript programokat kell írniuk az új alkalmazások létrehozásakor. A programozó azonban kihasználhatja a PostScript nyelv azon képességeit, amelyek egyetlen alkalmazásban sem érhetők el, ha PS-programot ír az adott speciális helyzetre.

## Rövid története ##

A PostScript nyelv fogalmát először John Warnock vezette be. 1966-ban a New York-i kikötő egyik projektjén dolgozott. Megpróbált egy tolmácsot fejleszteni egy nagy, háromdimenziós grafikához a projekt adatbázisához. Ezen grafikák feldolgozásához John Warnock megalkotta a Design System nyelvet. Eközben a Xerox PARC szabványos eszközt keresett az oldalképek meghatározásához első lézernyomtatójához. Bár Bob Sproull és William Newman 1975-76-ban kifejlesztette a Press formátumot (adatformátumot) a lézernyomtatók meghajtására, mégis szükség volt egy nyelvre a nagyobb rugalmasság érdekében. 1978-ban Warnock csatlakozott Martin Newellhez a Xerox PARC-ban, és átírta az értelmező nyelvet, a JaM-et, amelyet később kibővítettek és kiterjesztettek az Interpress nyelvre. Warnock 1982 decemberében alapította meg az Adobe Systems-t Chuck Geschke, Doug Brotz, Ed Taft és Bill Paxton társaságában. Elkezdtek dolgozni egy egyszerűbb nyelven, a PostScript néven, hasonló az Interpresshez, amely 1984-ben jelent meg kereskedelmi forgalomban. Steve Jobs az Apple-től meglátogatta őket, és azt tanácsolta nekik, hogy adaptálják a PostScript-et a lézernyomtatók meghajtására.

1985 márciusában az első beágyazott PostScript értelmezővel rendelkező nyomtató az Apple LaserWriter volt, amely forradalmasította az asztali publikálást (DTP). A műszaki megalapozottság és a széles körű elérhetőség a PostScript-et választotta az asztali és elektronikus publikálás nyelvévé. 1990-ben a PostScript nyelv tolmácsa a lézernyomtatók elengedhetetlen része volt.

## Főbb jellemzői ##

A PostScript nyelv interaktív grafikák és oldalleírások kezelésére szolgáló képességei a következő tulajdonságokkal rendelkeznek:

**Alakzatok:** Tetszőleges természetűek, állhatnak egyenes vonalakból, görbékből, négyzetekből és köbös görbékből, amelyek lehetnek önjárók és szétválaszthatók (szakaszokban és lyukakban).

**Festési operátorok:** lehetővé teszik bármilyen vastagságú, színű, kitöltött alakzat körvonalát, vagy lehetővé teszik az alakzat kivágásként történő megrajzolását bármely más grafika kivágása érdekében.

**Színek:** olyan sokszínűek, mint a szürkeárnyalatos, az RGB, a CMYK és a CIE. Különböző tulajdonságként speciális színtípusokat modelleznek: direkt színek, színleképezés, egyenletes árnyékolás és ismétlődő minták.

**Szöveg:** teljesen integrálva a grafikával. Ezenkívül az Adobe képalkotó modell lehetővé teszi a szöveges karakterek grafikus alakzatokként történő megjelenítését, amelyeket bármely normál grafikus operátor kezelhet.

**Mintaképek**: eredeti forrásokból (beszkennelt fényképek) vagy szintetikusan előállíthatók. A PostScript nyelv változatos módokat kínál a képek bármilyen felbontású és színmodell szerinti újragenerálására egy kimeneti eszközön.

Egy általános célú programozási nyelv kihasználhatja a PostScript nyelv grafikus képességeit, ha Ps-t ágyaz be a keretébe. A primitív adattípusok, például számok, karakterek, tömbök és karakterláncok; vezérlőprimitívek, például hurkok, eljárások és feltételes feltételek; és néhány nem szokványos szolgáltatás, például szótárak vannak megadva a nyelvben. Ezek a funkciók lehetővé teszik a programozóknak, hogy parancsokat írjanak magasabb szintű műveletek meghívásához. Ezek a magas szintű műveletek kielégítik a komplex alkalmazások igényeit. Az ilyen gyakorlat kompaktabb és hatékonyabb, mint az alapvető műveletek rögzített halmaza.

A PostScript nyelven írt programok ASCII forrásszöveg formájában állíthatók elő, kommunikálhatók és értelmezhetők. A teljes nyelv definiálható nyomtatható karakterek és szóközök formájában. Ez az ábrázolás támogatja a programozókat a nyelv egyszerű létrehozásában, kezelésében és megértésében. Ezen túlmenően a fájlok tárolása és átvitele a különböző számítógépek és operációs rendszerek között kényelmes volt a gépfüggetlenség révén.

A nyelv binárisan kódolt formái akkor lehetségesek, ha a program garantált egy teljesen átlátható kommunikációs útvonalat a PostScript interpreter felé. Az Adobe javasolja a PS-programok ASCII-megjelenítésének szigorú koherenciáját a dokumentumcseréhez vagy az archív tároláshoz.

## Verziók ##

A PS(.ps) a PostScript-dokumentumok fájlkiterjesztése. Az Egyesült Királyság Nemzeti Archívuma a PostScript-fájl öt kronológiai változatát sorolja be a DSC-verzióban: 1.0, 2.0, 2.1, 3.0, 3.1. Mindegyik verzió fontos strukturáló megjegyzéseket határoz meg. Az Encapsulated PostScript File (EPS) a PostScript fájl egy speciális altípusa, amely a nyelvet használja a téglalap alakú grafika meghatározásához. A PostScript Language Reference Manual a következőképpen írja le az EPS-t: "Az Encapsulated PostScript (EPS) fájl egy PostScript program, amely legfeljebb egyetlen oldalt ír le olyan formában, amelyet más alkalmazások importálhatnak, hogy beágyazzanak egy dokumentumba." A PostScript dokumentumfájl EPS-fájlt is tartalmazhat. A PostScript egy további használatát Display PostScript (DPS) néven említik. A DPS a PostScript képalkotási modellt és nyelvet használó grafikus motoron keresztül állít elő a képernyőn megjelenő grafikákat.

## Hivatkozások ##

* [PostScript formátumcsalád](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

