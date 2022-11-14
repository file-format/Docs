{
  "date" : "2021-10-20",
  "keywords" :[ "fichier bns", "format de fichier bns", "qu'est-ce qu'un fichier bns", "fichier", "exemple bns", "Extension de fichier Portal Bonus Map Script","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier ortal Bonus Map Script BNS et les API qui peuvent créer et ouvrir des fichiers BNS.",
  "title" :"BNS - Fichier de script de carte de bonus de portail",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Qu'est-ce qu'un fichier BNS ?

Un fichier avec l'extension .bns est un fichier de script de jeu créé avec le jeu de résolution de casse-tête Portal Map développé par Valve. Il contient un script de texte pour définir des informations sur une carte de portail qui est stockée sous forme de fichier .bsp. Les fichiers BNS sont utilisés comme référence à ce fichier de carte réel et contiennent une liste de défis à relever. En outre, il contient le nom de la carte, des commentaires sur la carte et des références de fichier d'image miniature. Un fichier BNS peut être ouvert dans n'importe quel éditeur de texte tel que Notepad++, textEdit et Notepad.

## Format de fichier BNS

Les fichiers BNS sont enregistrés sous forme de fichiers texte brut lisibles par l'homme. Ceux-ci peuvent être ouverts dans des éditeurs de texte et modifiés également. Cependant, ceux-ci doivent être soigneusement modifiés pour éviter toute erreur dans le script.

## Exemple de format de fichier BNS

Un fichier BNS peut ressembler à ce qui suit lorsqu'il est ouvert dans un éditeur de texte tel que Notepad++.

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

## Parties d'un fichier BNS

Dans l'exemple ci-dessus,

* `#Bonus_Map_Challenges` - Représente le nom de la carte.
* `map` - Représente le nom de la carte à mettre dans le dossier des cartes du jeu
* `chapter` - Représente le chapitre auquel appartient la carte. Tous les fichiers de chapitre sont localisés dans le fichier VPK en ajoutant le nom de la carte au format `map your_map_name`
* `Image` - Il contient la vignette de la carte et est stocké dans le chemin racine steam\steamapps\common\portal\portal\materials\VGUI.
* `Commentaire` - Texte descriptif de la carte créée.

## Références

* [Script du défi du portail](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

