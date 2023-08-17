{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Microsoft Access Reports File",
  "keywords" :[ "mar", "mar file", "mar file format", "what is access report", "access report", "microsoft access report"],
  "description":"További információ az Acess Report (MAR) fájlformátumról, amelyet a Microsoft Access szoftver a Microsoft Access Report parancsikon vagy hivatkozás létrehozására használ.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Mi az a hozzáférési jelentés (MAR fájl)? ##
A Microsoft Access által a jelentés parancsikonjaként létrehozott fájl .mar kiterjesztéssel kerül mentésre. A **Microsoft Access jelentés** lehetőséget kínál a Microsoft Access adatbázisban lévő információk formázására, megtekintésére és összegzésére. Ezek a jelentések lehetővé teszik, hogy adatait precíz és informatív elrendezésben formázza a képernyőn való megtekintéshez vagy a nyomtatáshoz. A jelentés csak a statikus adatokat jeleníti meg, ami azt jelenti, hogy az Access jelentés megtekintésekor nem tudjuk módosítani a táblázatokban szereplő adatokat. A jelentés megnyitásakor a legfrissebb adatokat jeleníti meg.

## Microsoft Access Report (MAR) fájlformátum

A MAR fájlformátumot a Microsoft Access szoftver használja arra, hogy parancsikont vagy hivatkozást hozzon létre a Microsoft Access Reporthoz, amely egy adatbázis-objektum, amely akkor válik hasznossá, ha az adatbázisban lévő információkat az alábbi célokra kell bemutatnia:

- Az adatok összefoglalásának megjelenítése.
- Pillanatképek archiválása az adatokról.
- Részletek megjelenítése az egyes rekordokról.
- Hozzon létre címkéket.

## A hozzáférési jelentés részei
Az Access jelentés kialakítása különböző szakaszokra van felosztva, amelyek a Tervezés nézetben tekinthetők meg. Az alábbi táblázat bemutatja, hogy az egyes szakaszok hogyan működnek, és hogyan segíthetnek jelentéseket készíteni.
| szakasz | Hogyan jelenik meg a szakasz nyomtatáskor | Hol használható a szakasz |
---------|----|------|
| Jelentés fejléce | A riport elején. | Használja a jelentés fejlécét olyan információkhoz, amelyek általában megjelenhetnek a fedőlapon, például logó, cím vagy dátum. Ha a jelentés fejlécében elhelyez egy számított vezérlőelemet, amely az Összesítési függvényt használja, akkor a kiszámított összeg a teljes jelentésre vonatkozik. A jelentés fejléce az oldalfejléc elé kerül nyomtatásra. |
| Oldal fejléce | Minden oldal tetején. | Használjon oldalfejlécet a jelentés címének megismétléséhez minden oldalon. |
| Csoportfejléc | Minden új rekordcsoport elején. | Használja a csoport fejlécét a csoport nevének kinyomtatásához. Például egy termék szerint csoportosított jelentésben használja a csoport fejlécet a termék nevének kinyomtatásához. Ha olyan számított vezérlőelemet helyez el a csoport fejlécében, amely a Sum aggregate függvényt használja, az összeg az aktuális csoportra vonatkozik. Egy jelentésben több csoportfejléc-szakasz is szerepelhet, attól függően, hogy hány csoportosítási szintet adott hozzá. A csoportfejlécek és láblécek létrehozásával kapcsolatos további információkért tekintse meg a Csoportosítás, rendezés vagy összesítés hozzáadása című részt. |
| Részlet | A rekordforrás minden sorában egyszer jelenik meg. | Itt helyezheti el a jelentés fő részét alkotó vezérlőket. |
| Csoport lábléce | Minden rekordcsoport végén. | Használjon csoport láblécet egy csoport összefoglaló információinak kinyomtatásához. Egy jelentésben több csoportláb-szakasz is szerepelhet, attól függően, hogy hány csoportosítási szintet adott hozzá. |
| Oldal lábléce | Minden oldal végén. | Az oldalláb segítségével oldalszámokat vagy oldalankénti információkat nyomtathat. |
| Jelentés lábléce | A beszámoló végén. Megjegyzés: Tervező nézetben a jelentés lábléce az oldal lábléce alatt jelenik meg. Azonban minden más nézetben (például elrendezés nézetben, vagy amikor a jelentést kinyomtatják vagy megtekintik) a jelentés lábléce az oldal lábléce felett jelenik meg, közvetlenül az utolsó csoport lábléce vagy részletsora után az utolsó oldalon. | A jelentés láblécével kinyomtathatja a jelentés összesítését vagy egyéb összefoglaló információkat a teljes jelentésre vonatkozóan. |






## Referenciák ##

- [Az Access jelentéseinek bemutatása](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Jelentések tervezése az Accessben](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

