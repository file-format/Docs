{
"dátum":"2023-01-04",
   "keywords":[
"cs",
"cs fájl",
"cs cleo custom script",
"cs fájl megnyitása",
"fájl",
"cs fájlkiterjesztés",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"CS fájlformátum - CLEO egyéni szkript",
   "description":"További információ a CS CLEO egyéni szkriptformátumról és az API-król, amelyek CS-fájlokat hozhatnak létre és nyithatnak meg.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo",
         "parent":"game"
}
},
"lastmod":"2023-01-04"
}

## Mi az a CS fájl?

A .CS-fájl a CLEO-val összefüggésben (a CLEO Library rövidítése) általában a Grand Theft Auto (GTA) videojáték-sorozatban használt egyéni szkriptfájlra utal. A CLEO egy népszerű modding keretrendszer, amely lehetővé teszi a játékosoknak, hogy egyedi szkripteket hozzanak létre és adjanak hozzá a GTA-játékokhoz, lehetővé téve számukra a játékmenet módosítását, új funkciók hozzáadását és az általános játékélmény javítását.

## A CS fájl áttekintése

Íme egy alapvető áttekintés arról, hogy mit tartalmazhat egy .cs fájl a CLEO-ban:

1. **Script Code**: A .cs fájl CLEO szkriptnyelven írt szkriptkódot tartalmaz. Ez a szkriptnyelv a CLEO-ra jellemző, és az egyéni szkriptek játékon belüli viselkedésének meghatározására szolgál. A kód szövegszerkesztővel írható, és általában egy meghatározott szintaxist követ.
    









2. **Módosítások**: A CLEO szkriptek különféle módosításokat hajthatnak végre a játékon, például megváltoztathatják a játékon belüli objektumok viselkedését, egyedi küldetéseket hozhatnak létre, új járműveket, fegyvereket adhatnak hozzá és így tovább. A lehetőségek szélesek, és a forgatókönyv szerzőjének kreativitásától és programozási készségétől függenek.
    









3. **Triggerek**: A CLEO szkriptek gyakran tartalmaznak triggereket, amelyek meghatározzák, hogy mikor és hogyan fusson az egyéni szkript. Ezek a triggerek alapulhatnak a játékon belüli eseményeken, játékos akciókon vagy meghatározott feltételeken.
    









4. **Változók és függvények**: A CLEO szkriptek változókat használhatnak adatok tárolására és kezelésére, valamint függvényeket kód beágyazására és újrafelhasználására. Ezek a változók és függvények a szkript viselkedésének szabályozására szolgálnak.

## Példa CS fájlra

Íme egy egyszerű példa egy CLEO .cs szkriptre, amely megváltoztatja az időjárást a játékban:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## CLEO Könyvtár

A **CLEO Library**, amelyet gyakran egyszerűen csak "CLEO"-ként emlegetnek, egy népszerű és hatékony modding keretrendszer a Grand Theft Auto (GTA) videojáték-sorozathoz. Lehetővé teszi a játékosok és a modderek számára, hogy egyedi szkripteket hozzanak létre és adjanak hozzá a GTA-játékokhoz, lehetővé téve számukra a játékmenet módosítását, új funkciók hozzáadását és az általános játékélmény javítását. A CLEO különösen jól ismert rugalmasságáról és egyszerű használatáról a GTA modding közösségben.

Íme a CLEO Library néhány kulcsfontosságú funkciója és szempontja:

1. **Szkriptnyelv**: A CLEO bemutatja szkriptnyelvét, amely kifejezetten a módosítási keretrendszerre vonatkozik. A szkriptnyelvet úgy tervezték meg, hogy viszonylag könnyen érthető legyen, és így a kezdő és a tapasztalt modderek számára is elérhető legyen.
    









2. **Egyéni szkriptek**: A CLEO-val egyéni szkripteket hozhat létre, amelyek a játékvilágon belüli funkciók széles skáláját képesek ellátni. Ezek a szkriptek megváltoztathatják a játékon belüli viselkedést, új küldetéseket adhatnak, új járműveket vagy fegyvereket mutathatnak be, megváltoztathatják a játék fizikáját és még sok mást.
    









3. **Triggerek és események**: A CLEO szkripteket különböző játékon belüli események, játékos akciók vagy meghatározott feltételek válthatják ki. Ez lehetővé teszi a modderek számára, hogy dinamikus és interaktív tartalmat hozzanak létre a játékon belül.
    









4. **Több GTA-verzió támogatása**: A CLEO-nak vannak különböző GTA-játékokhoz szabott verziói, köztük a GTA III, a GTA Vice City, a GTA San Andreas, a GTA IV és mások. Ez azt jelenti, hogy a modderek létrehozhatják és megoszthatják egyéni szkripteiket a különböző GTA-címekhez.

## A CLEO Library által használt fájlformátumok

A Grand Theft Auto (GTA) játékokhoz készült CLEO modding során általában többféle fájlformátumot használnak a modok létrehozására és telepítésére. Ezek a fájlformátumok különféle célokat szolgálnak a tényleges szkriptek tárolásától a további erőforrások, például textúrák, modellek vagy hang tárolásáig. Íme néhány a CLEO moddingban használt kulcsfontosságú fájlformátumok:

1. **.cs (Custom Script)**: A CLEO .cs fájlok CLEO szkriptnyelven írt egyedi szkriptfájlok. Ezek a fájlok olyan kódot tartalmaznak, amely meghatározza a mod viselkedését és működését. A .cs fájlok a CLEO modding magját képezik, és a játék futtatja őket egyéni funkciók megvalósítása érdekében.
    









2. **.csa (Custom Script Archive)**: A .csa fájlok olyan archívumok, amelyek több .cs script fájlt is tárolhatnak. Gyakran használják a kapcsolódó szkriptek összecsomagolására a könnyebb telepítés és kezelés érdekében.
    









3. **.fxt (szövegfájlok)**: Az .fxt fájlok olyan szövegfájlok, amelyek segítségével lokalizálhatók vagy szövegfordítások biztosíthatók a CLEO modokhoz. A játékban megjeleníthető szöveges karakterláncokat tartalmaznak, így a modok különböző nyelveken érhetők el a játékosok számára.
    









4. **[.bmp](/hu/image/bmp/), [.png](/hu/image/png/), [.jpg](/hu/image/jpeg/) (Képformátumok)**: Ezek a képformátumok textúrák és képek tárolására használják a modokhoz. Használhatók egyedi skinekhez, járműtextúrákhoz, HUD elemekhez és még sok máshoz. Játéktól függően különböző képformátumok lehetnek előnyben.

## CS fájl - Mivel nyitható meg?

A CLEO .cs (Custom Script) fájlok megnyitásához és tartalmának megtekintéséhez használhat egy tetszőleges szövegszerkesztőt vagy kódszerkesztőt. A gyakori választások a következők:

- **Jegyzettömb**: Egyszerű szövegszerkesztő, amely előre telepítve van a Windows rendszerrel.
- **Jegyzettömb++**: A funkciókban gazdagabb szövegszerkesztő kódoláshoz és szkriptekhez.
- **Visual Studio Code**: Népszerű, ingyenes és rendkívül bővíthető kódszerkesztő.
- **Sublime Text**: Egy másik kódszerkesztő, amely gyorsaságáról és sokoldalúságáról ismert.
- **Atom**: A GitHub által fejlesztett nyílt forráskódú szerkesztő.

## Egyéb CS fájlok

Íme más fájltípusok, amelyek a **.cs** fájlkiterjesztést használják.

**Adatfájlok és játék**
- [CS - ColorSchemer Studio színséma](/hu/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/hu/game/cs-cleo/)

**Programozás**
- [CS - CSharp Code File](/hu/programming/cs/)

## Hivatkozások
* [CLEO könyvtár](https://cleo.li/)

