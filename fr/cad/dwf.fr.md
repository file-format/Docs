{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Format de fichier", "Ouvrir", "Lire", "Créer", "CAO" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier DWF et les API permettant de créer et d'ouvrir des fichiers DWF.",
  "title" :"Format de fichier DWF",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier DWF ?

Design Web Format (DWF) représente un dessin 2D/3D dans un format compressé pour l'affichage, la révision ou l'impression de fichiers de conception. Il contient des graphiques et du texte dans le cadre des données de conception et réduit la taille du fichier en raison de son format compressé. La taille réduite du fichier rend efficace la distribution et la communication de données de conception riches. DWF n'exige pas que le destinataire connaisse l'utilisation du logiciel de CAO qui a créé le dessin d'origine. Le contenu du format de fichier DWF peut être simple et inclure une seule feuille ou suffisamment complexe pour contenir des polices, des couleurs et des images.

## Bref historique ##

Autodesk a introduit le format de fichier DWF en 1995 dans le cadre du plug-in Netscape Navigation, WHIP. Le format a évolué du format 2D uniquement pour inclure des contenus 3D au fil du temps. De nombreuses applications tierces utilisent également ce format.

## Format de fichier DWF ##

DWF est un format ouvert et sécurisé conçu spécifiquement pour le partage de données de conception technique riches. Il est indépendant du logiciel d'application, du matériel et du système d'exploitation d'origine utilisés pour créer ces données de conception. Cela permet aux membres de l'équipe qui n'utilisent pas d'applications de CAO de participer aux processus numériques en visualisant les conceptions de bâtiments, de SIG ou de produits. Une archive de fichier DWF se compose de plusieurs fichiers XML et binaires regroupés dans une archive compressée créée avec la compression [ZIP](/fr/compression/zip/). Vous pouvez renommer une extension de fichier DWF en ZIP et afficher le contenu du fichier. Le package DWF peut contenir de nombreux types de données de conception, telles que des graphiques 2D, des graphiques 3D, des métadonnées de package et de section et d'autres fichiers de ressources.

**Fichiers de métadonnées DWF** – Fichiers XML contenant des informations relatives aux métadonnées et à la structure (auteur, titre, heure de création, dépendances de section, ordre des sections, descriptions des fichiers de ressources, rôles, types mime, etc.) et relatives à la section (page informations, métadonnées de conception, etc.). Les métadonnées structurelles sont utilisées pour créer des objets logiques (collections de fichiers pour représenter une partie ou une page, etc.).

**Fichiers de ressources** : fichiers multimédias ou autres fichiers de contenu référencés à partir des métadonnées du package/de la section et qui sont généralement des présentations de données de conception dans différents formats (ZGL, W2D, [JPG](/fr/image/jpeg/), [PNG] (/fr/image/png/), AVI, XML, [TXT](/fr/word-processing/txt/), [DOC](/fr/word-processing/doc/), etc.)

### Détails du format de fichier ###

Les fichiers DWF sont organisés en trois sections principales, comme indiqué ci-dessous.

* En-tête d'identification de fichier
* Bloc de données de fichier
* Remorque de fin de fichier

#### En-tête d'identifiant de fichier ####

L'en-tête de l'identificateur de fichier permet l'identification des fichiers DWF par les applications. Il identifie également la version des spécifications DWF utilisée pour encoder le fichier. Il s'agit d'un en-tête de 12 octets organisé comme suit :


|Octet|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Caractère|(|D|W|F|(espace)|V|0|0|.|3|0|)

Voici un résumé de ce tableau :

* Les six premiers octets de l'en-tête représentent toujours les caractères ASCII "(DWF V"
* Les 5 octets suivants contiennent des informations sur le numéro de version, par exemple "00.30" avec la valeur de version majeure et mineure du format

Les applications créant un fichier DWF doivent spécifier le numéro de version le plus bas possible qu'une application de lecteur doit prendre en charge pour utiliser correctement les données.

#### Bloc de données de fichier ####

Le bloc de données de fichier commence au 13e octet d'un fichier DWF et est une série de paires d'opcodes et d'opérandes, comme dans le tableau suivant.

|Champ 1|Champ 2|Champ 3|Champ 4|Champ 5|Champ 5
--- | --- |--- | --- |--- | --- |
|opcode|opérande|opcode|opérande|opcode|opérande

Un fichier DWF peut contenir des paires opcode-opérande au format ASCII lisible ainsi qu'un code binaire ou un mélange des deux. Toutes les opérations DWF ont une forme d'opcode/opérande ASCII lisible, et la plupart des opérations ont également une forme d'opcode/opérande binaire codée. Les opcodes sont en un seul octet permettant plus de 200 opérations. L'ASCII étendu et le binaire étendu sont des cas exceptionnels. Les valeurs des Opcodes peuvent aller de 0 à 255 à quelques exceptions près. À l'exception des deux types spéciaux d'opcodes ASCII étendu et binaire étendu, un lecteur de fichier doit savoir comment calculer la longueur de l'opérande.

##### Opcodes interdits #####

Les représentations ASCII des éléments suivants ne peuvent pas être utilisées comme opcodes :

Les représentations ASCII suivantes ne peuvent pas être utilisées comme opcodes :

* Espace (0x20)
* Onglet (0x09)
* Trait d'union (0x2D)
* Chiffres ASCII 0-9 (0x30 - 0x39)
* Retour chariot (0x0D)
* Alimentation de ligne (0x0A)
* Guillemets simples (0x27)
* Guillemet double (0x22)
* Période (0x2E)
* Parenthèse (0x28 et 0x29)
* Accolades (0x7B et 0x7D)
* Crochets (0x5B et 0x5D)
* Barre oblique inversée (0x5C)

#### Remorque de fin de fichier ####

La bande-annonce de fin de fichier pour DWF est simplement un code opération spécial indiquant la fin du fichier. Certaines applications peuvent stocker des données non DWF après l'opcode de terminaison. La bande-annonce est comme illustré ci-dessous :


|Octet|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Caractère|(|E|n|d|0|f|D|W|F|)

## Références ##

* [DWF - Par Wikipédia](https://en.wikipedia.org/wiki/Design_Web_Format)
* [Format de données WHIP](http://paulbourke.net/dataformats/whip/)
* [http://blogs.msdn.com/opc/archive/2009/05/18/adventures-in-packaging-episode-1.aspx](http://blogs.msdn.com/opc/archive/2009 /18/05/aventures-dans-l-emballage-episode-1.aspx)

