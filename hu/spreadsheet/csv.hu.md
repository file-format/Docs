{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "file", "extension", "file format", "Comma Separated Values", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a CSV-fájlformátumról és a CSV-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"CSV fájlformátum",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Mi az a CSV-fájl?

A .csv (vesszővel elválasztott értékek) kiterjesztésű fájlok egyszerű szöveges fájlok, amelyek vesszővel elválasztott értékekkel rendelkező adatrekordokat tartalmaznak. A CSV-fájl minden sora egy új rekord a fájlban található rekordkészletből. Az ilyen fájlok akkor jönnek létre, amikor az egyik tárolórendszerről a másikra adatátvitelt terveznek. Mivel minden alkalmazás képes felismerni a vesszővel elválasztott rekordokat, az ilyen adatfájlok importálása az adatbázisba nagyon kényelmes. Szinte minden táblázatkezelő alkalmazás, például a Microsoft Excel vagy az OpenOffice Calc, különösebb erőfeszítés nélkül képes importálni a CSV-fájlt. Az ilyen fájlokból importált adatok egy táblázat celláiba vannak rendezve a felhasználó számára történő megjelenítés céljából.

## Rövid története ##

Az alábbiakban néhány gyors tényt olvashat a CSV fájlformátum eredetéről és történetéről.

* 1972 - Az IBM Fortran (H szintű kiterjesztett) fordító támogatja őket OS/360 alatt

* 1978 - A listavezérelt bemenetet/kimenetet a FORTRAN 77 támogatja, amely vesszőket és szóközöket használt az elválasztókhoz

* 2005 – A CSV-t szabványosították az [RFC4180](https://tools.ietf.org/html/rfc4180) MIME-tartalomtípussal.

* 2013 - Az RFC4180 hiányosságait a W3C ajánlás kezelte

* 2015 – A W3C elkészítette a CSV-metaadat-szabványokra vonatkozó ajánlások első vázlatait, amelyek 2015 decemberében ajánlásként indultak

## CSV-fájlok konvertálása ##

A CSV-fájlok több különböző fájlformátumba konvertálhatók az ezeket a fájlokat megnyitó alkalmazásokkal. Például a Microsoft Excel képes adatokat importálni CSV fájlformátumból, és menteni XLS, [XLSX](/hu/spreadsheet/xlsx/), [PDF](/hu/pdf/), [TXT](/hu/word-processing/txt/) formátumba. , XML és [HTML](/hu/web/html/) fájlformátumok. Hasonlóképpen, más asztali és online szolgáltatások is lehetővé teszik a CSV-fájlok exportálását HTML-be, ODS-be és [RTF](/hu/word-processing/rtf/).

## CSV fájlformátum ##

A CSV-fájlformátum köztudottan az [RFC4180](https://tools.ietf.org/html/rfc4180) alatt van megadva. Minden fájlt CSV-kompatibilisnek határoz meg, ha:

* Minden rekord külön sorban található, sortöréssel (CRLF) határolva. Például:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* A fájl utolsó rekordja tartalmazhat záró sortörést, de lehet, hogy nem. Például:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* Előfordulhat, hogy a fájl első soraként egy opcionális fejlécsor jelenik meg a normál rekordsorokkal megegyező formátumban. Ez a fejléc a fájl mezőinek megfelelő neveket tartalmaz, és ugyanannyi mezőt kell tartalmaznia, mint a fájl többi részének rekordjainak (a fejlécsor meglétét vagy hiányát az opcionális "fejléc" paraméterrel kell jelezni MIME típus). Például:
* mező_neve, mező_neve, mező_neve CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* A fejlécen és minden rekordon belül egy vagy több mező lehet, vesszővel elválasztva. Minden sornak ugyanannyi mezőt kell tartalmaznia a fájlban. A szóközök egy mező részének tekintendők, és nem szabad figyelmen kívül hagyni őket. A rekord utolsó mezőjét nem követheti vessző. Például:
* aaa,bbb,ccc
* Az egyes mezőket idézőjelek közé lehet tenni, de lehet, hogy nem (egyes programok, például a Microsoft Excel azonban egyáltalán nem használnak idézőjeleket). Ha a mezőket nem zárja kettős idézőjel, akkor előfordulhat, hogy dupla idézőjelek nem jelennek meg a mezőkben. Például:\
* "aaa", "bbb", "ccc" CRLF
* zzz,yyy,xxx
* A sortörést (CRLF), dupla idézőjeleket és vesszőket tartalmazó mezőket dupla idézőjelbe kell zárni. Például:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Ha a mezők közé dupla idézőjeleket használunk, akkor a mezőn belül megjelenő dupla idézőjelből egy másik kettős idézőjelet kell megelőzni. Például:
* "aaa","b""bb","ccc"

A modern használat fényében azonban az elválasztójel nem korlátozódik csak vesszőre, hanem lehet pontosvessző, tabulátor vagy szóköz is. Az olyan alkalmazások, mint a Microsoft Excel, lehetőséget biztosítanak a határoló karakter megadására a rekordok CSV-fájlból történő importálásához.

## Hivatkozások

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV – Wikipédia](https://en.wikipedia.org/wiki/Comma-separated_values)

