{
  "date" : "2021-10-20",
  "keywords" :[ "file bns", "formato file bns", "cos'è un file bns", "file", "esempio bns", "estensione file Portal Bonus Map Script", "estensione", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file BNS di Ortal Bonus Map Script e le API che possono creare e aprire file BNS.",
  "title" :"BNS - File script mappa bonus portale",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Che cos'è un file BNS?

Un file con estensione .bns è un file di script di gioco creato con il gioco di risoluzione dei puzzle Portal Map sviluppato da Valve. Contiene uno script di testo per definire le informazioni su una mappa del portale che è memorizzata come file .bsp. I file BNS vengono utilizzati come riferimento a questo file di mappa effettivo e contengono un elenco di sfide che devono essere completate. Inoltre, contiene il nome della mappa, commenti sulla mappa e riferimenti ai file di immagine in miniatura. Un file BNS può essere aperto in qualsiasi editor di testo come Notepad++, textEdit e Blocco note.

## Formato file BNS

I file BNS vengono salvati come file di testo semplice leggibili dall'uomo. Questi possono essere aperti in editor di testo e modificati. Tuttavia, questi dovrebbero essere modificati con attenzione per evitare errori nello script.

## Esempio di formato file BNS

Un file BNS può avere un aspetto simile al seguente quando viene aperto in un editor di testo come Notepad++.

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

## Parti di un file BNS

Nell'esempio sopra,

* `#Bonus_Map_Challenges` - Rappresenta il nome della mappa.
* `mappa` - Rappresenta il nome della mappa da inserire nella cartella delle mappe del gioco
* `capitolo` - Rappresenta il capitolo a cui appartiene la mappa. Tutti i file dei capitoli si trovano nel file VPK aggiungendo il nome della mappa nel formato `map your_map_name`
* `Image` - Contiene la miniatura della mappa ed è memorizzata nel percorso principale steam\steamapps\common\portal\portal\materials\VGUI.
* `Commento` - Testo descrittivo sulla mappa creata.

## Riferimenti

* [Script Portal Challenge](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

