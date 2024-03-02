{
  "date": "2021-10-20",
  "keywords": [
"comhad bns",
"formáid comhaid bns",
"cad is comhad bns ann",
"comhad",
"sampla bns",
"Síneadh comhad Script Léarscáil Bónas Tairseach",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi ortal Bónas Léarscáil Script formáid comhaid BNS agus APIs ar féidir leo comhaid BNS a chruthú agus a oscailt.",
  "title": "BNS - Comhad Script Léarscáil Bónas Tairseach",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-gas"
}
},
  "lastmod": "2021-10-20"
}

## Cad is comhad BNS ann?

Is comhad scripte cluiche é comhad le síneadh .bns a cruthaíodh le cluiche réitigh puzal Portal Map a d'fhorbair Valve. Tá script téacs ann chun faisnéis a shainiú faoi léarscáil Tairseach a stóráiltear mar chomhad .bsp. Úsáidtear comhaid BNS mar thagairt don fhíorchomhad léarscáile seo agus tá liosta de na dúshláin atá le cur i gcrích ann. Ina theannta sin, tá ainm léarscáile, tuairimí faoin léarscáil, agus tagairtí comhad íomhá mionsamhlacha ann. Is féidir comhad BNS a oscailt in aon eagarthóir téacs ar nós Notepad++, textEdit, agus Notepad.

## Formáid Chomhaid BNS

Déantar comhaid BNS a shábháil mar chomhaid gnáth-théacs atá inléite ag daoine. Is féidir iad seo a oscailt in eagarthóirí téacs agus iad a chur in eagar freisin. Ba chóir iad seo a chur in eagar go cúramach, áfach, chun aon earráidí sa script a sheachaint.

## Sampla BNS Formáid Comhaid

Seans go mbeidh cuma mar seo a leanas ar chomhad BNS nuair a osclaítear é in eagarthóir téacs mar Notepad++.

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

## Páirteanna de Chomhad BNS

Sa sampla thuas,

 * `#Bónas_Map_Challenges` - Léiríonn sé ainm na léarscáile.
 * `mapa` - Léiríonn sé ainm na léarscáile atá le cur i bhfillteán léarscáileanna an chluiche
 * `chaibidil` - Léiríonn sé an chaibidil lena mbaineann an léarscáil. Tá gach comhad caibidle lonnaithe sa chomhad VPK trí ainm na léarscáile a chur leis san fhormáid `map your_map_name`
 * `Íomhá` - Tá mionsamhail na léarscáile ann agus tá sé stóráilte ag an bhfréamhchosán gaile \ steamapps \ common \ tairseach \ tairseach \ ábhair \ VGUI.
 * `Comment` - Téacs tuairisciúil faoin léarscáil a cruthaíodh.

## Tagairtí

 * [Script Dúshlán Tairseach](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

