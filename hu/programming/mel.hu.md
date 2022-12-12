{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded Language", "file", "extension", "file format", "Maya 3D", "Programozási útmutató" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL – Maya Embedded Language File Format",
  "description":"További információ a MEL fájlformátumról és az API-król, amelyek MEL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Mi az a MEL fájl?

A .mel (Maya Embedded Language) kiterjesztésű fájl egy szkriptnyelv, amelyet az Autodesk Maya használ grafikus felületek létrehozására. Lehetővé teszi a grafikus elemek létrehozásának automatizálását a Maya grafikus felületén kívül végrehajtható szkriptek használatával. A MEL lehetővé teszi grafikus felületek létrehozását programozás tanulása nélkül. Ez makrók és egyéni műveletek létrehozásával érhető el, amelyek felgyorsítják az ismétlődő feladatokat. Ezekkel az eljárásokkal és szkriptekkel egyéni modellezést, animációkat, dinamikát és feladatmegjelenítést hozhat létre. Az Autodesk Maya 2020 segítségével megnyitható és megtekinthető az EML-fájlok tartalma.

## MEL fájlformátum - További információ

A programozói [referencia-kézikönyv](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) elérhető a fejlesztők számára a Maya dokumentációs részében. A MEL az UINX-hez hasonló shell script parancsokon alapul, hogy elérje a dolgokat. A parancsfájl alapú parancsok irrelevánssá teszik a hagyományos és objektum orientált programozás (OOP) szempontjából, így nem használnak adatstruktúrákat, nem hívnak függvényeket vagy nem használnak OOP-t, mint más nyelvekben.

A MEL néhány kulcsfontosságú pontja a következő.

"Megjegyzések" - A MEL-ben minden utasításnak pontosvesszővel (;) kell végződnie, még a blokk végén is.

"Értékek visszaadása" – Egy értéket visszaadó kifejezés megadása nem írja ki automatikusan az értéket a MEL-ben. Ehelyett hibát okoz.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
"Parancsok a létrehozáshoz, szerkesztéshez és törléshez" - Ugyanez a parancs használható dolgok létrehozására, szerkesztésére vagy információk lekérdezésére a meglévő dolgokról. A jelző azonban szabályozza, hogy a parancs mit tegyen (létrehozzon, szerkesszen vagy lekérdezzen).

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` – A függvény szintaxisa automatikusan visszaad egy értéket. Ha a parancs szintaxisával visszatérési értéket szeretne kapni, a parancsot idézőjelek közé kell tennie.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Hivatkozások

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

