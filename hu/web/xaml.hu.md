{
  "date" : "2019-10-11",
  "keywords" :[ "xaml", "xaml fájl", "xaml fájlformátum", "xaml fájltípus", "fájl", "típus", "mi az xaml fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAML – XML alapú jelölőnyelv",
  "description":"További információ a XAML fájlformátumról és az API-król, amelyek XAML fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "XAML ",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a XAML fájl?

Az XAML, az Extensible Application Markup Language, a kiterjesztésfájlok a Windows Presentation Foundation (WPF) alapú szoftveralkalmazások felhasználói felületének elemeit írják le. Bár nyelv, nem kell programozni, mivel a **[XML](/hu/web/xml/)** szabványos formátumán alapul, amely könnyen használható és érthető. Az XAML-t (ejtsd: "zammel") a Microsoft fejlesztette ki, kifejezetten felhasználói felületek létrehozására. Az eredeti mozaikszó az Extensible Avalon Markup Language kifejezést jelentette, ahol az Avalon a WPF kódneve. A XAML fájlokat néha XOML kiterjesztéssel is mentik.

## XAML alkalmazások

Az XAML a .NET Framework 3.0 és a .NET Framework 4.0 technológiák, például a WPF, a Silverlight, a Windows Workflow Foundation (WF) és néhány más technológiában használható. A felhasználói felület elemeit, az adat-összerendeléseket, az eseményeket és egyéb jellemzőket a WPF XAML űrlapjai határozzák meg. Hasonlóképpen, a WF munkafolyamatai XAML használatával definiálhatók. Eszközökkel könnyen feldolgozható, mivel XML-alapú. Mivel ez egy deklaratív nyelv, és nem igényel fordítást, sok olyan termék jelenik meg, amelyek XAML-alapú alkalmazásokon alapulnak. Bármi, amit XAML-ben hoztak létre vagy implementáltak, kifejezhető egy hagyományos .NET nyelven, például C# vagy Visual Basic .NET használatával.

## XAML fájlformátum

Az XAML teljes mértékben az XML formátumon alapul. Az [XAML Object Mapping] kezdeti specifikációit (http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML%5D.pdf) tették közzé 2006, majd egy másik [verzió](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf) 2009. Ezek a specifikációk két absztrakt információs modellt határoznak meg:

* XAML séma információs készlet modell
* XAML információs készlet modell

Az Xaml információkészlet (röviden 'Xaml Infoset') határozza meg az Xaml-példány által reprezentálható információk szerkezetét. Az Xaml séma információs készlet lehetővé teszi bizonyos Xaml szótárak meghatározását. Ez a specifikáció egy XML-dokumentum Xaml-információs készletté alakítására vonatkozó szabályokat is meghatároz. Az XML az Xaml általános formátuma. (Az „Xaml-dokumentum” kifejezés olyan XML-dokumentumra utal, amely egy Xaml-információs készletet képvisel.) De bár ez a specifikáció nem határoz meg semmilyen más ábrázolást, bármilyen fizikai ábrázolás használható mindaddig, amíg az Xaml információs készletben lévő információkat képes reprezentálni. .

## Hivatkozások

* [XAML – a Wikipedia által](https://en.wikipedia.org/wiki/Extensible_Application_Markup_Language)
* [XAML fájlformátum specifikációi](http://download.microsoft.com/download/0/A/6/0A6F7755-9AF5-448B-907D-13985ACCF53E/%5BMS-XAML-2009%5D.pdf)

