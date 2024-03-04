{
  "date": "2021-10-20",
  "keywords": [
"bns failą",
"bns failo formatas",
"kas yra bns failas",
"failą",
"bns pavyzdys",
"Portal Bonus Map Script failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie ortalinį „Bonus Map Script“ BNS failo formatą ir API, kurios gali kurti ir atidaryti BNS failus.",
  "title": "BNS - Portalo premijų žemėlapio scenarijaus failas",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-lts"
}
},
  "lastmod": "2021-10-20"
}

## Kas yra BNS failas?

Failas su plėtiniu .bns yra žaidimo scenarijaus failas, sukurtas naudojant Portal Map galvosūkių sprendimo žaidimą, kurį sukūrė Valve. Jame yra teksto scenarijus, skirtas apibrėžti informaciją apie portalo žemėlapį, kuris saugomas kaip .bsp failas. BNS failai naudojami kaip nuoroda į šį faktinį žemėlapio failą ir juose yra iššūkių, kuriuos reikia atlikti, sąrašas. Be to, jame yra žemėlapio pavadinimas, komentarai apie žemėlapį ir miniatiūrų failų nuorodos. BNS failą galima atidaryti bet kuriame teksto rengyklėje, pvz., Notepad++, textEdit ir Notepad.

## BNS failo formatas

BNS failai išsaugomi kaip paprasto teksto failai, kuriuos gali skaityti žmogus. Juos galima atidaryti ir redaguoti teksto rengyklėse. Tačiau juos reikia atidžiai redaguoti, kad scenarijuje nebūtų klaidų.

## BNS failo formato pavyzdys

BNS failas gali atrodyti maždaug taip, kai jis atidaromas teksto rengyklėje, pvz., Notepad++.

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

## BNS failo dalys

Aukščiau pateiktame pavyzdyje

 * `#Bonus_Map_Challenges` – nurodo žemėlapio pavadinimą.
 * Žemėlapis – nurodo žemėlapio pavadinimą, kuris bus įtrauktas į žaidimo žemėlapių aplanką
 * skyrius – nurodo skyrių, kuriam priklauso žemėlapis. Visi skyrių failai yra VPK faile, pridedant žemėlapio pavadinimą formatu `map your_map_name`
 * Vaizdas – jame yra žemėlapio miniatiūra ir jis saugomas pagrindiniame kelyje steam\steamapps\common\portal\portal\materials\VGUI.
 * `Komentaras` – aprašomasis tekstas apie sukurtą žemėlapį.

## Nuorodos

 * [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

