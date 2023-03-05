{
  "date" : "2021-10-20",
  "keywords" :[ "bns-Datei", "bns-Dateiformat", "was ist eine bns-Datei", "Datei", "bns-Beispiel", "Portal Bonus Map Script-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das BNS-Dateiformat von ortal Bonus Map Script und APIs, die BNS-Dateien erstellen und öffnen können.",
  "title" :"BNS - Portal-Bonuskarten-Skriptdatei",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Was ist eine BNS-Datei?

Eine Datei mit der Erweiterung .bns ist eine Spielskriptdatei, die mit dem von Valve entwickelten Rätsellösungsspiel Portal Map erstellt wurde. Es enthält ein Textskript zum Definieren von Informationen über eine Portalkarte, die als .bsp-Datei gespeichert ist. BNS-Dateien werden als Verweis auf diese eigentliche Kartendatei verwendet und enthalten eine Liste von Herausforderungen, die abgeschlossen werden müssen. Darüber hinaus enthält es den Kartennamen, Kommentare zur Karte und Verweise auf Miniaturbilddateien. Eine BNS-Datei kann in jedem Texteditor wie Notepad++, textEdit und Notepad geöffnet werden.

## BNS-Dateiformat

BNS-Dateien werden als Klartextdateien gespeichert, die für Menschen lesbar sind. Diese können in Texteditoren geöffnet und ebenfalls bearbeitet werden. Diese sollten jedoch sorgfältig bearbeitet werden, um Fehler im Skript zu vermeiden.

## Beispiel für ein BNS-Dateiformat

Eine BNS-Datei kann etwa wie folgt aussehen, wenn sie in einem Texteditor wie Notepad++ geöffnet wird.

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

## Teile einer BNS-Datei

Im obigen Beispiel

* `#Bonus_Map_Challenges` - Repräsentiert den Namen der Karte.
* `map` - Repräsentiert den Namen der Karte, die in den Kartenordner des Spiels eingefügt werden soll
* "Kapitel" - Repräsentiert das Kapitel, zu dem die Karte gehört. Alle Kapiteldateien befinden sich in der VPK-Datei, indem der Name der Karte im Format „map your_map_name“ hinzugefügt wird
* `Bild` - Es enthält die Miniaturansicht der Karte und wird im Stammpfad steam\steamapps\common\portal\portal\materials\VGUI gespeichert.
* `Kommentar` - Beschreibender Text über die erstellte Karte.

## Verweise

* [Portal-Challenge-Skript](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

