{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM fájl – kézi eszköz jelölőnyelvi fájl",
  "description":"További információ a HDM fájlformátumról és az API-król, amelyek HDM-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## Mi az a HDM fájl?

A HDM-fájl egy jelölőnyelvi weboldalfájl, amely a kézieszköz-jelölőnyelven (HDML) jön létre. A [HTML](/hu/web/html/) nyelvhez hasonló jelölőcímkéket tartalmaz, de kézi elektronikus eszközökhöz, például okostelefonokhoz és PDA-khoz tervezték. A [HDML fájlformátum specifikációit] (https://www.w3.org/TR/NOTE-Submission-HDML-spec.html) benyújtották a W3C-nek szabványosításra, de nem válhattak szabványossá. A HDM a W3 webhelyén elérhető [HDML](/hu/web/hdml/) fájlformátum-specifikációkon alapul.

## HDM fájlformátum – További információ

A HDM-fájl jelölőcímkékből áll, amelyek a kézi eszközökön vizuálisan megtervezett webhelyen jelennek meg. A HDM-fájlok a HTML-oldalakhoz használt HTTP-protokoll helyett a HDTP (Handheld Device Transport Protocol) protokollt használó eszközökre másolódnak.

## HDML fájlelemek

Az alábbiakban felsoroljuk azokat az elemeket, amelyek futásidejű környezetet biztosítanak a HDML számára, és amelyekre felhasználói ügynökként hivatkozunk.

|Elem|Leírás|
---|---|
|Kártyák|Ez a HDML alapvető építőköve, és megjeleníti és lehetővé teszi a felhasználó számára, hogy az információs kártyákkal kommunikáljon. |
|Packok|A HDML-kártyák pakliba vannak csoportosítva. A HDML-csomag hasonló a HTML-oldalhoz, mivel az URL [RFC1738] azonosítja, és a kiszolgálótól kért és a felhasználói ügynök által gyorsítótárazott tartalom egysége.|
|Műveletek|A műveletek lehetnek PREV, SOFT1-SOFT8 és HELP típusúak. Ezek absztraktak, és a felhasználói felület felhasználói ügynök-specifikus módon támogatott.|
|Tevékenységek|Egy tevékenység olyan, mint egymáshoz kapcsolódó kártyák csoportja, amelyek egyetlen logikai funkciót hajtanak végre. Ezek egy vagy több fedélzetre terjedhetnek ki. A HDML-navigációs és állapotmodell tevékenységek köré épül fel.|
|Előzmény alapú navigáció|A felhasználói ügynök a felhasználó számára megjelenített kártyák előzményeit vezeti. Minden egyes elért kártya hozzáadódik a kártyaelőzményekhez. A felhasználói ügynök lehetővé teszi a felhasználó számára, hogy könnyen visszanavigáljon az előzmények előző kártyájához.|

## Hivatkozások

* [HDML – Wikipédia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML-specifikációk – W3 Schools](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

