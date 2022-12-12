{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "fájl", "kiterjesztés", "fájlformátum", "hta implementáció", "Programozási útmutató", "hta példa", "HTML alkalmazás", "Hypertext Markup Language Application", "HTA fájlok", "Microsoft HTML Application"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA – HTML alkalmazásfájlok",
  "description":"További információ a HTA fájlformátumról és az API-król, amelyek HTA-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Mi az a HTA fájl?

A HTMLA a **Hypertext Markup Language Application** rövidítése egy olyan program, amely kompatibilis a Microsoft Windows rendszerrel. A program forráskódja egynél több szkriptnyelvet tartalmaz, például [HTML](/hu/web/html/) és [JavaScript](/hu/web/js/). A felhasználói felülethez a HTML-alkalmazást részesítjük előnyben, míg a programlogikai követelmény teljesítése érdekében bármilyen más szkriptnyelvet használunk.

A HTML-alkalmazások függetlenek az internetböngésző biztonsági modelljétől, és teljesen megbízható alkalmazásként futnak. Az ezekkel az alkalmazásokkal kapcsolatos fájlok kiterjesztése HTA. Ezek az alkalmazások a HTML szolgáltatásait, valamint más szkriptnyelvek tulajdonságait tartalmazzák.


## Rövid története ##

A HTA-t először 1999-ben vezette be a Microsoft, az Internet Explorer 5 kiadásával együtt. Kompatibilis volt az Internet Explorerrel, így csak Windows operációs rendszeren volt futtatható. Ezt a technológiát 2003-ban szabadalmazták. A HTA fájlok ugyanúgy futnak, mint bármely más .exe fájl. A HTA fájlok a Windows 11 mai frissített verziójával is kompatibilisek.


## Műszaki specifikáció ##

A HTA-k formátuma megegyezik bármely más HTML-oldallal, míg néhány attribútum a programok kereteinek vagy ikonjainak stílusának vezérlésére szolgál. Ezen túlmenően érvek is szerepelnek a HTA elindítása mellett. Ezek az alkalmazások az mshta.exe nevű programmal futtathatók. Egyszerűen a fájlra duplán kattintva érhető el. Ezek a programok automatikusan futnak az Internet Explorerrel együtt. Az egyéb specifikációk mellett ezek nem függetlenek a Trident motorböngészőtől, de függetlenek az Internet Explorertől. Ez azt jelenti, hogy ezek az Internet Explorer használata nélkül is végrehajthatók.

A címkéket az alkalmazások megjelenésének testreszabása érdekében használjuk. A Microsoft HTML alkalmazásból HTA formátumba való átalakítás egyszerűbb, azaz csak a kiterjesztést kell módosítani. Mint tudjuk, hogy ezek az alkalmazások teljes mértékben megbízhatóak, így ezek több szolgáltatást és előnyt kínálnak az egyszerű HTML-fájlokhoz képest. Szövegszerkesztők használhatók HTA létrehozására. Ezeket a szerkesztőket a Microsoft vagy bármely más megbízható forrás beszerezheti.


## HTA fájlformátum példa ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Hivatkozási szám

* [HTA – a Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



