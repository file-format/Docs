{
  "date" : "2019-10-11",
  "keywords": [ "pdb file", "pdb", "extension", "format", "What is a pdb file", "pdb file format", "PDB metadata" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier PDB - Un fichier de base de données de programme",
  "description":"En savoir plus sur le format de fichier PDB et les API qui peuvent créer et ouvrir des fichiers PDB.",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier PDB ?

Un fichier avec l'extension .pdb est un fichier de base de données de programme qui contient des informations de débogage pour un exécutable compilé (EXE/DLL). Les fichiers PDB sont générés par les compilateurs Microsoft lorsqu'un programme d'application est compilé en mode débogage. La présence d'un fichier PDB peut aider à la rétro-ingénierie d'un exécutable car il contient des informations importantes sur tous les symboles des modules. C'est pour cette raison que ces fichiers sont séparés de l'exécutable final. L'[API DgbHelp] de Microsoft (https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) peut ouvrir un fichier PDB pour obtenir des informations telles que les publics et les exportations, les symboles globaux, les symboles locaux, données de type, fichiers source et numéros de ligne.

## Format de fichier APB

PDB est le format de fichier propriétaire de Microsoft et n'a encore été officiellement documenté nulle part. Cependant, une documentation de départ est disponible [ici](https://github.com/Microsoft/microsoft-pdb) et peut être référencée.

### Flux PDB

Les fichiers PDB se composent de plusieurs flux où chaque flux agit comme un fichier individuel virtuel et contient des informations. Les rédacteurs de fichiers PDB peuvent écrire dans ces fichiers et le fichier n'est finalisé qu'après l'émission d'une validation explicite. Un compilateur peut continuer à écrire dans un fichier PDB mais ne valider que si tout le code utilisateur se compile avec succès. Un fichier PDB se compose des flux suivants :

|Stream No. |Contenu |Brève description|
---|---|---|
|1| Pdb (en-tête) |Informations sur la version et informations pour connecter cette PDB à l'EXE|
|2| Tpi (Gestionnaire de types) |Tous les types utilisés dans l'exécutable.|
|3| Dbi (informations de débogage) |Contient les contributions de la section et la liste des 'Mods'|
|4| NomCarte| Contient une table de chaînes hachées |
|4-(n+4)| n Mod's (Informations sur le module)| Chaque flux Mod contient des symboles et des numéros de ligne pour un compiland |
|n+4| Hachage de symbole global | Un index qui permet de rechercher dans les symboles globaux par nom |
|n+5| Hachage de symbole public | Un index qui permet de rechercher dans les symboles publics par adresses |
|n+6| Enregistrements de symboles| Enregistrements de symboles réels des symboles mondiaux et publics |
|n+7| Tapez le hachage | Hachage utilisé par le flux TPI.|

Chaque flux d'un fichier PDB comprend plusieurs pages qui ne sont pas nécessairement numérotées consécutivement.

### En-tête de l'APB

Un fichier PDB est doté d'un en-tête qui consiste en une signature permettant d'identifier et de valider le format spécifique. La longueur de la signature dépend du format PDB. L'en-tête peut être plus long qu'une seule page.

### Métadonnées PDB
Les métadonnées PDB sont chargées de reconnaître tous les flux de composants, en indiquant la longueur et la séquence des pages pour chaque flux. Les ordres sont donnés aux flux consécutivement ; commençant par 0. Il existe également un flux racine non ordonné, qui contient certaines des métadonnées.

## Références
* [APB - Wikipédia](https://en.wikipedia.org/wiki/Program_database)
* [APB Microsoft](https://github.com/Microsoft/microsoft-pdb)

