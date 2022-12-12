{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC File Extension - Mi az INC fájl?",
  "description":"További információ az INC-ről Include fájlformátum és API-k, amelyek INC-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## Mi az INC fájl?

Az INC-fájl egy olyan belefoglaló fájl, amelyet a szoftverprogram forráskódja használ a fejlécinformációk hivatkozására. Hasonló a [.h fájlformátumhoz](/hu/programming/h/), és deklarációkat, függvényeket, fejléceket vagy makrókat tartalmaz, amelyeket a forráskódfájlok, például a C++ újra felhasználhatnak. Az INC fájlokat számos programozási nyelv használja, mint például a C, [C++](/hu/programing/cpp/), Pascal, [PHP](/hu/programing/php/) és [Java](/hu/programing/java/). A szövegszerkesztők, például a Microsoft Notepad, a Notepad++ és a TextEdit használhatók az INC fájlok megnyitásához.

## INC fájlformátum - További információ

Egy INC-fájl egyszerű szöveges fájlként kerül mentésre az összes deklarációval a deklaráció szintaxisának megfelelően. Egy INC-fájl más INC-fájlokra is hivatkozhat. A létrehozást követően az INC-fájl a projekt részévé válik, és forrásfájlokból, például C++-ból hivatkozhat rá. Több forrásfájl is hivatkozhat rá a párhuzamosságok elkerülése érdekében.

## INC fájl tartalma

Az INC fájlok a következő információkat tartalmazhatják.

**`Változók`** – Objektumorientált programozás (OOP) esetén az osztályfejléc fájl tartalmazza az összes olyan osztályszintű változó definícióját, amely elérhető a megvalósítási forráskódfájlokon keresztül.

**`Methods Declaration`** – Az összes metódusdeklaráció szerepel a .h fejlécfájlokban, hogy több megvalósítási fájlon keresztül is elérhető legyen.

**`Non-line Function Definitions`** - A fejlécfájlok nem soron belüli metódusok definícióit is tartalmazhatják.

## Az INC fájl PHP-ben való használatának hátránya

A PHP szerveroldali szkriptek, amelyek a szerveren futnak, és az eredményeket visszaküldik a hívó weboldalaknak. Ha egy PHP-fájl egy INC-fájlra hivatkozik, és a szerver nincs beállítva .inc-fájlok elemzésére (ami nagyon gyakori), a felhasználó az URL-könyvtárban megtekintheti a php-forráskódot az .inc fájlban. Tehát óvatosnak kell lennie az INC fájlok használatakor, mivel a PHP-ben tartalmaz fájlokat.

## Hivatkozások

* [Az INC használata PHP-ben](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

