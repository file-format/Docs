{
  "date" : "2021-03-30",
  "keywords" :[ "PMLZ", "Fichier Zipped Palm Markup Language", "extension", "Fichier", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier PMLZ, Palm Markup Language et les API qui peuvent créer et ouvrir des fichiers PMLZ.",
  "title" :"PMLZ - Fichier de langage de balisage Palm compressé",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Qu'est-ce qu'un fichier PMLZ ?

Palm Inc a introduit un type de fichier eBook ; connu sous le nom de format de fichier PMLZ qui est une version compressée du format de fichier [PML](/fr/ebook/pml/). C'est pourquoi les fichiers avec les extensions .pmlz sont connus sous le nom de **Zipped Palm Markup Language File**. Le fichier PMLZ est simplement un conteneur zip d'un fichier qui compile les fichiers [PDB](/fr/programming/pdb/) pour créer des documents pour **eReader** (connu comme un appareil de lecture d'ebook tel qu'une tablette). Le fichier PML donne la mise en page à un fichier PDB (contenant divers fichiers de données) à afficher sur un appareil Palm. Considérant qu'un fichier PDB est un fichier de base de données utilisé par diverses applications, notamment Quicken, Pegasus, Microsoft Visual Studio et Palm Pilot. En bref, un PMLZ est un conteneur compressé de fichiers PML et PDB.


## Connaissance du langage de balisage Palm
Le tableau suivant spécifie les commandes PML :

|Commande|Description|
---|---|
| \p | Nouvelle page |
| \x | Nouveau chapitre; provoque également un nouveau saut de page. Entourez le titre du chapitre (et tous les codes de style) avec \x et \x |
| \Xn | Nouveau chapitre, indenté de n niveaux (n compris entre 0 et 4 inclus) dans la boîte de dialogue Chapitre ; ne provoque pas de saut de page. Entourez le titre du chapitre (et tous les codes de style) avec \Xn et \Xn |
| \Cn="Titre du chapitre" | Insérez "Titre du chapitre" dans la liste des chapitres, avec le niveau n (comme \Xn). Le texte n'est pas affiché sur la page et ne force pas un saut de page. Cela peut parfois être utile pour insérer une marque de chapitre au début d'une introduction au chapitre, par exemple. |
| \c | Centrez ce bloc de texte ; fermer avec \c en début de ligne |
| \r | Bloc de texte justifié à droite ; fermer avec \r en début de ligne |
| \i | Mettre le bloc en italique ; fermer avec \i |
| \u | Bloc de soulignement ; fermer avec \u |
| \o | Blocage Overstrike ; fermer avec \o |
| | Texte invisible ; fermer avec \v (peut être utilisé pour les commentaires) |
| \t | Bloc d'indentation. Commencer au début d'une ligne, terminer avec \t en fin de ligne |
| \T="50%" | Indente le pourcentage spécifié de la largeur de l'écran, 50 % dans ce cas. Si la position de dessin actuelle dépasse déjà l'emplacement d'écran spécifié, cette balise est ignorée. |
| \w="50%" | Incorporer une règle horizontale d'un pourcentage donné de la largeur de l'écran, dans ce cas 50 %. Cette balise provoque un saut de ligne avant et après. La règle est centrée. Le signe pourcentage est obligatoire. |
| \n | Passez à la police "normale", qui est spécifiée par l'utilisateur |
| \s | Passez à stdFont ; fermer avec \s pour revenir à la police normale |
| \b | Passez à boldFont ; fermez avec \b pour revenir à la police normale (obsolète ; utilisez \B à la place) |
| \l | Passez à largeFont ; fermer avec \l pour revenir à la police normale |
| \B | Marquez le texte en gras. Contrairement à la balise \b, \B ne change pas la police, vous pouvez donc avoir un gros texte en gras. Vous ne pouvez pas mélanger \b et \B dans le même fichier PML. |
| \Sp | Marquer le texte en exposant. Ne doit pas être mélangé avec d'autres styles tels que gras, italique, etc. Placez le texte en exposant avec \Sp. |
| \Sb | Marquer le texte en indice. Ne doit pas être mélangé avec d'autres styles tels que gras, italique, etc. Entourez le texte en indice avec \Sb. |
| \k | Transformez le texte inclus en petites majuscules ; fermez avec \k. Tous les caractères inclus dans les balises \k (y compris ceux avec des accents) sont mis en majuscule et sont rendus avec une taille en points plus petite qu'un caractère majuscule normal. |
| \\ | Représente une seule barre oblique inverse |
| \aXXX | Insérez un caractère non ASCII dont le code Windows-1252 est décimal XXX. Voir la table des caractères PML pour plus de détails. |
| \UXXXX | Insérer un caractère non ASCII dont le code Unicode est XXXX hexadécimal. Voir le tableau des caractères PML étendu pour plus de détails. |
| \m="nomimage.png" | Insérez l'image nommée. Voir la section sur les images ci-dessous. |
| \q="#linkanchor"Du texte\q | Référencez une ancre de lien qui se trouve à un autre endroit du document. La chaîne après la spécification de l'ancre et avant le \q de fin est soulignée ou autrement indiquée comme un lien lors de l'affichage du document. |
| \Q="lienancre" | Spécifiez une ancre de lien dans le document. |
| \- | Insérez un trait d'union souple. Un trait d'union souple n'apparaît que s'il est nécessaire de couper un mot sur une ligne. |
| \Fn="footnote1"1\Fn | Liez le "1" à une note de bas de page dont le nom est footnote1, étiqueté à la fin du document PML. Voir la section sur les notes de bas de page et les encadrés ci-dessous. |
| \Sd="sidebar1"Barre latérale\Sd | Liez le texte "Sidebar" à une barre latérale dont le nom est sidebar1, étiqueté à la fin du document PML. Voir la section sur les notes de bas de page et les encadrés ci-dessous. |
| \Je | Marquer comme élément d'index de référence. Entourez l'élément d'index (et tous les codes de style) avec \I et \I.|


## Références

* [Langage de balisage Palm - Par MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader - Par MobileRead](https://en.wikipedia.org/wiki/E-reader)

