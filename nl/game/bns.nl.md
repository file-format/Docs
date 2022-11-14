{
  "date" : "2021-10-20",
  "keywords" :[ "bns-bestand", "bns-bestandsindeling", "wat is een bns-bestand", "bestand", "bns-voorbeeld", "Portal Bonus Map Script-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over de ortal Bonus Map Script BNS-bestandsindeling en API's die BNS-bestanden kunnen maken en openen.",
  "title" :"BNS - Portal Bonus Map-scriptbestand",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Wat is een BNS-bestand?

Een bestand met de extensie .bns is een gamescriptbestand dat is gemaakt met de Portal Map-puzzeloplossingsgame die is ontwikkeld door Valve. Het bevat een tekstscript voor het definiëren van informatie over een Portal-kaart die is opgeslagen als .bsp-bestand. BNS-bestanden worden gebruikt als verwijzing naar dit eigenlijke kaartbestand en bevatten een lijst met uitdagingen die moeten worden voltooid. Daarnaast bevat het de naam van de kaart, opmerkingen over de kaart en verwijzingen naar miniatuurafbeeldingen. Een BNS-bestand kan in elke teksteditor worden geopend, zoals Notepad++, textEdit en Notepad.

## BNS-bestandsindeling

BNS-bestanden worden opgeslagen als platte tekstbestanden die voor mensen leesbaar zijn. Deze kunnen in teksteditors worden geopend en ook worden bewerkt. Deze moeten echter zorgvuldig worden bewerkt om fouten in het script te voorkomen.

## Voorbeeld BNS-bestandsindeling

Een BNS-bestand kan er ongeveer zo uitzien als het wordt geopend in een teksteditor zoals Notepad++.

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

## Delen van een BNS-bestand

In het bovenstaande voorbeeld,

* `#Bonus_Map_Challenges` - Vertegenwoordigt de naam van de kaart.
* `map` - Vertegenwoordigt de naam van de kaart die in de map met kaarten van het spel moet worden geplaatst
* `chapter` - Vertegenwoordigt het hoofdstuk waartoe de kaart behoort. Alle hoofdstukbestanden bevinden zich in het VPK-bestand door de naam van de kaart toe te voegen in het formaat `map your_map_name`
* `Afbeelding` - Het bevat de miniatuur van de kaart en wordt opgeslagen in het hoofdpad steam\steamapps\common\portal\portal\materials\VGUI.
* `Commentaar` - Beschrijvende tekst over de gemaakte kaart.

## Referenties

* [Portal Challenge-script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

