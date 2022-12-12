{
  "date" : "2021-10-20",
  "keywords" :[ "soubor bns", "formát souboru bns", "co je soubor bns", "soubor", "příklad bns", "přípona souboru Portal Bonus Map Script", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru BNS ortal Bonus Map Script a rozhraních API, která mohou vytvářet a otevírat soubory BNS.",
  "title" :"BNS - Portal Bonus Map Script File",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Co je soubor BNS?

Soubor s příponou .bns je soubor se skriptem hry vytvořený pomocí hry na řešení hádanek Portal Map, která byla vyvinuta společností Valve. Obsahuje textový skript pro definování informací o mapě portálu, který je uložen jako soubor .bsp. Soubory BNS se používají jako reference na tento skutečný mapový soubor a obsahují seznam výzev, které je třeba dokončit. Kromě toho obsahuje název mapy, komentáře k mapě a odkazy na soubory miniatur. Soubor BNS lze otevřít v libovolném textovém editoru, jako je Notepad++, textEdit a Notepad.

## Formát souboru BNS

Soubory BNS se ukládají jako prosté textové soubory, které jsou čitelné pro člověka. Ty lze otevřít v textových editorech a také je upravovat. Ty by však měly být pečlivě upraveny, aby se předešlo chybám ve skriptu.

## Příklad formátu souboru BNS

Soubor BNS může při otevření v textovém editoru, jako je Notepad++, vypadat nějak takto.

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

## Části souboru BNS

Ve výše uvedeném příkladu

* `#Bonus_Map_Challenges` - Představuje název mapy.
* `map` - Představuje název mapy, která má být vložena do složky map ve hře
* `kapitola` - Představuje kapitolu, do které mapa patří. Všechny soubory kapitol jsou umístěny v souboru VPK přidáním názvu mapy ve formátu `map your_map_name`
* `Obrázek` - Obsahuje miniaturu mapy a je uložen v kořenové cestě steam\steamapps\common\portal\portal\materials\VGUI.
* `Komentář` - Popisný text o vytvořené mapě.

## Reference

* [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

