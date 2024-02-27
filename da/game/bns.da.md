{
  "date": "2021-10-20",
  "keywords": [
"bns fil",
"bns filformat",
"hvad er en bns-fil",
"fil",
"bns eksempel",
"Portal Bonus Map Script filudvidelse",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om ortal Bonus Map Script BNS-filformat og API'er, der kan oprette og åbne BNS-filer.",
  "title": "BNS - Portal Bonus Map Script File",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-das"
}
},
  "lastmod": "2021-10-20"
}

## Hvad er en BNS fil?

En fil med filtypenavnet .bns er en spilscriptfil, der er oprettet med Portal Map-puslespil, der blev udviklet af Valve. Det indeholder tekstscript til at definere information om et portalkort, som er gemt som .bsp-fil. BNS-filer bruges som reference til denne aktuelle kortfil og indeholder en liste over udfordringer, der skal løses. Derudover indeholder det kortnavn, kommentarer om kortet og referencer til miniaturebilleder. En BNS-fil kan åbnes i en hvilken som helst teksteditor, såsom Notepad++, textEdit og Notepad.

## BNS filformat

BNS-filer gemmes som almindelige tekstfiler, der kan læses af mennesker. Disse kan åbnes i teksteditorer og også redigeres. Disse bør dog redigeres omhyggeligt for at undgå fejl i scriptet.

## Eksempel på BNS-filformat

En BNS-fil kan se nogenlunde sådan ud, når den åbnes i en teksteditor, såsom Notepad++.

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

## Dele af en BNS-fil

I ovenstående eksempel,

 * `#Bonus_Map_Challenges` - Repræsenterer navnet på kortet.
 * `map` - Repræsenterer navnet på det kort, der skal placeres i spillets maps folder
 * `kapitel` - Repræsenterer det kapitel, kortet tilhører. Alle kapitelfilerne er placeret i VPK-filen ved at tilføje navnet på kortet i formatet `map your_map_name`
 * `Billede` - Det indeholder miniaturebilledet af kortet og er gemt på rodstien steam\steamapps\common\portal\portal\materials\VGUI.
 * `Kommentar` - Beskrivende tekst om det oprettede kort.

## Referencer

 * [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

