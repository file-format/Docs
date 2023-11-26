{
"date": "07/03/2023",
  "keywords": [
"fichier enregistré",
"qu'est-ce qu'un fichier reg",
"déposer",
"extension de fichier reg",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier REG - Fichier de registre Windows",
  "description":"Découvrez le format REG et les API permettant de créer et d'ouvrir des fichiers REG.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent": "système"
}
},
"derniermod": "07/03/2023"
}

## Qu'est-ce qu'un fichier REG ?

Un fichier REG est un format de fichier utilisé pour importer ou exporter des données du registre Windows. Le registre Windows est une base de données hiérarchique qui stocke les paramètres et options de configuration du système d'exploitation Windows et des applications installées. Le registre contient des informations telles que les préférences utilisateur, les paramètres des applications, les données de configuration matérielle et logicielle, etc.

Un fichier REG a généralement une extension de fichier « .reg » et est un fichier texte brut contenant une série d'entrées et de valeurs de registre dans un format spécifique. Le format se compose d'une section d'en-tête qui identifie le fichier en tant que fichier de registre, suivie d'une série de paires clé-valeur qui représentent les entrées de registre.

## Format de fichier REG - Plus d'informations

Voici un exemple de format de fichier reg :

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

La première ligne du fichier précise la version de l'éditeur de registre. Les lignes suivantes contiennent les entrées de registre sous la forme d'un chemin de clé suivi d'un nom de valeur et de données de valeur. Dans cet exemple, le fichier reg contient deux entrées : une qui ajoute un programme appelé "Example.exe" à la liste de démarrage de Windows et une autre qui définit la valeur "Caché" dans les paramètres avancés de l'Explorateur Windows sur "true".

Les fichiers Reg peuvent être créés et modifiés à l'aide d'un éditeur de texte tel que le Bloc-notes. Ils sont souvent utilisés à des fins de sauvegarde et de restauration, ainsi que pour configurer plusieurs ordinateurs avec les mêmes paramètres de registre.

## Importer ou exporter le registre Windows

Un fichier REG est un type de fichier utilisé pour importer ou exporter des données à partir du registre Windows. Le registre Windows est une base de données hiérarchique qui stocke les paramètres et options de configuration du système d'exploitation Windows et des applications installées. Le registre contient des informations telles que les préférences utilisateur, les paramètres des applications, les données de configuration matérielle et logicielle, etc.

Les fichiers Reg peuvent être utilisés pour créer ou modifier des entrées de registre, et ils sont souvent utilisés à des fins de sauvegarde et de restauration, ainsi que pour configurer plusieurs ordinateurs avec les mêmes paramètres de registre. Voici comment utiliser un fichier reg pour ajouter une nouvelle entrée de registre au registre Windows :

1. Créez un nouveau fichier texte à l'aide d'un éditeur de texte tel que le Bloc-notes.
2. Saisissez l'entrée de registre au format correct. Le format se compose d'une section d'en-tête qui identifie le fichier en tant que fichier de registre, suivie d'une série de paires clé-valeur qui représentent les entrées de registre. Voici un exemple :

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Cela crée une nouvelle clé appelée « Exemple » sous la clé « Logiciel » dans la ruche de registre de l'utilisateur actuel et définit la valeur « Paramètre 1 » sur « Valeur 1 ».

3. Enregistrez le fichier avec une extension de fichier .reg.
4. Double-cliquez sur le fichier .reg pour ajouter la nouvelle entrée de registre au registre Windows.

Vous serez invité à confirmer que vous souhaitez ajouter l'entrée au registre. Une fois que vous avez confirmé, la nouvelle entrée sera ajoutée au registre et vous pourrez la vérifier à l'aide de l'outil Éditeur du Registre.

## Les références
* [Registre Windows](https://en.wikipedia.org/wiki/Windows_Registry)

