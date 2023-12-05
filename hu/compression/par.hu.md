{
"dátum":"2023-07-18",
   "keywords":[
"PAR",
"PAR fájl",
"hogyan lehet megnyitni egy par fájlt",
"fájl",
"PAR fájl kiterjesztése",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"PAR Fájlformátum - Parchive Index File",
   "description":"További információ a PAR formátumról és az API-król, amelyek PAR fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
}
},
"lastmod":"2023-07-18"
}

## Mi az a PAR fájl?

A Parchive (PAR) archívumokban a .par fájl olyan indexfájlra utal, amely paritáskötetek vagy paritásblokkok csoportját tartalmazza. Ezt az indexfájlt hibaészlelési és helyreállítási célokra használják, ha egy vagy több fájl elveszik vagy megsérül az archívumban.

Az archívum archívuma általában az eredeti adatfájlokból és a megfelelő paritáskötetekből áll. A paritáskötetek Reed-Solomon hibajavító algoritmusok segítségével jönnek létre. Ezek a paritáskötetek redundáns információkat tartalmaznak, amelyek felhasználhatók az eredeti adatfájlok visszaállítására.

A .par fájl, más néven paritáskötet-készlet, információkat tartalmaz a paritáskötetek szerkezetéről és elhelyezkedéséről az archívumban. Indexként vagy térképként szolgál a helyreállítási folyamathoz. A .par fájl használatával a speciális PAR-szoftver meg tudja határozni, hogy mely paritáskötetekre van szükség, és hogyan kell ezeket használni a hiányzó vagy sérült fájlok helyreállításához.

Ha az archívumban egy vagy több fájl elérhetetlenné válik vagy megsérül, a .par fájl a rendelkezésre álló paritáskötetekkel együtt használható az elveszett adatok helyreállítására. A PAR szoftver beolvassa a .par fájlt, azonosítja a hiányzó vagy sérült fájlokat, és a paritáskötetek segítségével rekonstruálja azokat.

## PAR fájl - Mivel nyitható meg egy PAR fájl?

A .par fájlok megnyitásához és használatához speciális PAR szoftverre lesz szüksége. Íme néhány népszerű szoftverbeállítás, amely képes kezelni a .par fájlokat:

- **QuickPar:** A QuickPar egy széles körben használt PAR szoftver Windowshoz. Lehetővé teszi PAR fájlok létrehozását, ellenőrzését és javítását. Megnyithat egy .par fájlt a QuickPar alkalmazásban, hogy ellenőrizze annak integritását, vagy felhasználhatja a sérült vagy hiányzó fájlok javítására az archívumban.

- **MultiPar:** A MultiPar egy másik népszerű PAR szoftver, amely elérhető a Windows számára. Támogatja a PAR és a PAR2 fájlformátumokat, és fejlett funkciókat kínál az archívumok létrehozásához, ellenőrzéséhez és javításához. A MultiPar meg tudja nyitni a .par fájlokat, és hibaészlelési és helyreállítási műveleteket hajt végre a megadott paritáskötetek alapján.

- **MacPAR deLuxe:** A MacPAR deLuxe egy kifejezetten macOS-hez tervezett PAR szoftver. Támogatja a PAR és PAR2 fájlformátumokat, és hasonló funkciókat kínál, mint a QuickPar és a MultiPar. A MacPAR deLuxe képes megnyitni a .par fájlokat, és segítséget nyújtani az archívumok ellenőrzésében és a sérült vagy hiányzó fájlok helyreállításában.

## PAR fájlformátum - További információ

A PAR-fájlformátum, amelyet általában Parchive-nak neveznek, egy speciális fájlformátum, amelyet a paritásadatok létrehozására, valamint a fájlarchívumokban történő hibaészlelésre és -helyreállításra használnak. A PAR fájlformátum általában három típusból áll: PAR, PAR2 és PAR3.

- **PAR:** Az eredeti PAR fájlformátumot, más néven PAR1-et, a Parchive projekt fejlesztette ki. Tartalmazza az eredeti adatfájlokból generált paritásadatokat. A PAR fájlok a hibaészlelés és -helyreállítás alapvető szintjét biztosítják, de a hibajavítási képességek korlátai vannak.

- **PAR2:** A PAR2 a PAR fájlformátum továbbfejlesztett változata. Fejlettebb hibajavítási lehetőségeket és továbbfejlesztett helyreállítási funkciókat kínál. A PAR2 fájlokat általában olyan paritásadatok létrehozására használják, amelyek helyreállíthatják az elveszett vagy sérült fájlokat az archívumban. A PAR2 fájlok jobb védelmet nyújtanak az adatsérülés ellen, és széles körben használják fájlarchiválási célokra.

- **PAR3:** A PAR3 a PAR fájlformátum legújabb verziója, és további fejlesztéseket biztosít a hibajavítás és helyreállítás terén. A PAR2-hez képest még magasabb szintű redundanciát és hibajavítási képességeket kínál. A PAR3 fájlokat úgy tervezték, hogy erőteljesebb védelmet és helyreállítási lehetőségeket biztosítsanak az archívumokban tárolt adatok számára.

Mind a PAR2, mind a PAR3 fájlformátumot széles körben támogatja a PAR szoftver, és lehetővé teszi az archívumban lévő fájlok integritásának ellenőrzését, valamint az elveszett vagy sérült adatok helyreállítását. A PAR és PAR2 fájlok továbbra is általánosan használtak, míg a PAR3 fájlok fokozatosan elterjednek a továbbfejlesztett hibajavító képességeik miatt.

## Hivatkozások
* [Archívum](https://en.wikipedia.org/wiki/Parchive)

