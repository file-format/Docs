{
  "date" : "2021-07-13",
  "keywords" :[ "scr fájl", "mi az scr fájl", "fájl", "scr példa", "scr fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - Windows Screensaver File",
  "description":"További információ az SCR fájlformátumról és az SCR-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## Mi az SCR fájl?
Az .scr kiterjesztésű fájl a Microsoft Windows operációs rendszer által használt képernyővédő fájl. Animációkat, grafikákat, diavetítéseket vagy videókat tartalmaz, amelyek Windows képernyővédőként használhatók. Az SCR-fájlokat általában a Microsoft Windows főkönyvtárában tárolják. A képernyővédőknek meg kellett volna akadályozniuk, hogy a CRT vagy plazma számítógép-monitorok olyan állapotba kerüljenek, amely akkor fordul elő, ha a képernyő túl sokáig mutatja ugyanazt a képet. A legújabb monitorok ugyan nem szenvednek ilyen állapotot, de a képernyővédőket biztonsági okokból továbbra is a képernyő megakadályozására használják.

## SCR fájlformátum
A képernyővédő olyan számítógépes program, amely animált képekkel vagy mintákkal tölti meg, ha a számítógépen hosszú ideig semmilyen tevékenység nem történik. A képernyővédőket azért vezették be, hogy megakadályozzák a foszfor beégését a plazma, a katódsugárcső (CRT) és az OLED számítógép-monitorokon. A képernyővédőket általában úgy állítják be, hogy egy alapvető biztonsági réteget alkalmazzanak, és jelszót kérnek az eszköz újranyitásához. A képernyővédőket általában különféle programozási nyelvek, valamint grafikus felületek segítségével fejlesztik és kódolják. A képernyővédők fejlesztői többnyire a C vagy C++ programozási nyelveket használják, valamint grafikus könyvtárakat vagy GDI-ket, például az OpenGL-t, amely számos 3D-s megjelenítésre képes platformon működik. A képernyővédők kimenete hordozható futtatható fájlként kerül mentésre.

### SCR fájlhasználat
A régi katódsugárcsöves vagy plazma alapú monitoroknál azért jelentették a képernyőégést, mert ugyanaz a kép volt látható a képernyőn hosszú ideig. A képernyő leégése olyan eset, amikor a képernyő belsejében lévő foszfor bevonat exponált területeinek tulajdonságai fokozatosan megváltoznak, és végül elsötétült árnyékképhez vezet a képernyőn. A képernyővédőknek tehát folyamatosan változtatniuk kellett a képernyőképet, és általában az .scr fájlok nélkülözhetetlenek voltak az ATM-ek vagy a vasúti jegykiadó automaták monitoraihoz. Később az LCD-k és a monitorok fejlettebb verziói megoldották a problémát. Ezért a képernyővédőket a modern korban is használják, hogy megvédjék a tétlen eszközöket a második személy használatától. Jelszó vagy minta szükséges az eszköz újbóli eléréséhez.

## Képernyővédő létrehozása C# segítségével
Bár bármelyik .NET programozási nyelven létrehozhatunk képernyővédőt, itt a C# programozási nyelv adott:

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
Módosítsa a végrehajtható fájl kiterjesztését .exe-ről .scr-re. Tehát az SCR fájl elnevezése ScreenSaver.scr.

## Hivatkozások

* [Képernyővédő](https://en.wikipedia.org/wiki/Screensaver)
* [Írjon olyan képernyővédőt, amely valóban működik](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


