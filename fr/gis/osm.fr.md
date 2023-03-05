{
  "date" : "2019-10-11",
  "keywords" :[ "fichier osm", "qu'est-ce qu'un fichier osm", "fichier", "exemple osm", "extension de fichier osm","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - Format de fichier OpenStreetMap",
  "description":"En savoir plus sur le format de fichier OSM et les API qui peuvent créer et ouvrir des fichiers OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier OSM ?

OpenStreetMap (OSM) est une énorme collection de magasins d'informations géographiques volontaires dans différents types de fichiers, utilisant différents schémas de codage pour convertir ces données en bits et en octets. OSM est un effort de collaboration vers la création d'une carte modifiable gratuite du monde. Le résultat principal de cet effort de collaboration est constitué de données géographiques plutôt que de la carte elle-même. Les contraintes sur l'utilisation ou la disponibilité des informations géographiques dans une grande partie du monde déclenchent la nécessité de créer un OSM. Les données disponibles auprès d'OSM sont prêtes à remplacer Google Maps pour les applications classiques (Facebook, Craigslist, etc.) et les données par défaut pour les applications du récepteur GPS. source d'information.

## Bref historique ##

Inspiré par le succès de Wikipédia, en 2004, Steve Coast, un entrepreneur britannique, a créé ce projet communautaire de cartographie du monde au Royaume-Uni. Il s'est d'abord concentré sur la cartographie du Royaume-Uni. La Fondation OpenStreetMap a été créée en avril 2006 pour soutenir l'évolution, l'expansion et la circulation du géospatial gratuit pour tous. En décembre 2006, Yahoo a aidé OpenStreetMap avec sa photographie aérienne pour la production de cartes. Des données routières complètes pour les Pays-Bas et des données sur les routes principales pour l'Inde et la Chine ont été fournies à OSM en avril 2007 par Automotive Navigation Data (AND). En décembre 2007, l'Université d'Oxford était l'organisation la plus importante à avoir intégré les données OpenStreetMap dans son site Web principal. Depuis lors, plus de 2 millions d'utilisateurs enregistrés contribuent aux données de ce projet à l'aide d'appareils GPS, de photographies aériennes et de relevés manuels. Ces données fournies par la communauté sont mises à disposition sous la licence de base de données ouverte. Une organisation à but non lucratif enregistrée en Angleterre, OpenStreetMap Foundation, a géré le site OSM.

## Format de fichier OSM ##

Il existe de nombreuses façons et formats de fichiers pour stocker des données géographiques, mais le format de fichier **OSM** est limité à OpenStreetMap. OSM est un format standard spécialement conçu pour être transporté facilement sur Internet. Un format ordonné structuré, codé en XML constitue le fichier .osm. Dans OpenStreetMap, il existe quatre éléments pivots pour stocker la structure des données topologiques :

{{< figure src="../OSM.png" alt="Format de fichier OSM" >}}


|Nœuds|Chemins|Relations|Tags
---|---|---|---|
|<ul><li> Représente la position géographique stockée sous forme de paires d'une latitude et d'une longitude.</li><li> Utilisé pour représenter les entités cartographiques sans taille, telles que les sommets des montagnes.</li></ul> |<ul><li> Listes triées de nœuds, signifiant une polyligne ou un polygone</li><li> Représentez des éléments linéaires tels que des routes et des rivières, ainsi que des zones telles que des zones de stationnement, des jungles et des parcs.</li></ul> |<ul><li> Des listes triées de nœuds et de voies représentent leur relation comme des barrières et des virages en U sur les routes, les autoroutes couvrent différentes voies et zones existantes avec des trous.</li></ul> |<ul><li> Stockez les métadonnées sur les objets de la carte. * Toujours attaché à n'importe quel nœud, chemin ou relation</li></ul>


Les balises sont utilisées pour caractériser les caractéristiques physiques au sol (bâtiments et routes, etc.) dans OpenStreetMap. Chaque balise concerne une caractéristique géographique de l'entité représentée par ce nœud ou cette relation spécifique. Dans ce système de marquage gratuit, pour décrire une entité, un nombre illimité d'attributs peut être inclus dans une carte. Des combinaisons spécifiques de clé et de valeur approuvées par les utilisateurs enregistrés agissent comme des normes informelles pour les balises fréquemment utilisées. Cependant, de nouvelles balises peuvent être créées chaque fois que de nouveaux aspects nécessitent d'analyser des attributs précédemment non cartographiés des entités. La plupart des fonctionnalités n'utilisent qu'un petit nombre de balises pour la description.

Trois types de fichiers sont utilisés par OSM pour stocker ses principales données.

OSM gère tous ces fichiers avec les informations sur leurs détails de formatage. Mais les mêmes objets internes sont produits par ces fichiers. Pour les fichiers de données, le drapeau visible sur les objets OSM est toujours vrai, ce qui n'est pas le cas pour les fichiers d'historique et de modifications.

Dans l'usage courant, il existe une diversité de formats de fichiers OSM. Les formats de fichiers définissent l'encodage du contenu sur disque ou filaire en bits et octets. OSM est capable de lire et d'écrire le maximum de ces formats.

**XML**

Le format OSM d'origine est basé sur XML. Les données de retour de l'API principale de la base de données OSM sont au format XML.

**PBF**

L'encodage Protocol Buffers repose sur le format binaire et l'un des formats les plus compacts.

**O5M/O5C**

Format binaire basé sur un format plus simple mais relativement moins utilisé. OSM peut lire mais ne peut pas écrire ce format.

**OPL**

Un format simple proposé à utiliser avec les outils de ligne de commande UNIX standard. Proche des fichiers CSV, permet une entité OSM sur une ligne.

**DÉBOGUER**

Format textuel destiné à être créé pour le débogage. L'OSM peut écrire ce format mais ne peut pas le lire.

**TROU NOIR**

Un format factice qui dispose de toutes les données. L'OSM peut écrire ce format mais ne peut pas le lire.

## Stockage de données OSM ##

La base de données principale **PostgreSQL** d'OSM conserve la copie principale des données OSM avec l'extension PostGIS. Pour chaque primitive de données, la base de données principale maintient une table dont les lignes stockent des objets individuels. Toutes les modifications mettent à jour cette base de données et tous les autres formats sont formés à l'aide de cette base de données. De nombreux pools de bases de données téléchargeables sont créés pour transférer des données d'un endroit à un autre. Deux formats, l'un utilisant XML et l'autre utilisant le Protocol Buffer Binary Format (PBF) définissent ces pools. Les données complètes sont stockées dans un fichier appelé planet.osm

## Compression dans les fichiers OSM ##

Les formats textuels (XML, OPL et Debug) utilisent la compression gzip ou bzip2 en option.

## Références ##

* [Manuel des formats de fichiers OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Apprendre OSM](https://learnosm.org/en/osm-data/getting-data/)

