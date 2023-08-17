{
  "date" : "2019-10-11",
  "keywords" :[ ".swf", "SWF", "Apple swift", "file", "extension", "file format", "apple swift bemutató", "programozási útmutató" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SWIFT - Apple Source Code File",
  "description":"További információ a SWIFT fájlformátumról és az API-król, amelyek SWIFT-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "SWIFT",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az a Swift fájl?

A .swift kiterjesztésű fájl az Apple által bevezetett SWIFT programozási nyelvre vonatkozik, amely szoftveralkalmazások és alkalmazások írására szolgál macOS, iOS, tvOS és egyéb rendszerekre. A SWIFT előtt az Objective-C volt az elsődleges programozási nyelv az alkalmazások írásához. Használható az Xcode-al, amely egy teljes fejlesztői eszközkészlet Mac, iPhone, iPad, Apple Watch és Apple TV alkalmazások létrehozásához. A SWIFT erősebb, interaktívabb, kifejezőbb, és tervezésénél fogva nagyobb biztonságot kínál anélkül, hogy a teljesítményt veszélyeztetné. A Swift fájlok az Apple Xcode mellett bármilyen szövegszerkesztőben megnyithatók szerkesztés céljából. Támogatja az Apple operációs rendszereit, a Linuxot, a Windowst és az Androidot.

## Rövid története

* A fejlesztést 2010 közepén indította el Chris Lattner az Apple más programozóinak közreműködésével
* Az első hivatalos SWIFT-ben írt alkalmazás 2014. június 2-án jelent meg az Apple WorldWide Developer Conference (WWDC) rendezvényen, és a nyelv béta verziója megjelent a regisztrált Apple fejlesztők számára.
* A Swift 1.0 2014. szeptember 9-én jelent meg az iOS Xcode-jával
* A Swift 1.1 2014. október 22-én jelent meg az Xcode 6.1 megjelenésével
* A Swift 1.2 2015. április 8-án jelent meg az Xcode 6.3-mal együtt
* A Swift 2.0-t a 2015-ös WWDC-n jelentették be, és 2015. szeptember 21-én elérhetővé vált alkalmazások közzétételére az App Store-ban.
* A Swift 3.0 2016. szeptember 13-án jelent meg.
* A Swift 4.0 2017. szeptember 19-én jelent meg.
* A Swift 4.1 2018. március 29-én jelent meg.
* A Swift nyelv 2015. december 3-án nyílt forráskódú, a támogató könyvtárakkal, a hibakeresővel és a csomagkezelővel együtt az Apache 2.0 licenc alatt. A projektet a [Swift.org](https://swift.org/), forráskódja pedig a [GitHub](https://github.com/apple/swift) webhelyen tárolja.
* A 2019-es WWDC során az Apple bejelentette a SwiftUI keretrendszert a felhasználói felület szerkezetének kialakításához az összes Apple platformon

## Swift fájlformátum – További információ

A Swift fájlok egyszerű szöveges fájlok, amelyek bármely szövegszerkesztővel megnyithatók. A swift fájlok megnyitásához és szerkesztéséhez használt elsődleges szövegszerkesztő az Apple Xcode. A Swift számos része ismeri a C és Objective-C használatával történő alkalmazásfejlesztést. A Swift dokumentációja részletes [alkalmazásfejlesztési útmutatót](https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics/) tartalmaz a Swift használatával történő kódíráshoz.

## Swift nyelvi funkciók

A Swift a következő jellemzők alapján különbözik meg a többi programnyelvtől.

„Modern” – A megnevezett paraméterek tiszta szintaxisban vannak kifejezve, amely még könnyebben olvashatóvá és karbantarthatóvá teszi a Swift API-it. Még jobb, ha nem is kell pontosvesszőt beírni.

"Biztonság" – A változókat mindig használat előtt inicializálják, a tömbök és egész számok túlcsordulását ellenőrzik, a memória automatikusan felügyelődik, és a memória kizárólagos hozzáférésének érvényesítése megóv számos programozási hibától.

"Gyors és hatékony" – A hihetetlenül nagy teljesítményű LLVM fordítótechnológia segítségével a Swift kódot optimalizált natív kóddá alakítják, amely a legtöbbet hozza ki a modern hardverből.

"Forrás és bináris kompatibilitás" – A Swift korábbi verziójával fejlesztett alkalmazások kompatibilisek az új kiadásokkal, és a forráskódot nem kell újrafordítani. A Swift 5 elindításával a Swift-könyvtárak minden operációs rendszer-kiadásban szerepelnek a jövőben. Ezzel elkerülhető a Swift-könyvtárak felvétele a jelenlegi és jövőbeli operációs rendszer-kiadásokat célzó alkalmazásokba.

"Nyílt forráskódú" – A Swift nyílt forráskódú, több száz Swift-közösség-tag hozzájárulásával. Erős hibakövető, fórumok és rendszeres fejlesztési buildek támogatják, amelyek mindenki számára nyilvánosan elérhetők.

## Hivatkozások
* [Swift – GitHub](https://github.com/apple/swift)
* [Swift – Wikipédia](https://en.wikipedia.org/wiki/Swift_(programming_language))

