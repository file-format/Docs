{
  "date" : "2021-03-08",
  "keywords" :[ "PML", "eReader", "extension", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a PML-fájlformátumról, a Palm jelölőnyelvről és a PML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"PML - Palm Markup Language File",
  "linktitle" : "PML",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Mi az a PML fájl?

A Palm Inc bevezette a PML fájlformátumot, amely a Palm Markup Language File rövidítése. Célja, hogy dokumentumokat hozzon létre az eReaderhez, amely egy, a táblagéphez hasonló e-könyv-olvasó eszköz. A PML-fájl egy [PDB](/hu/programming/pdb/) fájl elrendezését adja meg (különböző adatfájlokat tartalmaz), amelyet a Palm Devicen megjeleníthet.

## A PML-fájlok technikai részletei

A PML-fájlok szerkezete címkékből áll az e-könyv beállításához, beleértve a bekezdéseket, címsorokat, behúzásokat és hivatkozásokat. Lehetővé teszi az olyan formázási címkéket is, mint a félkövér, kis nagybetűs és felső index. A fejlesztők képeket is hozzáadhatnak az e-könyvekhez.

### Palm jelölőnyelv
A következő táblázat a PML parancsokat határozza meg:

|Parancs|Leírás|
---|---|
| \p | Új oldal |
| \x | Új fejezet; új oldaltörést is okoz. A fejezetcímet (és a stíluskódokat) a \x és \x | jelekkel zárja be
| \Xn | Új fejezet, n szint behúzással (n 0 és 4 között) a Fejezet párbeszédablakban; nem okoz oldaltörést. A fejezetcímet (és a stíluskódokat) \Xn és \Xn |
| \Cn="Fejezet címe" | Szúrja be a "Fejezet címét" a fejezetlistába n szinten (például \Xn). A szöveg nem jelenik meg az oldalon, és nem kényszeríti az oldaltörést. Ez néha hasznos lehet, ha például egy fejezetjelet szúr be a fejezet bevezetőjének elejére. |
| \c | Középre állítja ezt a szövegblokkot; zárja be a \c karakterrel a | sor elején
| \r | Jobb oldali sorkizárás szövegblokk; zárja be a \r karakterrel a sor elején |
| \i | Dőlt betűs blokk; zárja be a \i |
| \u | Aláhúzott blokk; zárja be a \u |
| \o | Overstrike blokk; zárja be a \o |
| \v | Láthatatlan szöveg; zárja be a \v karakterrel (megjegyzésekhez használható) |
| \t | Behúzás blokk. Kezdje a sor elején, zárja a \t karakterrel a sor végén |
| \T="50%" | Behúzza a képernyő szélességének megadott százalékát, ebben az esetben 50%-át. Ha az aktuális rajzpozíció már túl van a képernyő megadott helyén, akkor ezt a címkét a rendszer figyelmen kívül hagyja. |
| \w="50%" | A képernyő adott százalékos szélességének vízszintes szabályának beágyazása, ebben az esetben 50%. Ez a címke sortörést okoz előtte és utána. A szabály középen van. A százalékjel kötelező. |
| \n | Váltson a "normál" betűtípusra, amelyet a felhasználó határoz meg |
| \s | Váltás stdFont-ra; zárja be a \s karakterrel a normál betűtípushoz való visszatéréshez |
| \b | Váltás félkövér betűtípusra; zárja be a \b-vel a normál betűtípusra való visszatéréshez (elavult; használja helyette a \B-t) |
| \l | Váltás nagy betűtípusra; zárja be a \l karakterrel a normál betűtípushoz való visszatéréshez |
| \B | Szöveg megjelölése félkövérként. A \b címkével ellentétben a \B nem változtatja meg a betűtípust, így nagy, félkövér szöveget használhat. A \b és a \B nem keverhető ugyanabban a PML-fájlban. |
| \Sp | Szöveg megjelölése felső indexként. Nem keverhető más stílusokkal, például félkövér, dőlt stb. |
| \Sb | Szöveg megjelölése alsó indexként. Nem keverhető más stílusokkal, például félkövérrel, dőlt betűvel stb. Az aláírt szöveget \Sb karakterrel zárja be. |
| \k | A mellékelt szöveg kisbetűssé tétele; \k-val zárjuk. A \k címkékbe zárt karakterek (beleértve az ékezeteseket is) nagybetűsek, és kisebb pontmérettel jelennek meg, mint egy normál nagybetűs karakter. |
| \\ | Egyetlen fordított perjelet jelent |
| \aXXX | Szúrjon be olyan nem ASCII karaktert, amelynek Windows-1252 kódja decimális XXX. A részletekért lásd a PML karaktertáblázatot. |
| \UXXXX | Szúrjon be nem ASCII karaktert, amelynek Unicode kódja hexadecimális XXXX. A részletekért lásd a kiterjesztett PML karaktertáblázatot. |
| \m="képnév.png" | Illessze be a megnevezett képet. Tekintse meg a Képekkel foglalkozó részt alább. |
| \q="#linkanchor"Néhány szöveg\q | Hivatkozzon egy hivatkozási horgonyra, amely a dokumentum másik pontján található. A horgonyspecifikáció után és a \q előtti karakterlánc alá van húzva, vagy más módon hivatkozásként jelenik meg a dokumentum megtekintésekor. |
| \Q="linkanchor" | Adjon meg egy hivatkozási horgonyt a dokumentumban. |
| \- | Helyezzen be egy lágy kötőjelet. A lágy kötőjel csak akkor jelenik meg, ha egy szót egy soron át kell törni. |
| \Fn="lábjegyzet1"1\Fn | Kapcsolja össze az „1”-et egy lábjegyzettel, amelynek neve lábjegyzet1, és a PML-dokumentum végén található. Lásd alább a lábjegyzetekről és az oldalsávokról szóló részt. |
| \Sd="oldalsáv1"Oldalsáv\Sd | Kapcsolja össze az "Oldalsáv" szöveget egy oldalsávval, amelynek neve sidebar1, és a PML-dokumentum végén van címkézve. Lásd alább a lábjegyzetekről és az oldalsávokról szóló részt. |
| \I | Jelölje meg referencia indexelemként. Az indexelemet (és a stíluskódokat) \I és \I.| zárja be
 


## Hivatkozások

* [Palm Markup Language – MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader – a MobileRead által](https://en.wikipedia.org/wiki/E-reader)

