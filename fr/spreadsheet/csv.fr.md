{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "fichier", "extension", "format de fichier", "Valeurs séparées par des virgules", "Feuille de calcul" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier CSV et les API qui peuvent créer et ouvrir des fichiers CSV.",
  "title" :"Format de fichier CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Qu'est-ce qu'un fichier CSV ?

Les fichiers avec l'extension .csv (Comma Separated Values) représentent des fichiers en texte brut qui contiennent des enregistrements de données avec des valeurs séparées par des virgules. Chaque ligne d'un fichier CSV est un nouvel enregistrement de l'ensemble d'enregistrements contenus dans le fichier. De tels fichiers sont générés lorsque le transfert de données est prévu d'un système de stockage à un autre. Étant donné que toutes les applications peuvent reconnaître les enregistrements séparés par des virgules, l'importation de ces fichiers de données dans la base de données se fait de manière très pratique. Presque toutes les applications de tableur telles que Microsoft Excel ou OpenOffice Calc peuvent importer du CSV sans trop d'effort. Les données importées à partir de ces fichiers sont disposées dans des cellules d'une feuille de calcul pour être présentées à l'utilisateur.

## Bref historique ##

Voici quelques faits rapides sur l'origine et l'histoire du format de fichier CSV.

* 1972 - Le compilateur IBM Fortran (niveau H étendu) les supporte sous OS/360

* 1978 - L'entrée/sortie dirigée par liste était prise en charge par FORTRAN 77 qui utilisait des virgules et des espaces pour les délimiteurs

* 2005 - CSV a été normalisé avec [RFC4180](https://tools.ietf.org/html/rfc4180) comme type de contenu MIME.

* 2013 - Les lacunes de la RFC4180 ont été traitées par une recommandation du W3C

* 2015 - Le W3C a rédigé les premières ébauches de recommandations pour les normes de métadonnées CSV, qui ont commencé comme recommandation en décembre 2015

## Convertir les fichiers CSV ##

Les fichiers CSV peuvent être convertis en plusieurs formats de fichiers différents à l'aide des applications qui peuvent ouvrir ces fichiers. Par exemple, Microsoft Excel peut importer des données à partir du format de fichier CSV et les enregistrer au format XLS, [XLSX](/fr/spreadsheet/xlsx/), [PDF](/fr/pdf/), [TXT](/fr/word-processing/txt/) , XML et [HTML](/fr/web/html/). De même, d'autres services de bureau ainsi que des services en ligne offrent la possibilité d'exporter des fichiers CSV vers HTML, ODS et [RTF](/fr/word-processing/rtf/).

## Format de fichier CSV ##

Le format de fichier CSV est connu pour être spécifié sous [RFC4180](https://tools.ietf.org/html/rfc4180). Il définit tout fichier comme étant compatible CSV si :

* Chaque enregistrement est situé sur une ligne distincte, délimitée par un saut de ligne (CRLF). Par exemple:
* aaa, bbb, ccc CRLF
* zzz,aaa,xxx CRLF
* Le dernier enregistrement du fichier peut avoir ou non un saut de ligne de fin. Par exemple:
* aaa, bbb, ccc CRLF
* zzz, aaa, xxx
* Il peut y avoir une ligne d'en-tête facultative apparaissant comme première ligne du fichier avec le même format que les lignes d'enregistrement normales. Cet en-tête contiendra les noms correspondant aux champs du fichier et devra contenir le même nombre de champs que les enregistrements du reste du fichier (la présence ou l'absence de la ligne d'en-tête devra être indiquée via le paramètre optionnel "en-tête" de ce type MIME). Par exemple:
* nom_champ, nom_champ, nom_champ CRLF
* aaa, bbb, ccc CRLF
* zzz,aaa,xxx CRLF
* Dans l'en-tête et chaque enregistrement, il peut y avoir un ou plusieurs champs, séparés par des virgules. Chaque ligne doit contenir le même nombre de champs dans tout le fichier. Les espaces sont considérés comme faisant partie d'un champ et ne doivent pas être ignorés. Le dernier champ de l'enregistrement ne doit pas être suivi d'une virgule. Par exemple:
* aaa, bbb, ccc
* Chaque champ peut ou non être entouré de guillemets doubles (cependant, certains programmes, tels que Microsoft Excel, n'utilisent pas du tout les guillemets doubles). Si les champs ne sont pas entourés de guillemets doubles, les guillemets doubles peuvent ne pas apparaître à l'intérieur des champs. Par exemple:\
* "aaa","bbb","ccc" CRLF
* zzz, aaa, xxx
* Les champs contenant des sauts de ligne (CRLF), des guillemets doubles et des virgules doivent être placés entre guillemets doubles. Par exemple:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz, aaa, xxx
* Si des guillemets doubles sont utilisés pour délimiter des champs, alors un guillemet double apparaissant à l'intérieur d'un champ doit être échappé en le faisant précéder d'un autre guillemet double. Par exemple:
* "aaa","b""bb","ccc"

Cependant, à la lumière de l'usage moderne, le délimiteur n'est pas limité à la virgule et peut également être un point-virgule, une tabulation ou des espaces. Des applications telles que Microsoft Excel offrent la possibilité de spécifier le caractère délimiteur pour importer des enregistrements à partir d'un fichier CSV.

## Références

* [RFC4180](https://tools.ietf.org/html/rfc4180)
* [RFC2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipédia](https://en.wikipedia.org/wiki/Comma-separated_values)

