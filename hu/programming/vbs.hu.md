{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "file", "extension", "file format", "Visual Basic Script", "Programming Guide", "vbs example", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS – Visual Basic Script File",
  "description":"További információ a VBS fájlformátumról és az API-król, amelyek VBS-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Mi az a VBS fájl?

A VBS vagy a VBScript a Microsoft Visual Basic script kiadásához kapcsolódik. A számítástechnikai környezetben a felhasználó hozzáférhet és szabályozhatja annak számos aspektusát. A VBScript használhatja a **Component Object Model** nevű modellt a környezet elemeinek és eszközeinek használatához. Ez a környezet a VBScript működéséhez és futtatásához van megadva.

Hasonlóan szolgál a Javascript-hez, amikor az ügyfél hozzáfér a webfejlesztés területén. A szerverek weboldalak feldolgozására is használják. Megfontolható néhány más típusú szkriptfájlban, például a [HTML](/hu/web/html/) alkalmazásaiban.


## Rövid története ##

Először 1996-ban indították el, a Microsoft által a Windows Scriptekhez meghatározott technológiák részeként. Kezdetben kifejezetten a webfejlesztők segítségére lett kifejlesztve. Ugyanebben az évben megjelent a Microsoft Windows Explorer Internet Explorer nevű böngészője a Visual Basic Script szolgáltatásaival együtt.

A technológia és a webfejlesztés fejlődésével a VBScript számos verziója, valamint számos fejlett funkció megjelent. Sőt, a következő évben ez a szkriptnyelv új funkciókkal a Microsoft Windows része lesz.

## Műszaki specifikáció ##

A szerveroldali weboldalakhoz olyan eszközöket használnak, mint az **Active Server Pages** a VBScript mellett. Ez a szkriptnyelv a Windows parancsfájl-összetevőjében is használható. Ennek a nyelvnek a fájljait .vbs kiterjesztéssel tárolja a Windows.

Ennek a nyelvnek a kódjában számos vezérlőstruktúra található, például hurkok. Tartalmaz olyan argumentumokat is, amelyek parancssorosak, és nevezhetők vagy névtelenek. Az ilyen nyelvű fájlok egyszerűen a Windows operációs rendszer mappáiban vagy asztalán tárolhatók. Bár nincs speciális integrált fejlesztői környezet a VBScript programok számára, mint például a Microsoft Script Editor, biztosítják ennek a nyelvnek a fejlesztését.

Amikor a VBScriptet a Windows Script gazdagépe üzemelteti, az különféle funkciókat biztosít, amelyek meglehetősen gyakoriak a szkriptnyelvekben, de a Visual Basic 6.0-ban nem érhetők el. Az egyszerű vagy közvetlen hozzáférést igénylő szolgáltatások magukban foglalják a hálózati nyomtatókat, a névtelen és megnevezett parancssori argumentumokat, az stdout-ot és az stdin-t, a hálózati megosztásokat, a Windows Management Instrumentation-t, a hálózatok felhasználói adatait, például a csoporttagságot és még sok mást.

## VBS fájlformátum példa ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Hivatkozási szám

* [VBS – a Wikipedia által](https://en.wikipedia.org/wiki/VBScript)



