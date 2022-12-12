{
  "date" : "2021-10-20",
  "keywords" :[ "fișier bns", "format fișier bns", "ce este un fișier bns", "fișier", "exemplu bns", "Extensie fișier Portal Bonus Map Script", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier BNS ortal Bonus Map Script și despre API-urile care pot crea și deschide fișiere BNS.",
  "title" :"BNS - Fișier script Portal Bonus Map",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Ce este un fișier BNS?

Un fișier cu extensia .bns este un fișier script de joc creat cu jocul de rezolvare a puzzle-urilor Portal Map care a fost dezvoltat de Valve. Conține un script text pentru definirea informațiilor despre o hartă Portal care este stocată ca fișier .bsp. Fișierele BNS sunt folosite ca referință la acest fișier de hartă real și conțin o listă de provocări care urmează să fie finalizate. În plus, conține numele hărții, comentarii despre hartă și referințe la fișierele cu imagini în miniatură. Un fișier BNS poate fi deschis în orice editor de text, cum ar fi Notepad++, textEdit și Notepad.

## Format de fișier BNS

Fișierele BNS sunt salvate ca fișiere text simplu, care pot fi citite de om. Acestea pot fi deschise în editorii de text și editate, de asemenea. Cu toate acestea, acestea ar trebui editate cu atenție pentru a evita orice erori în script.

## Exemplu de format de fișier BNS

Un fișier BNS poate arăta așa cum urmează atunci când este deschis într-un editor de text, cum ar fi Notepad++.

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

## Părți ale unui fișier BNS

În exemplul de mai sus,

* `#Bonus_Map_Challenges` - Reprezintă numele hărții.
* `map` - Reprezintă numele hărții care va fi pus în folderul hărți al jocului
* `capitol` - Reprezintă capitolul căruia îi aparține harta. Toate fișierele de capitol sunt localizate în fișierul VPK prin adăugarea numelui hărții în formatul `map your_map_name`
* `Imagine` - Conține miniatura hărții și este stocată la calea rădăcină steam\steamapps\common\portal\portal\materials\VGUI.
* `Comment` - Text descriptiv despre harta creată.

## Referințe

* [Script Portal Challenge](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

