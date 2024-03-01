{
  "date": "2021-10-20",
  "keywords": [
"bns tiedosto",
"bns tiedostomuoto",
"mikä on bns-tiedosto",
"tiedosto",
"bns esimerkki",
"Portal Bonus Map Script -tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi ortal Bonus Map Script BNS-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata BNS-tiedostoja.",
  "title": "BNS - Portaalin bonuskarttakooditiedosto",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bn-fis"
}
},
  "lastmod": "2021-10-20"
}

## Mikä on BNS-tiedosto?

Tiedosto, jonka laajennus on .bns, on pelin skriptitiedosto, joka on luotu Valven kehittämällä Portal Map -pulmapelin avulla. Se sisältää tekstikomentosarjan .bsp-tiedostona tallennetun portaalikartan tietojen määrittämiseksi. BNS-tiedostoja käytetään viitteenä tähän varsinaiseen karttatiedostoon, ja ne sisältävät luettelon suoritettavista haasteista. Lisäksi se sisältää kartan nimen, karttaa koskevia kommentteja ja pikkukuvatiedostoviittauksia. BNS-tiedosto voidaan avata missä tahansa tekstieditorissa, kuten Notepad++, textEdit ja Notepad.

## BNS-tiedostomuoto

BNS-tiedostot tallennetaan vain tekstitiedostoina, jotka ovat ihmisen luettavissa. Näitä voidaan avata tekstieditoreissa ja myös muokata. Näitä tulee kuitenkin muokata huolellisesti, jotta vältytään kirjoitusvirheiltä.

## Esimerkki BNS-tiedostomuodosta

BNS-tiedosto voi näyttää tältä, kun se avataan tekstieditorilla, kuten Notepad++.

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

## BNS-tiedoston osia

Yllä olevassa esimerkissä

 * `#Bonus_Map_Challenges` - Edustaa kartan nimeä.
 * `kartta` - Edustaa pelin karttakansioon lisättävän kartan nimeä
 * `luku` - Edustaa lukua, johon kartta kuuluu. Kaikki lukutiedostot sijaitsevat VPK-tiedostossa lisäämällä kartan nimi muodossa `kartta karttasi_nimi`
 * Kuva - Se sisältää kartan pikkukuvan ja on tallennettu juuripolkuun steam\steamapps\common\portal\portal\materials\VGUI.
 * `Kommentti` - Kuvaava teksti luodusta kartasta.

## Viitteet

 * [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

