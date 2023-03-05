{
  "date" : "2021-08-02",
  "keywords" :[ "fichier reg", "format de fichier reg", "qu'est-ce qu'un fichier reg", "fichier", "exemple reg", "extension de fichier reg","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"En savoir plus sur le format de fichier REG et les API qui peuvent créer et ouvrir des fichiers REG.",
  "title" :"REG - Fichier de registre Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Qu'est-ce qu'un fichier REG ?
Un fichier REG est simplement un fichier texte avec l'extension .reg. Ces fichiers sont généralement créés en exportant des clés typiques du registre. Ces fichiers peuvent également être utilisés comme sauvegarde du registre (spécialement cette étape est importante avant d'apporter des modifications !). Vous pouvez voir que certains les ont rendus disponibles sous forme de fichiers téléchargeables sur les mêmes sites qui vous montrent comment effectuer un hack de registre. Un fichier REG est utile pour apporter des modifications manuelles au registre et exporter ces modifications. Il suffit de nettoyer un peu le fichier, puis de le partager avec d'autres.

## Format de fichier REG
Le format de fichier REG a été conçu pour exporter et importer des parties du registre Windows à l'aide d'une syntaxe basée sur INI. Le registre Windows est une base de données relationnelle ou hiérarchique qui conserve les paramètres de bas niveau du système d'exploitation Microsoft Windows et d'autres applications qui utilisent le registre Windows. Alternativement, nous pouvons dire que le registre ou registre Windows se compose d'informations, d'options, de paramètres et d'autres valeurs pour les programmes et le matériel installés sur toutes les versions des systèmes d'exploitation Microsoft Windows.
### Syntaxe du fichier REG
Voici quelques éléments clés dans le cadre d'une syntaxe de fichier REG :
- **RegistryEditorVersion** : par exemple "Windows Registry Editor Version 5.00" pour Windows 2000, Windows XP et Windows Server 2003.
- **Ligne vide** : Identifie le début d'un nouveau chemin de registre.
- **RegistryPathx** : le chemin de la sous-clé qui contient la première valeur que vous importez.
- **DataItemNamex** : le nom de l'élément de données que vous souhaitez importer.
- **DataTypex** : le type de données pour la valeur de registre.

Les clés sont stockées dans des fichiers .reg en utilisant la syntaxe suivante :
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Vous pouvez modifier la valeur par défaut d'une clé en utilisant "@" au lieu de "Nom de la valeur" :
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Exemple
Voici un exemple de fichier REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Références

* [Registre Windows - par Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Comment ajouter, modifier ou supprimer des sous-clés et des valeurs de registre à l'aide d'un fichier .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
