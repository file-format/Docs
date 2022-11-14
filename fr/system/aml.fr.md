{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier AML - Fichier de langage machine ACPI",
  "description":"En savoir plus sur le format de fichier ACPI AML et les API qui peuvent créer et ouvrir des fichiers AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Qu'est-ce qu'un dossier AML ?

Un fichier AML est un fichier système créé avec le langage ACPI (Advanced Configuration and Power Interface) utilisé pour configurer les propriétés du matériel. Il contient un code binaire indépendant de la machine qui est utilisé pour configurer le matériel même pour des opérations simples telles que l'arrêt d'un ordinateur. Les fichiers AML peuvent contenir des instructions en fonction de l'objectif pour lequel ils doivent être installés sur la machine. La mise en œuvre des normes ACPI vous permet d'améliorer la fonctionnalité de gestion de l'alimentation et une interface robuste pour configurer les périphériques de la carte mère tels que les cartes mères P55.

## Format de fichier ACPI AML

Les fichiers AML sont enregistrés sous forme de fichiers binaires sur un disque avec un contenu écrit en code octet. Les spécifications de format de fichier de la norme ACPI sont disponibles sur [uefi](https://uefi.org/node/735). Le langage a été conçu pour offrir stabilité et rétrocompatibilité, nécessitant moins de réécritures ou de reconstructions de la pile d'applications.

## Spécifications du format de fichier AML

Un fichier AML comprend des tables DSDT et SSDT. Le bytecode AML est lu et analysé depuis le début de chacune de ces tables. Cela donne des informations sur les définitions des périphériques et des objets dans l'espace de noms ACPI. À l'aide de ces informations, l'interpréteur AML peut générer une liste de tous les périphériques disponibles dans le système, ainsi que leurs propriétés et fonctions prises en charge.

### Exemple de code ASL pour un DSDT

Un exemple de code ASL pour un DSDT est le suivant.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## Références

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

