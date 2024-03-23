{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOCK File Format - Mi az a zárfájl?",
  "description":"Ismerje meg a LOCK fájlformátumot és annak .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Mi az a LOCK fájl?

A **LOCK** fájl egy átnevezett fájl, amelyet alkalmazások és operációs rendszerek használnak egy fájl vagy egyes eszköz zároltként való megjelölésére. Ez arra utasítja a többi alkalmazást, hogy ne használják a fájlt, hacsak nem szabad az azt használó alkalmazástól. A legtöbb esetben ezek a zárfájlok üresek, de más esetekben a zárral kapcsolatos információkat, például tulajdonságokat és beállításokat tartalmazhatnak.

Néha a .lock fájlt a Microsoft .NET-keretrendszere használja az adatbázisfájlok **lockeed** másolatainak létrehozására. Ebben az esetben megnyílik az adatbázisfájl egy példánya .lock kiterjesztéssel. Ez nem teszi lehetővé a felhasználó számára, hogy módosítsa a fájlt, miközben azt egy másik felhasználó használja.

## Fájlformátum lezárása – További információ

Minden alkalmazás létrehoz egy LOCK fájlt, és a fájl formátuma az alkalmazásra jellemző. Ezek a zárfájlok szöveges és bináris formátumban is menthetők.

A zárolási fájlok jelenléte megakadályozza, hogy egy erőforrás egyidejűleg több fájlhoz is hozzáférjen, amelyek megpróbálják elérni az erőforrást. Létrejön az eredeti fájl másolata .lock kiterjesztéssel a nevéhez. Ez azt mondja a többi alkalmazásnak, hogy csak olvasási hozzáféréssel rendelkezzenek a fájlhoz. Például a resource.dat resource.data.lock lesz.

A Ruby programozási nyelvhez találkozhat a **gemfile.lock** fájllal. Itt tartja nyilván a Bundler a pontosan telepített verziókat. Így, amikor egy projektet/könyvtárat áthelyeznek egy másik gépre, a futó csomag a Gemfile-ben nézi meg a pontos megfelelő verziót.

## Fájl zárolása Linux alatt

A Linux kétféle fájlzárolást támogat: a tanácsadó zárolást és a kötelező zárolást.

* **Advisory Locks**: Nem érvényesített zárolás típusa. Ebben az esetben a résztvevő folyamatok együttműködnek egymással, kifejezetten zárolást szerezve. Ha ez nem lehetséges, a rendszer figyelmen kívül hagyja a figyelmeztető zárakat.

* **Kötelező zárolások**: Kötelező zárolás esetén az operációs rendszer kényszeríti a fájlok zárolását azáltal, hogy megakadályozza, hogy más folyamatok olvassák vagy írják a fájlt. Ez nem igényel semmilyen együttműködést a folyamatok között.

A kötelező zárolás nem igényel együttműködést a résztvevő folyamatok között. A kötelező zárolás aktiválása után az operációs rendszer megakadályozza, hogy más folyamatok olvassák vagy írják a fájlt.

## Hivatkozások

* [GemFile és Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Zárolás Linux alatt](https://www.baeldung.com/linux/file-locking)
