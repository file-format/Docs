{
  "date" : "2021-10-20",
  "keywords" :[ "bns fil", "bns filformat", "vad är en bns fil", "fil", "bns exempel", "Portal Bonus Map Script filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om ortal Bonus Map Script BNS-filformat och API:er som kan skapa och öppna BNS-filer.",
  "title" :"BNS - Portal Bonus Map Script File",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Vad är en BNS fil?

En fil med tillägget .bns är en spelskriptfil skapad med Portal Map-pussellösningsspel som utvecklats av Valve. Den innehåller textskript för att definiera information om en portalkarta som lagras som .bsp-fil. BNS-filer används som referens till denna faktiska kartfil och innehåller en lista över utmaningar som ska genomföras. Dessutom innehåller den kartnamn, kommentarer om kartan och referenser till miniatyrbilder. En BNS-fil kan öppnas i vilken textredigerare som helst som Notepad++, textEdit och Notepad.

## BNS filformat

BNS-filer sparas som vanliga textfiler som är läsbara för människor. Dessa kan öppnas i textredigerare och även redigeras. Dessa bör dock redigeras noggrant för att undvika eventuella fel i skriptet.

## Exempel på BNS-filformat

En BNS-fil kan se ut ungefär som följande när den öppnas i en textredigerare som Notepad++.

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

## Delar av en BNS-fil

I exemplet ovan,

* `#Bonus_Map_Challenges` - Representerar namnet på kartan.
* `karta` - Representerar namnet på kartan som ska placeras i spelets kartmapp
* `kapitel` - Representerar kapitlet som kartan tillhör. Alla kapitelfiler finns i VPK-filen genom att lägga till namnet på kartan i formatet `map your_map_name`
* `Bild` - Den innehåller miniatyren av kartan och lagras på rotvägen steam\steamapps\common\portal\portal\materials\VGUI.
* `Kommentar` - Beskrivande text om den skapade kartan.

## Referenser

* [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

