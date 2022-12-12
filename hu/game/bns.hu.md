{
  "date" : "2021-10-20",
  "keywords" :[ "bns fájl", "bns fájl formátum", "mi az a bns fájl", "fájl", "bns példa", "Portal Bonus Map Script fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az ortal Bonus Map Script BNS fájlformátumról és az API-król, amelyek BNS-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"BNS - Portál bónusztérkép szkriptfájlja",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Mi az a BNS-fájl?

A .bns kiterjesztésű fájl egy játékszkript fájl, amelyet a Valve által kifejlesztett Portal Map rejtvénymegoldó játékkal hoztak létre. Szöveges parancsfájlt tartalmaz a .bsp fájlként tárolt portáltérkép információinak meghatározásához. A BNS-fájlok hivatkozásként szolgálnak erre a tényleges térképfájlra, és tartalmazzák a teljesítendő kihívások listáját. Ezenkívül tartalmaz térképnevet, megjegyzéseket a térképpel kapcsolatban, valamint miniatűr képfájl hivatkozásokat. A BNS-fájl bármely szövegszerkesztőben megnyitható, például a Notepad++-ban, a textEdit-ben és a Jegyzettömbben.

## BNS fájlformátum

A BNS-fájlok egyszerű szöveges fájlként kerülnek mentésre, amely ember által olvasható. Ezek a szövegszerkesztőkben megnyithatók és szerkeszthetők is. Ezeket azonban gondosan szerkeszteni kell, hogy elkerüljük a szkriptben előforduló hibákat.

## BNS fájlformátum példa

Egy BNS-fájl a következőhöz hasonlóan nézhet ki, ha egy szövegszerkesztőben, például a Notepad++-ban van megnyitva.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## Egy BNS-fájl részei

A fenti példában

* `#Bonus_Map_Challenges` - A térkép nevét jelöli.
* `térkép` - A játék térképmappájába kerülő térkép nevét jelöli
* `fejezet` - Azt a fejezetet jelöli, amelyhez a térkép tartozik. Az összes fejezetfájl a VPK-fájlban található a térkép nevének hozzáadásával `map your_map_name` formátumban.
* `Kép` - A térkép bélyegképét tartalmazza, és a gyökérútvonalon van tárolva: steam\steamapps\common\portal\portal\materials\VGUI.
* `Megjegyzés` - Leíró szöveg a létrehozott térképről.

## Hivatkozások

* [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

