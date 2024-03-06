{
  "date": "2021-10-20",
  "keywords": [
"bns failu",
"bns faila formātā",
"kas ir bns fails",
"failu",
"bns piemērs",
"Portāla bonusa kartes skripta faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par ortal Bonus Map Script BNS faila formātu un API, kas var izveidot un atvērt BNS failus.",
  "title": "BNS - Portāla bonusa kartes skripta fails",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-lvs"
}
},
  "lastmod": "2021-10-20"
}

## Kas ir BNS fails?

Fails ar paplašinājumu .bns ir spēles skripta fails, kas izveidots ar Portal Map mīklu risināšanas spēli, ko izstrādāja Valve. Tajā ir teksta skripts, lai definētu informāciju par portāla karti, kas tiek saglabāta kā .bsp fails. BNS faili tiek izmantoti kā atsauce uz šo faktisko kartes failu, un tajos ir saraksts ar uzdevumiem, kas ir jāpabeidz. Turklāt tajā ir kartes nosaukums, komentāri par karti un sīktēlu faila atsauces. BNS failu var atvērt jebkurā teksta redaktorā, piemēram, Notepad++, textEdit un Notepad.

## BNS faila formāts

BNS faili tiek saglabāti kā vienkārša teksta faili, kas ir lasāmi cilvēkiem. Tos var atvērt teksta redaktoros un rediģēt. Tomēr tie ir rūpīgi jārediģē, lai izvairītos no skripta kļūdām.

## BNS faila formāta piemērs

BNS fails var izskatīties šādi, kad tas tiek atvērts teksta redaktorā, piemēram, Notepad++.

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

## BNS faila daļas

Iepriekš minētajā piemērā

 * `#Bonus_Map_Challenges` — attēlo kartes nosaukumu.
 * `karte` — apzīmē tās kartes nosaukumu, kas jāievieto spēles karšu mapē
 * `nodaļa` — apzīmē nodaļu, kurai karte pieder. Visi nodaļu faili atrodas VPK failā, pievienojot kartes nosaukumu formātā `karte jūsu_kartes_nosaukums`
 * Attēls — tas satur kartes sīktēlu un tiek saglabāts saknes ceļā steam\steamapps\common\portal\portal\materials\VGUI.
 * `Komentārs` - aprakstošs teksts par izveidoto karti.

## Atsauces

 * [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

