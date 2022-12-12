{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "asmx fájl", "asmx fájlformátum", "asmx fájltípus", "fájl", "típus", "mi az asmx fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX – ASP.NET webszolgáltatási fájl",
  "description" :"További információ az ASMX-fájlokról és az API-król, amelyek ASMX-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Mi az ASMX fájl?

Az .asmx kiterjesztésű fájl egy ASP.NET webszolgáltatás-fájl, amely kommunikációt biztosít két objektum között az interneten keresztül a Simple Object Access Protocol (SOAP) használatával. Szolgáltatásként kerül telepítésre a Windows-alapú webszerveren a bejövő kérések feldolgozására és a válasz visszaküldésére. Ellentétben az [ASPX](/hu/web/aspx/) fájlokkal, amelyek az ASP.NET weboldalak vizuális megjelenítéséhez szükséges kódot tartalmazzák, az ASMX fájlok a szerveren futnak a háttérben, és különféle feladatokat hajtanak végre, mint például az adatbázishoz való csatlakozás, az adatok lekérése és visszaadása a kérés formátuma. Ezeket kifejezetten XML webszolgáltatásokhoz használják.

## ASMX fájlformátum

Az ASMX fájlok egyszerű szöveges formátumúak, és olyan alkalmazásokban nyithatók meg vagy szerkeszthetők, mint a Microsoft Visual Studio vagy szövegszerkesztők. Ez a Microsoft szabadalmaztatott fájlformátuma, és jól meghatározott szintaxissal rendelkezik a webszolgáltatások létrehozásához. A SOAP XML formátumú ASMX-fájl válasza a következő elemeket tartalmazza.

* `Envelop` – gyökérelem, amely az XML-dokumentumot SOAP-üzenetként azonosítja.
* `Header` – Opcionális elem, amely alkalmazás-specifikus információkat, például hitelesítési adatokat tartalmaz. Ha a Header elem jelen van, annak az Envelope elem első gyermek elemének kell lennie.
* "Body" - A címzettnek szánt SOAP üzenetet tartalmazza.
* `Hiba` – Nem kötelező elem, amely hibaüzeneteket jelez. Ha a Hiba elem jelen van, akkor annak a Body elem gyermekelemének kell lennie.

Az ASMX fájlok .NET nyelveken írhatók, például [C#](/hu/programming/cs/), [Visual Basic](/hu/programming/vb/) vagy JScript.

## Miben különbözik az ASMX az ASPX-től és az ASCX-től?

Az ASMX fájlok eltérnek az ASPX és ASCX fájloktól.

* Az ASPX, az Active Server Pages, a fájlok olyan programozási fájlok, amelyeket a webszervereken futó Microsoft ASP.NET keretrendszer segítségével állítanak elő. Ezek az ügyfél webböngészőjében jelennek meg, amikor a felhasználó hozzáférést kér egy ilyen oldalhoz.
* Az ASCX, az Active Server User Control olyan felhasználói vezérlőket határoz meg, amelyek az ASP.NET weboldalakon vagy a teljes webhelyen újrafelhasználható vezérlők meghatározására szolgálnak.

## Hivatkozások

* [Az ASMX szolgáltatás igénybevétele](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [ASCX felhasználói vezérlés](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

