---
date: 2019-10-11
keywords: json, .json, json fájlformátum, json fájlok megnyitása, javascript objektum jelölés, json adatformátum, .json fájlformátum
szerző:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON fájlformátum - Mi az a JSON fájl?
linktitle: JSON
description: "További információ a JSON-fájlformátumokról és az API-król, amelyek JSON-fájlokat hozhatnak létre és nyithatnak meg."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Mi az a JSON fájl?

A JSON (JavaScript Object Notation) egy nyílt szabványos fájlformátum az adatok megosztására, amely ember által olvasható szöveget használ az adatok tárolására és továbbítására. A JSON-fájlok tárolása .json kiterjesztéssel történik. A JSON kevesebb formázást igényel, és jó alternatíva az [XML](/hu/web/xml/) számára. A JSON a JavaScriptből származik, de nyelvtől független adatformátum. A JSON generálását és elemzését számos modern programozási nyelv támogatja. Az *application/json* a JSON-hoz használt médiatípus.

## JSON fájlformátum – Rövid előzmények

Valós idejű szerver-kliens kommunikációra volt szükség, amely a JSON létrehozásához vezetett. A JSON formátumot először Douglas Crockford határozta meg 2001 márciusában. A JSON az ECMA-262 szabvány 3. kiadásán (1999. december) alapult, amely a JavaScript egy részhalmaza.

Az ECMA-404 JSON-szabvány első kiadását 2013 októberében tette közzé az Ecma International. 2014-ben az RFC 7159 lett a JSON internethasználatának fő referenciapontja. 2017 novemberében az ISO/IEC 21778:2017 nemzetközi szabványként jelent meg. Az RFC 8259 szabványt 2017. december 13-án tette közzé az Internet Engineering Task Force, amely az Internet Standard STD 90 jelenlegi verziója.

## JSON fájlszerkezet

A JSON-adatok **kulcs/érték** párokba vannak írva. A kulcsot és az értéket kettőspont (:) választja el középen, a kulcs a bal oldalon, az érték pedig a jobb oldalon. A különböző kulcs/érték párokat vessző(,) választja el. A kulcs egy karakterlánc, dupla idézőjelek között, például "név". Az értékek a következő típusúak lehetnek.

- "Szám".
- "String": Unicode-karakterek sorozata, kettős idézőjelekkel körülvéve.
- "Boolean": igaz vagy hamis.
- "Tömb": például szögletes zárójelekkel körülvett értékek listája

``` json
[ "Alma", "Banán", "Narancs"]
```

- "Object": kulcs/érték párok gyűjteménye, amelyeket kapcsos zárójelek vesznek körül, például

``` json
{"név": "Jack", "életkor": 30, "kedvencSport" : "Futball"}
```

JSON-objektumok is beágyazhatók az adatok szerkezetének megjelenítéséhez. Az alábbiakban látható egy példa egy JSON-objektumra.

### JSON formátum példa

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Mekkora a JSON-fájl maximális mérete?

A JSON-fájlok maximális méretére gyakorlatilag nincs korlátozás. Olyan hosszú lehet, mint amennyi helyet igényel a tárolandó tartalom.

Amikor JSON fájlformátumot használunk az adatok interneten keresztüli átvitelére, óvatosnak kell lenni a számítógép rendelkezésre álló erőforrásaival kapcsolatban. Ha nagy JSON-adatokat visz át, az átvitelt befolyásolja, ha az ügyfélböngésző korlátozott memóriával rendelkezik.


A specifikáció nem határoz meg szigorú korlátozást, de ügyeljen arra, hogy ne merítse ki az erőforrásokat a felhasználók számítógépén, mivel ez gyorsan rontja a felhasználói élményt, és valószínűleg elhagyják az alkalmazást.

## JSON vs XML

Az **XML** egy másik gyakori és széles körben használt fájlformátum az interneten keresztüli adatcseréhez. Amikor az alkalmazások közötti adatcseréről van szó, a fejlesztőknek lehetőségük van XML és JSON fájlformátumok használatára is. A JSON azonban a legkényelmesebb módja az alkalmazások közötti interneten keresztüli adatcsere, a következő okok miatt.

1. A JSON áttekinthető és könnyebben olvasható nézetet biztosít az adatokról az XML fájlformátumokhoz képest
1. A JSON csökkenti az interneten keresztüli adatátvitel többletköltségét, mivel kevesebb karaktert tartalmaz ugyanazon adatkészlet meghatározásához, mint az XML
1. A modern programozási nyelvek beépített elemzőket biztosítanak a JSON-válasz webes elemzéséhez.

## Tudtad?

A FileFormat.com közreműködőjévé válhat, hogy a fájlformátum-közösséget naprakészen tartsa az eredményekről. Ha bármit meg kell osztania a JSON- vagy webes fájlformátumokkal kapcsolatban, közzéteheti megállapításait a [Web File Format News](https://news.fileformat.com/t/Web) részben, hogy az emberek többet megtudjanak ezekről.

## Hivatkozások

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [A JSON bemutatása](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

