{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL fájl – Android interfész definíciós nyelvi fájl",
  "description":"Ismerje meg, mi az AIDL fájlformátum, példákkal és API-kkal, amelyek AIDL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Mi az AIDL fájl?

Az AIDL (Android Interface Definition Language) fájl lehetővé teszi az Android fejlesztők számára, hogy kommunikációt létesítsenek a különböző alkalmazások között. A programozási interfész alapján mind az ügyfél, mind a szolgáltatás megállapodik abban, hogy az interprocess communication (IPC) segítségével kommunikálnak. Az AIDL fájl [Java](/hu/programming/java/) forráskódot tartalmaz ezen interfészek és az alkalmazások közötti kommunikációra vonatkozó szerződések meghatározásához.

Az AIDL fájlokat megnyithatja a Google Android Studióval vagy bármilyen szövegszerkesztővel, például a Microsoft Notepad és a Notepad++ segítségével.

## AIDL fájlformátum - További információ

Az AIDL olyan szöveges fájlok, amelyek az alkalmazások közötti kommunikáció interfészeit tartalmazzák. Az Android OS nem teszi lehetővé, hogy egy folyamat hozzáférjen egy másik folyamat memóriájához. Ez arra készteti a folyamatokat, hogy az objektumokat primitívekre bontsák, hogy megértsék az alapul szolgáló operációs rendszert, és létrehozzák a kommunikációs struktúrák folyamatát a fejlesztők számára.

### Milyen adattípusokat támogat az AIDL?

Az AIDL alapértelmezés szerint a következő adattípusokat támogatja.

* Minden primitív típus a Java programozási nyelvben (például int, long, char, boolean és így tovább)
* Húr
* CharSequence
* Lista
* Térkép

## AIDL fájl példa

Az alábbiakban egy példa az AIDL fájlra.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Hivatkozások

* [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

