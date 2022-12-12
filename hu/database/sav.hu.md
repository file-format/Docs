{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "kiterjesztés", "sav file", "sav file format", "Database File Type", "Database File Format", "What is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a SAV fájlformátumról és az API-król, amelyek SAV-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"SAV - SPSS adatfájl",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Mi az a SAV fájl?
A SAV fájl a Társadalomtudományi Statisztikai Csomag (SPSS) által létrehozott adatfájl, amelyet piackutatók, egészségügyi kutatók, felmérést végző cégek, kormányzat, oktatáskutatók, marketingszervezetek és adatbányászok széles körben használnak statisztikai elemzésekhez. A szabadalmaztatott bináris formátumban mentett SAV, amely egy adatkészletből és egy szótárból áll, amely az adatkészletet reprezentálja, sorokban és oszlopokban menti az adatokat.

## SAV fájlformátum
A SAV fájlformátum viszonylag stabil lett, de nem mondhatjuk statikusnak. A visszafelé és előre kompatibilitás opcionálisan elérhető, ha szükséges, de nincs megfelelően karbantartva. A SAV-fájlban lévő adatok a következő szakaszokba vannak sorolva:

### Fájlfejléc
176 bájtból áll. Az első 4 bájt a **$FL2** vagy **$FL3** karakterláncot jelzi a fájlhoz használt karakterkódolásban. Az utolsó három bájt azt jelenti, hogy a fájlban lévő adatok a **ZLIB** használatával vannak tömörítve. A következő 60 bájtos karakterlánc a **@(#) SPSS DATA FILE** karakterlánccal kezdődik, és meghatározza a fájlt létrehozó operációs rendszert és SPSS-verziót is. A fejléc ezután hat számjegyű mezőkkel folytatódik, amelyek a megfigyelésenkénti változók számát és a tömörítéshez szükséges számjegykódot tartalmazzák, és a létrehozás dátumát és időpontját jelző karakteradatokkal, valamint egy fájlcímkével zárul.
### Változóleíró rekordok
A rekord rögzített mezősorozatot tartalmaz, amely osztályozza a változó típusát és nevét, valamint az SPSS által használt formázási információkat. Minden változórekord opcionálisan tartalmazhat egy legfeljebb 120 karakter hosszúságú változócímkét és legfeljebb három hiányzó érték specifikációt.
### Értékcímkék
Az értékcímkék nem kötelezőek, és rekordpárokban vannak tárolva a 3. és 4. egész számmal. Az első rekord, amely a 3. címke, mezőpárokból álló sorozatot tartalmaz, mindegyik pár egy értéket és a hozzá tartozó értékcímkét tartalmaz. A második rekord, amely a 4-es címke, azt jelzi, hogy az értékek/címkék halmaza mely változókra vonatkozik.
### Dokumentumok
Egy vagy több rekord egész szám címkével 6. Opcionális dokumentáció. 80 karakteres sorokat tartalmaz.
### Kiterjesztési rekordok
Egy vagy több rekord egész szám 7-es címkével. A kiterjesztésrekordok olyan információkat nyújtanak, amelyek biztonságosan figyelmen kívül hagyhatók, de sok esetben megőrizhetők, lehetővé téve az újabb szoftverekkel írt fájlok visszamenőleges kompatibilitásának megőrzését. A kiterjesztésrekordok egész számú altípus-címkékkel rendelkeznek.
### Szótár terminátor
Csak a 999-es egész szám címkével rögzítsen. Ez elválasztja a szótárt az adatmegfigyelésektől.
### Adatmegfigyelések
Úgy tekintjük, hogy az adatok megfigyelési sorrendben vannak, pl. minden változó érték az első megfigyelésnél, majd az összes érték a második megfigyelésnél stb. Az adatrekord formátuma a fájlfejléc rekordban lévő tömörítési kódtól függően változik. A .sav fájl adatrésze kicsomagolható:
- **0-s kód**: bájtkóddal tömörítve
- **1-es kód**: ZLIB tömörítéssel tömörítve
 







## Hivatkozások ##

* [SPSS rendszeradat-fájlformátumcsalád (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

