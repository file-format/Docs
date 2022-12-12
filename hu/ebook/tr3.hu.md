{
  "date" : "2021-04-10",
  "keywords" :[ "TR3", "File", "Extension", "File Format", "eBook", "TomeRaider", "Yadabyte" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a TR3 fájlformátumról és az API-król, amelyek TR3 fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"TR3 - TomeRaider 3 eBook File",
  "linktitle" : "TR3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-04-10"
}

## Mi az a TR3 fájl? ##

A TR3 fájl egy TomeRaider 3 eBook, amely támogatja a gyors keresést és tömörítést. Ez megfelelően működhet a TomeRaiderrel kapcsolatos programon keresztül. A Yadabyte ennek a szoftvernek a fejlesztője, egy brit szoftver- és webfejlesztő cég, amelynek székhelye az Egyesült Királyságban található. A TomeRaider eBook olvasó alkalmazás használható a TR3 fájlok megfelelő működéséhez és tartalmának kezeléséhez. Ez a kapcsolódó e-könyv-olvasó telepíthető olyan számítógépekre, amelyek Microsoft Windows-alapú rendszerekkel és számos átvihető kütyüvel futnak. A TR3 fájl az olyan operációs rendszerekben használt eBook Files csoportjába tartozik, mint a Windows 10, Windows 7, Windows 8 / 8.1, Windows Vista, Windows XP.

A TR3-specifikus **HTML-címkék** a következők:

|Címke|Leírás|
---|---|
|\<new> |TomeRaider fájlok szöveges fájlokból történő létrehozásához csak az Új címke szükséges.<new> címke határozza meg az oldalak elejét.|
|\<CATDEF> ... \</CATDEF> |meghatározza a kategória nevét|
|\<META> ... \</META> |egy címke, amely a fájlformátumban használt összes metaadat meghatározására szolgál. Ez a címke számos paramétert tartalmaz.|
|\<EXPMSG> |Ez a címke szabályozza a fájl lejártakor megjelenő üzenetet. Amikor egy felhasználó megpróbál egy oldalt megtekinteni, miután a fájl lejárt, a tényleges oldal szövege helyett a lejárati üzenet jelenik meg.|
|\<DIEMSG> |Ez a címke hasonló az EXPMSG-hez. Üzenet megjelenítésére szolgál, amikor a fájl elhal.|
|\<ENGMSG> |Ez a címke a titkosított oldalak esetén megjelenő üzenet létrehozására szolgál. Az üzenet jelenik meg az oldal szövege helyett, ha a felhasználó megpróbál megnyitni egy titkosított oldalt a zárolás feloldása előtt.|
|\<expmsg> ,\<diemsg> és \<encmsg> |Figyelmen kívül hagyva az oldal szövegében. Ezeket a fájl fejléc részében kell elhelyezni az első előtt<new> tag.|
|\<SELECTION> . \</ SELECTION> |A Query támogatására szolgál. Ennek a címkének az első előtt kell lennie<new> címke. Összeállítja a kiválasztási adatokat a felhasználó lekérdezéséhez.|
|\<catset> . \</catset> | Kategórianevek hozzárendelésére szolgál minden tantárgyhoz.|


## Problémák a TR3 fájl megnyitásakor ##

Az alábbiakban felsorolunk néhány gyakori problémát, amelyek előfordulhatnak, és a fájlformátum hibás működését okozhatják:

* Sérült fájl
* Fertőzött fájl vírus miatt
* Helytelen hivatkozások a TR3 fájlra az archívum elérésében
* Nincs hozzáférési jog a rendszerben a fájlok megnyitásához
* Elavult meghajtó a rendszerben
* A TR3 jelentésének eltávolítása a Windows archívumából
* A fejlesztővel való kapcsolatfelvétel jobb megoldás lehet a jobb teljesítmény érdekében

