{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Kézieszköz-jelölőnyelvi fájl",
  "description":"További információ a HDML-fájlformátumról és az API-król, amelyek HDML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## Mi az a HDML fájl?

A .hdml (Handheld Device Markup Language) kiterjesztésű fájl egy jelölőnyelv weboldalak létrehozására hordozható elektronikus eszközökhöz, például kézi számítógépekhez, okostelefonokhoz és információs megjelenítő eszközökhöz. A HDML állítólag az [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) nyelv kiterjesztése. A HDML hasonló a HTML-hez, de olyan vezeték nélküli és kézi eszközökhöz, amelyek kis kijelzővel rendelkeznek, például PDA-k, mobiltelefonok és így tovább. Felváltotta a WML, amelyre fontos hatással volt.

## HDML fájlformátum – További információ

A HDML egy kézi eszközök jelölőnyelve, amely a HTML-hez hasonló jelölőcímkéken alapul. A HDML-t benyújtották a W3C-hez szabványosítás céljából, de soha nem vált szabványossá. Fájlformátumának specifikációi azonban referenciaként elérhetők a [W3 webhelyén](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html). A [HDML nyelv szintaxisa](https://www.w3.org/TR/hdml20-5.html#HEADING5-0) elérhető a fejlesztők számára, és használható példaalkalmazás-fejlesztéshez.

## HDML elemek

Az alábbiakban felsoroljuk azokat az elemeket, amelyek futásidejű környezetet biztosítanak a HDML számára, és amelyekre felhasználói ügynökként hivatkozunk.

|Elem|Leírás|
---|---|
|Kártyák|Ez a HDML alapvető építőköve, és megjeleníti és lehetővé teszi a felhasználó számára, hogy az információs kártyákkal kommunikáljon. |
|Packok|A HDML-kártyák pakliba vannak csoportosítva. A HDML-csomag hasonló a HTML-oldalhoz, mivel az URL [RFC1738] azonosítja, és a kiszolgálótól kért és a felhasználói ügynök által gyorsítótárazott tartalom egysége.|
|Műveletek|A műveletek lehetnek PREV, SOFT1-SOFT8 és HELP típusúak. Ezek absztraktak, és a felhasználói felület felhasználói ügynök-specifikus módon támogatott.|
|Tevékenységek|Egy tevékenység olyan, mint egymáshoz kapcsolódó kártyák csoportja, amelyek egyetlen logikai funkciót hajtanak végre. Ezek egy vagy több fedélzetre is kiterjedhetnek. A HDML-navigációs és állapotmodell tevékenységek köré épül fel.|
|Előzmény alapú navigáció|A felhasználói ügynök a felhasználó számára megjelenített kártyák előzményeit vezeti. Minden egyes elért kártya hozzáadódik a kártyaelőzményekhez. A felhasználói ügynök lehetővé teszi a felhasználó számára, hogy könnyen visszanavigáljon az előzmények előző kártyájához.|

## Hivatkozások

* [HDML – Wikipédia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML-specifikációk – W3 Schools](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

