{
  "date" : "2019-10-11",
  "keywords" :[ "fichier rtf", "format de fichier rtf", "qu'est-ce qu'un fichier rtf", "fichier", "exemple rtf", "extension de fichier rtf","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Format de texte enrichi",
  "description":"En savoir plus sur le format de fichier RTF et les API qui peuvent créer et ouvrir des fichiers RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier RTF ?

Introduit et documenté par Microsoft, le format RTF (**RTF**) représente une méthode de codage de texte et de graphiques formatés à utiliser dans les applications. Le format facilite l'échange de documents entre plates-formes avec d'autres produits Microsoft, servant ainsi l'objectif d'interopérabilité. Cette capacité en fait une norme de transfert de données entre les logiciels de traitement de texte et, par conséquent, le contenu peut être transféré d'un système d'exploitation à un autre sans perdre le formatage du document. Les spécifications de format de fichier sont disponibles par Microsoft pour [téléchargement] public(https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) et peuvent être consultées du point de vue du développeur.

## Bref historique du format de fichier RTF ##

Le format de fichier RTF a subi plusieurs révisions depuis sa publication. Sa version officielle en lecture/écriture a été publiée dans le cadre de Microsoft Word 3.0 pour Macintosh avec les spécifications de la version 1.0. La version finale des spécifications, 1.9.1, a été publiée par Microsoft en mars 2008. Aucune autre amélioration des spécifications n'est apportée par la suite. À l'heure actuelle, presque tous les systèmes d'exploitation ont des applications plus riches en fonctionnalités qui ont minimisé/éradiqué l'utilisation du format de fichier RTF.

## Spécifications du format de fichier RTF ##

RTF sert de norme de transfert de données entre les logiciels de traitement de texte et de transfert de contenu d'un système d'exploitation à un autre. Ceci est réalisé en utilisant des mots de contrôle qui ont été introduits par Microsoft Office Word jusqu'en 2007. Un fichier RTF standard se compose d'ASCII pour représenter du texte enrichi et de caractères non ASCII qui sont convertis en valeurs de code appropriées. Les versions plus récentes de Word peuvent lire les fichiers RTF générés avec les versions précédentes, tandis que les anciennes versions ignorent les mots de contrôle et les groupes qu'elles ne comprennent pas.

### Comprendre les fondements du RTF ###

Les fichiers RTF utilisent du texte brut ASCII 7 bits, composé de :

* mots de contrôle
* symboles de contrôle, et
* groupes.

Ceux-ci agissent comme des blocs de construction pour la représentation des données RTF sous forme de texte compréhensible et d'encodage de caractères.

#### Mot de contrôle ####

Celles-ci représentent une commande spécialement formatée utilisée pour marquer les caractères à afficher et ne peuvent pas dépasser 32 lettres. Un mot de contrôle est défini par :

\<ASCII Letter Sequence> //<//Delimiter//> //

Chaque mot de contrôle est sensible à la casse et commence par une barre oblique inverse. La séquence de lettres ASCII peut contenir des alphabets ASCII (a à z et A à Z). La<Delimite> marque la fin du nom du mot de contrôle et peut être l'un des suivants :

* Un espace. Celui-ci sert uniquement à délimiter un mot de contrôle et est ignoré lors du traitement ultérieur.
* Un chiffre numérique ou un signe moins ASCII, qui indique qu'un paramètre numérique est associé au mot de contrôle. La séquence numérique suivante est alors délimitée par n'importe quel caractère autre qu'un chiffre ASCII (généralement un autre mot de contrôle qui commence par une barre oblique inverse). Le paramètre peut être un nombre décimal positif ou négatif. La plage des valeurs pour le nombre est nominalement –32768 à 32767, c'est-à-dire un entier signé de 16 bits. Un petit nombre de mots de contrôle prend des valeurs comprises entre -2 147 483 648 et 2 147 483 647 (entier signé 32 bits). Ces mots de contrôle incluent **\binN**, **\revdttmN//**, **\rsidN** mots de contrôle associés et certaines propriétés d'image comme **\bliptagN**. Ici **N** représente le paramètre numérique. Un analyseur RTF doit autoriser jusqu'à 10 chiffres éventuellement précédés d'un signe moins. Si le délimiteur est un espace, il est ignoré, c'est-à-dire qu'il n'est pas inclus dans le traitement ultérieur.
* Tout caractère autre qu'une lettre ou un chiffre. Dans ce cas, le caractère de délimitation termine le mot de contrôle et ne fait pas partie du mot de contrôle. Comme une barre oblique inverse "\", ce qui signifie qu'un nouveau mot de contrôle ou un symbole de contrôle suit.

#### Symbole de contrôle ####

Un symbole de contrôle représente une occurrence spéciale qui a une signification spécifique en fonction de son contenu. Il se compose d'une barre oblique inverse suivie d'un caractère spécial (caractère non alphabétique) et n'a pas de délimiteurs.

#### Groupe ####

Un groupe peut être constitué de texte, de mots de contrôle ou de symboles de contrôle entre accolades (**{ }**). L'accolade ouvrante (**{** ) indique le début du groupe et l'accolade fermante ( **}**) indique la fin du groupe. Chaque groupe spécifie le texte affecté par le groupe et les différents attributs de ce texte.

### Structure du fichier RTF ###

Un fichier RTF a la syntaxe standard suivante :

Introduit et documenté par Microsoft, le format RTF (**RTF**) représente une méthode de codage de texte et de graphiques formatés à utiliser dans les applications. Le format facilite l'échange de documents entre plates-formes avec d'autres produits Microsoft, servant ainsi l'objectif d'interopérabilité. Cette capacité en fait une norme de transfert de données entre les logiciels de traitement de texte et, par conséquent, le contenu peut être transféré d'un système d'exploitation à un autre sans perdre le formatage du document. Les spécifications de format de fichier sont disponibles par Microsoft pour [téléchargement] public(https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) et peuvent être consultées du point de vue du développeur.

#### En-tête RTF ####

Un en-tête RTF a la représentation suivante.

|Champ|Description
---|---|
|\<header> |**\rtf1\fbidis** ? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Les tables d'en-tête doivent apparaître dans cet ordre si elles existent. Le fichier RTF peut inclure des groupes pour les polices, les styles, la couleur de l'écran, les images, les notes de bas de page, les commentaires (annotations), les en-têtes et les pieds de page, les informations récapitulatives, les champs, les signets, les propriétés de formatage des documents, des sections, des paragraphes et des caractères, les mathématiques, images et objets. Si la police, le fichier, le style, la couleur, la marque de révision et les groupes d'informations récapitulatives et les propriétés de mise en forme du document sont inclus dans le fichier, ils doivent apparaître dans l'en-tête RTF, qui précède le corps RTF. Si le contenu d'un groupe n'est pas utilisé, le groupe peut être omis. Tout groupe qui utilise les propriétés définies dans un autre groupe doit apparaître après le groupe qui définit ces propriétés. Par exemple, les propriétés de couleur et de police doivent précéder le groupe de style.

#### Version RTF ####

Un document RTF doit commencer par ces six caractères :

```
{\rtf1
```
où le 1 indique le numéro de version RTF.

#### Jeu de caractères ####

Après le {\rtf1, le document doit déclarer quel jeu de caractères il utilise. La façon de déclarer un jeu de caractères est avec l'une de ces commandes :

`\ansi` - Le document est dans le jeu de caractères ANSI, également connu sous le nom de page de codes 1252, le jeu de caractères MSWindows habituel.

`\mac` - Le document est dans le jeu de caractères MacAscii, le jeu de caractères habituel sous les anciennes versions (pré-10) de Mac OS.

`\pc` - Le document est en page de code DOS 437, le jeu de caractères par défaut pour MS-DOS. Les dactylographes avec une bonne mémoire musculaire remarqueront que c'est le jeu de caractères qui est encore utilisé pour interpréter les codes "Alt numériques" - c'est-à-dire que lorsque vous maintenez la touche Alt enfoncée et tapez "130" sur le pavé numérique, il produit un é, car le caractère 130 dans CP437 est un é. C'est à peu près la seule utilisation que CP437 voit de nos jours.

`\pca` - Le document est dans la page de code DOS 850, également connue sous le nom de page de code multilingue MS-DOS.

#### Commande de police ####

La définition du jeu de caractères est suivie de la commande `\deffN`. Cela définit que le numéro de police N est la police par défaut pour ce document. Le numéro de police N est référé à partir de la table des polices. La commande `\deffN` est techniquement facultative, mais elle devrait être là pour être du bon côté en tant que prologue commun comme suit choisit la police 0 comme police par défaut.

`{\rtf1\ansi\deff0`

#### Tableau des polices ####

Toutes les polices pouvant être utilisées dans un document sont répertoriées dans un tableau des polices où chaque police est représentée par un numéro de police. Le document doit avoir une table de polices bien que certains programmes fonctionnent également sans cela.

La syntaxe d'une table de polices est {\fonttbl //...declarations//...}, dans laquelle chaque déclaration a cette syntaxe de base :

`{\fnumber\familycommand Nom de la police ;}`

Une table de polices avec quatre déclarations est la suivante :

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Dans un document avec cette table de polices, `{\f2 stuff}` imprimerait "stuff" dans Courier New. Une police ne peut pas être utilisée dans un document tant qu'elle n'est pas répertoriée dans le tableau des polices.

### Fin du document ###

Chaque document RTF doit se terminer par un }, pour fermer le groupe ouvert par le { qui est le premier caractère du document. Rien ne peut suivre le } final, sauf éventuellement une nouvelle ligne.

## Références ##

* [Spécifications RTF 1.9.1](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)
* [Format de texte enrichi](https://en.wikipedia.org/wiki/Rich_Text_Format)

