{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru MK3D",
  "keywords" :[ "mk3d", "matroska video", "formát mkv", "stereoskopické 3d", "StereoMode", "video", "soubor", "formát" ],
  "description":"Zjistěte více o formátu souboru MK3D pro stereoskopická 3D videa vytvořená Matroskou a API, která mohou vytvářet a otevírat soubory MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Co je soubor MK3D? ##

Soubory MK3D patří do rodiny video formátů Matroska. Tyto soubory jsou ve skutečnosti **stereoskopická 3D** videa vytvořená pomocí formátu Matroska 3D. Kontejner souboru MKV používá hodnotu pole StereoMode k definování typu stereoskopického 3D videa. K dispozici je také hodnota StereoMode pro zobrazení starých stereo 3D videí oddělením azurové a červené barvy (AnaGlyph)

## Technické údaje ##
3D videa lze komprimovat následujícími dvěma způsoby:

- Samostatná dráha pro každé oko.
- Zkombinujte každé sledování očí do jedné stopy.

Souborový kontejner MKV podporuje obojí.

Pro jednostopá videa, která jsou s 3D materiálem uvnitř snazší, musíte nastavit pole **StereoMode**, které rozhodne, zda budou letadla sestavena do mono nebo levé pravé kombinované stopy. Můžete použít jednu z následujících hodnot pole StereoMode:

|Hodnota | Popis |
|---|---|
|0| mono|
|1| vedle sebe (levé oko je první)|
|2| nahoře-dole (pravé oko je první)|
|3| nahoře-dole (levé oko je první)|
|4| šachovnice (pravá je první)|
|5| šachovnice (vlevo je první)|
|6| řádek prokládaný (pravý je první)|
|7| řádek prokládaný (vlevo je první)|
|8| sloupec prokládaný (pravý je první)|
|9| sloupec prokládaný (vlevo je první)|
|10| anaglyf (azurová/červená)|
|11| vedle sebe (pravé oko je první)|
|12| anaglyf (zelená/purpurová)|
|13| obě oči sešněrované v jednom bloku (levé oko je první) (sekvenční režim pole)|
|14| obě oči sešněrované v jednom bloku (pravé oko je první) (sekvenční režim pole)|

U více kolejí musí kontejner MKV rozhodnout o funkčnosti každé koleje samostatně. K této práci se používá **TrackOperation** s **TrackCombinePlanes**.


## Reference ##

- [Poznámky ke specifikaci Matrosky](https://www.matroska.org/technical/notes.html)
- [Podpora kontejneru souborů MKV pro stereo 3D video a soubory MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

