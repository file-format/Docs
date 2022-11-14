{
  "date" : "2021-06-24",
  "keywords" :[ "fichier bat", "qu'est-ce qu'un fichier bat", "fichier", "exemple de fichier bat", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier BAT et les API qui peuvent créer et ouvrir des fichiers BAT.",
  "title" :"BAT - Format de fichier par lots",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Qu'est-ce qu'un fichier BAT ?
Un fichier BAT est connu comme un fichier de commandes exécuté avec DOS et toutes les versions de Windows, sous cmd.exe. Il se compose d'une série de commandes de ligne en texte brut à exécuter par l'interpréteur de ligne de commande pour effectuer différentes tâches, telles que l'exécution d'utilitaires de maintenance dans Windows ou le démarrage de programmes typiques. Un fichier de commandes peut inclure n'importe quelle commande pouvant être acceptée par l'interpréteur de manière interactive et utiliser la structure de code qui permet le branchement et la boucle conditionnels tels qu'ils sont écrits dans le fichier de commandes.
## Format de fichier BAT
Un format de fichier BAT est simplement un script incorporé pour automatiser les séquences de commandes qui sont de nature répétitive. Le terme "batch" est utilisé pour le traitement par lots, il peut être considéré comme une "exécution non interactive". Par conséquent, un fichier de commandes peut ne pas traiter un lot de plusieurs données. Dans l'ancien système d'exploitation de disque (DOS), le fichier de commandes était exécuté sous l'interface de ligne de commande en tapant le nom de fichier et l'extension .bat. L'ancien système d'exploitation basé sur l'interface graphique de Microsoft, tel que Microsoft Windows, dépendait de DOS. Les utilisateurs devaient utiliser DOS pour effectuer des opérations typiques comme la réparation, l'optimisation ou la réinstallation de Windows. Plus tard, Microsoft a introduit Windows NT qui ne dépendait pas du système d'exploitation DOS. Par conséquent, les fichiers de commandes peuvent être exécutés à l'aide de l'invite de commande ou de ** cmd.exe ** dans les systèmes d'exploitation Microsoft modernes.
### Paramètres du fichier batch
L'invite de commande prend en charge un certain nombre de variables spéciales telles que **%0, %1 à %9** afin de faire référence au nom et au chemin du travail par lots et aux neuf paramètres d'appel depuis le travail par lots. Les paramètres inexistants sont remplacés par une chaîne de longueur nulle. Cependant, ils peuvent être utilisés de la même manière que les variables d'environnement, mais ne sont pas enregistrés dans l'environnement. Microsoft et IBM se réfèrent à ces variables comme des paramètres de remplacement, tandis que Novell, Digital Research et Caldera ont introduit le terme variables de remplacement pour eux.

Voici quelques commandes de fichiers batch utiles :
| Commande | Descriptif |
------|------------|
| VER | Cette commande batch affiche la version de MS-DOS que vous utilisez. |
|ASSOC| Il s'agit d'une commande batch qui associe une extension à un type de fichier (FTYPE), affiche les associations existantes ou supprime une association. |
|CD| Cette commande batch aide à apporter des modifications à un répertoire différent ou affiche le répertoire actuel. |
|CLS| Cette commande par lots efface l'écran. |
|COPIER| Cette commande batch est utilisée pour copier des fichiers d'un emplacement à l'autre. |
|SUPPR| Cette commande batch supprime les fichiers et non les répertoires. |
|DIR| Cette commande batch liste le contenu d'un répertoire. |
|DATE| Cette commande batch aide à trouver la date système. |
|ÉCHO| Cette commande batch affiche des messages ou active ou désactive l'écho des commandes. |
|SORTIR| Cette commande batch quitte la console DOS. |
|MD| Cette commande batch crée un nouveau répertoire à l'emplacement actuel. |
|DEPLACER| Cette commande par lots déplace des fichiers ou des répertoires entre des répertoires. |
|CHEMIN| Cette commande batch affiche ou définit la variable de chemin. |
|PAUSE| Cette commande par lots invite l'utilisateur et attend qu'une ligne d'entrée soit saisie. |
|INVITE| Cette commande batch peut être utilisée pour modifier ou réinitialiser l'invite cmd.exe. |
|RD| Cette commande batch supprime les répertoires, mais les répertoires doivent être vides avant de pouvoir être supprimés. |
|REN| Renomme les fichiers et les répertoires |
|REM| Cette commande batch est utilisée pour les remarques dans les fichiers batch, empêchant l'exécution du contenu de la remarque. |
|DÉBUT| Cette commande batch démarre un programme dans une nouvelle fenêtre ou ouvre un document. |
|HEURE| Cette commande batch définit ou affiche l'heure. |
|TYPE| Cette commande batch imprime le contenu d'un ou plusieurs fichiers sur la sortie. |
|VOL| Cette commande batch affiche les étiquettes de volume. |
|ATTRIB| Affiche ou définit les attributs des fichiers dans le répertoire courant |
|CHKDSK| Cette commande batch vérifie le disque pour tout problème. |
|CHOIX| Cette commande batch fournit une liste d'options à l'utilisateur. |
|CMD| Cette commande batch appelle une autre instance de l'invite de commande. |
|COMP| Cette commande batch compare 2 fichiers en fonction de la taille du fichier. |
|CONVERTIR| Cette commande batch convertit un volume du système de fichiers FAT16 ou FAT32 en système de fichiers NTFS. |
|REQUETECONDUCTEUR| Cette commande batch affiche tous les pilotes de périphériques installés et leurs propriétés. |
|ÉTENDRE| Cette commande batch extrait les fichiers des fichiers CAB .cab compressés. |
|TROUVER| Cette commande par lots recherche une chaîne dans les fichiers ou l'entrée, en affichant les lignes correspondantes. |
|FORMAT| Cette commande par lots formate un disque pour utiliser le système de fichiers pris en charge par Windows tel que FAT, FAT32 ou NTFS, écrasant ainsi le contenu précédent du disque. |
|AIDE| Cette commande batch affiche la liste des commandes fournies par Windows. |
|IPCONFIG| Cette commande par lots affiche la configuration IP de Windows. Affiche la configuration par connexion et le nom de cette connexion. |
|ÉTIQUETTE| Cette commande batch ajoute, définit ou supprime une étiquette de disque. |
|PLUS| Cette commande batch affiche le contenu d'un ou plusieurs fichiers, un écran à la fois. |
|NET| Fournit divers services réseau, selon la commande utilisée. |
|PING| Cette commande par lots envoie des paquets "écho" ICMP/IP sur le réseau à l'adresse désignée. |
|ARRÊT| Cette commande par lots arrête un ordinateur ou déconnecte l'utilisateur actuel. |
|TRI| Cette commande batch prend l'entrée d'un fichier source et trie son contenu par ordre alphabétique, de A à Z ou de Z à A. Elle imprime la sortie sur la console. |
|SUBST| Cette commande par lots attribue une lettre de lecteur à un dossier local, affiche les affectations actuelles ou supprime une affectation. |
|INFOSSYSTÈME| Cette commande batch affiche la configuration d'un ordinateur et de son système d'exploitation. |
|TASKILL| Cette commande batch met fin à une ou plusieurs tâches. |
|LISTE DE TÂCHES| Cette commande batch répertorie les tâches, y compris le nom de la tâche et l'ID de processus (PID). |
|XCOPIER| Cette commande batch copie les fichiers et les répertoires de manière plus avancée. |
|ARBRE| Cette commande batch affiche une arborescence de tous les sous-répertoires du répertoire courant à n'importe quel niveau de récursivité ou de profondeur. |
|FC |Cette commande batch répertorie les différences réelles entre deux fichiers. |
|DISKPART |Cette commande batch affiche et configure les propriétés des partitions de disque. |
|TITLE |Cette commande batch définit le titre affiché dans la fenêtre de la console. |
|SET | Affiche la liste des variables d'environnement sur le système actuel. |

## Exemple de fichier BAT
Les scripts batch sont généralement enregistrés sous forme de simples fichiers texte ; contenant des commandes exécutées dans une séquence. Ces fichiers sont enregistrés avec l'extension .bat ; reconnu et exécuté à l'aide du logiciel **Command Interpreter**. Ce logiciel est disponible nativement dans Microsoft Windows sous le nom **cmd.exe**.

Voici un exemple de script batch qui supprime tous les fichiers du répertoire courant :
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Références

* [Script batch - Guide rapide](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Fichier batch - par Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

