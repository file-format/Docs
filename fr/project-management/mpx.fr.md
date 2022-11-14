{
  "date" : "2019-10-11",
  "keywords" :[ "fichier mpx", "format de fichier mpx", "qu'est-ce qu'un fichier mpx", "fichier", "exemple mpx", "extension de fichier mpx","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Format de fichier Microsoft Project Exchange",
  "description":"En savoir plus sur le format de fichier MPX et les API qui peuvent créer et ouvrir des fichiers MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Qu'est-ce qu'un fichier MPX ? ##

Un fichier avec l'extension .mpx est un format de fichier Microsoft Exchange. Un format de fichier MPX a été développé par Microsoft Project (MSP) pour faciliter l'échange d'informations de projet entre MSP et d'autres applications prenant en charge le format de fichier MPX, notamment Primavera Project Planner, Sciforma et Timerline Precision Estimating. À l'aide des fichiers MPX, vous pouvez transférer toutes sortes d'informations d'un projet vers un autre système, telles que des informations détaillées sur l'affectation des ressources, des informations sur le calendrier ou des informations à partir de la boîte de dialogue Informations sur le projet.

Microsoft Project 4.0 a introduit la prise en charge de la création et de la lecture des formats de fichiers MPX qui ont continué à être utilisés via Microsoft Project 98. Cependant, la prise en charge de la création de fichiers MPX a interrompu la version de Microsoft Project 2000, et les versions jusqu'à Microsoft Project 2010 ne prennent en charge que la lecture MPX. Le format de fichier MPX n'est pas pris en charge dans les versions ultérieures à MSP 2010.

## Format de fichier MPX ##

Un aperçu des spécifications du fichier MPX est donné dans cette section. Les spécifications complètes peuvent être trouvées dans cette [Base de connaissances](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) article et peut être consulté pour plus de détails.

### Enregistrements ###

Un enregistrement du fichier MPX contient des informations sur le projet. Il existe différents types d'enregistrements où chaque enregistrement a son propre ordre. Chaque type d'enregistrement est identifié par son numéro d'enregistrement. Pour un fichier MPX, il est nécessaire de contenir le type d'enregistrement Création de fichier. Les autres types d'enregistrements ne sont pas obligatoires. Le tableau suivant montre tous les types d'enregistrement, leurs numéros d'enregistrement et le nombre d'enregistrements que chaque type peut contenir dans le fichier MPX. L'inclusion d'enregistrements dans le fichier MPX doit suivre l'ordre du tableau, avec des commentaires insérés n'importe où.

|Nom de l'enregistrement|Numéro d'enregistrement|Nombre maximum d'enregistrements
---|---|---|
|Création de fichier (obligatoire)|aucun|1
|Paramètres de devise|10|1
|Paramètres par défaut|11|1
|Paramètres de date et d'heure|12|1
|Définition du calendrier de base|20|250
|Heures calendaires de base|25| 7 par enregistrement de définition de calendrier de base
|Exception de calendrier de base|26| 250 par enregistrement de définition de calendrier de base
|En-tête de projet|30|1
|Text Resource Table Definition|140|1- (Vous pouvez également utiliser l'enregistrement Numeric Resource Table Definition)
|Définition de la table des ressources numériques|41|1
|Ressource|50|9 999
|Remarques sur les ressources|51| 1 par enregistrement de ressource
|Définition du calendrier des ressources|55| 1 par enregistrement de ressource
|Heures du calendrier des ressources|56| 7 par calendrier de ressources
|Exception du calendrier des ressources| 57|250 par calendrier de ressources
|Text Task Table Definition|60|1 (Vous pouvez également utiliser l'enregistrement Numeric Task Table Definition)
|Définition de la table des tâches numériques|61|1
|Tâche|70|9
|Notes de tâche|71| 1 par enregistrement de tâche
|Tâche récurrente|72| 1 par enregistrement de tâche
|Affectation des ressources|75| 100 par enregistrement de tâche
|Champs du groupe de travail d'affectation|76| 1 par enregistrement d'affectation
|Noms de projet|80|500
|Liens clients DDE et OLE|81|500
|Commentaires|0|illimité

### Structure du fichier ###

Un fichier MPX se compose d'enregistrements mentionnés ci-dessus qui sont disposés de manière prédéfinie à l'intérieur du fichier. Les détails de ces types d'enregistrement sont décrits ci-dessous :

**Enregistrement de création de fichier (FCR) :** Il s'agit d'un enregistrement obligatoire dont le but est d'identifier :

* Format de fichier (MPX)
* Liste des caractères séparateurs utilisés dans le fichier
* Programme et numéro de version utilisés pour créer le fichier
* Numéro de version du format de fichier MPX utilisé dans le fichier
* Page de code utilisée pour créer le fichier

Il doit s'agir du premier enregistrement du fichier. Lors de l'exportation à partir de Microsoft Project, le caractère séparateur de liste est spécifié dans l'élément Paramètres régionaux du Panneau de configuration de Windows. Un enregistrement FCR comprend les champs suivants :

* MPX suivi immédiatement du caractère séparateur de liste
* Nom/Identifiant du programme
* Numéro de version du fichier
* Page de codes (850, 437, MAC, ANSI)

Par exemple, l'enregistrement peut contenir des informations **MPX, Microsoft Project, 3.0**, qui spécifient qu'une virgule est utilisée comme caractère séparateur de liste dans ce fichier MPX. La version du format MPX utilisée dans le fichier est exportée à partir de Microsoft Project version 3.0.

**Paramètres de devise** Cet enregistrement, portant le numéro d'enregistrement 10, spécifie les paramètres des options de devise dans la boîte de dialogue Options. Si cet enregistrement n'est pas inclus, les paramètres actuels de la boîte de dialogue Options sont utilisés. Les séparateurs des milliers et des décimales sont spécifiés dans l'élément Paramètres régionaux du Panneau de configuration de Windows.
Les champs inclus dans cet enregistrement sont :

* Symbole de la monnaie
* Position du symbole (0 # après, 1 # avant, 2 # après avec un espace, 3 # avant avec un espace)
* Chiffres monétaires (0,1,2)
* Séparateur de milliers
* Séparateur décimal

**Exemple :** 10,$,1,2,",",.
Cet exemple spécifie que les valeurs monétaires incluent un signe dollar ($) devant elles, que deux chiffres sont inclus après la virgule décimale, qu'une virgule est utilisée pour séparer les milliers et qu'un point est utilisé comme virgule décimale. Étant donné que le caractère séparateur de liste est inclus dans le champ Séparateur de milliers, le champ est entouré de guillemets.

**Paramètres par défaut :** Cet enregistrement, portant le numéro d'enregistrement 11, spécifie les paramètres des options par défaut dans la boîte de dialogue Options. Si une durée n'est pas spécifiée, l'unité de durée par défaut doit être définie pour des calculs d'unité de durée corrects. Si cet enregistrement n'est pas inclus, les paramètres actuels de la boîte de dialogue Options sont utilisés.
Les champs inclus dans cet enregistrement sont :

* Unités de durée par défaut (0 # minutes, 1 # heures, 2 # jours, 3 # semaines)
* Type de durée par défaut (0 # non fixe, 1 # fixe)
* Unités de travail par défaut (0 # minutes, 1 # heures, 2 # jours, 3 # semaines)
* Heures/jour par défaut
* Heures/semaine par défaut
* Tarif standard par défaut
* Taux d'heures supplémentaires par défaut
* La mise à jour de l'état des tâches met à jour l'état des ressources (0 # non, 1 # oui)
* Tâches en cours fractionnées (0 # non, 1 # oui)

**Paramètres de date et d'heure :** Cet enregistrement, portant le numéro d'enregistrement 12, spécifie les paramètres des options de date et d'heure dans la boîte de dialogue Options et l'option Format de date du texte à barres dans la boîte de dialogue Mise en page. Si cet enregistrement n'est pas inclus, les paramètres actuels de la boîte de dialogue Options sont utilisés.
\\Les champs inclus dans cet enregistrement sont :

* Ordre de date (0 # mois/jour/année, 1 # jour/mois/année, 2 # année/mois/jour)
* Format de l'heure (0 # 12 heures, 1 # 24 heures)
* Heure par défaut (nombre de minutes après minuit)
* Séparateur de dates
* Séparateur de temps
* 0:00 à 11:59 Texte
* Texte de 12h00 à 23h59
* Format de date (0 -14)*
* Format de date du texte de la barre (0 -194)*

**Définition du calendrier de base :** Ces enregistrements, portant le numéro d'enregistrement 20, définissent les calendriers de base et leurs jours ouvrés et non ouvrés de la semaine. Les paramètres par défaut sont utilisés s'il n'y a pas d'entrée pour un jour. Les paramètres par défaut sont du lundi au vendredi pour les jours ouvrables et le samedi et le dimanche pour les jours non ouvrables. Dans cet enregistrement, le champ Nom est obligatoire. Pour chacun des jours, une entrée de 0 indique que le jour est un jour chômé, et une entrée de 1 indique que le jour est un jour ouvré.
Les champs inclus dans cet enregistrement sont :

* Nom
* Dimanche
* Lundi
* Mardi
* Mercredi
* Jeudi
* Vendredi
* Samedi

**Heures calendaires de base :** Ces enregistrements, ayant le numéro d'enregistrement 25, spécifient les heures de travail pour les jours de la semaine s'ils diffèrent des paramètres par défaut. Les heures de travail par défaut sont de 8 h 00 à 12 h 00 et de 13 h 00 à 17 h 00. Chaque enregistrement d'heures calendaires de base fait référence à l'enregistrement de définition de calendrier de base précédent. Jusqu'à sept de ces enregistrements peuvent suivre chaque enregistrement de définition de calendrier de base.

* Jour de la semaine (1 - 7, où 1 # dimanche et 7 # samedi)
* À partir du temps 1
* Au temps 1
* À partir du temps 2
* Au temps 2
* À partir du temps 3
* Au temps 3

**Exception de calendrier de base :** Ces enregistrements, ayant le numéro d'enregistrement 26, définissent les exceptions aux jours et heures spécifiés dans les deux types d'enregistrement précédents. Jusqu'à 250 de ces enregistrements peuvent suivre chaque enregistrement de définition de calendrier de base. Ces enregistrements doivent être classés par ordre chronologique. Si une exception est d'un jour, vous pouvez laisser le champ Jusqu'à ce jour vide. Si aucune heure n'est indiquée, les heures par défaut de 8h00 à 12h00 et de 13h00 à 17h00 sont utilisées.
Les champs inclus dans cet enregistrement sont :

* Partir de la date
* À ce jour
* Chômé/Travail (0 # non-travail, 1 # travail)
* À partir du temps 1
* Au temps 1
* À partir du temps 2
* Au temps 2
* À partir du temps 3
* Au temps 3

**En-tête de projet :** Cet enregistrement, ayant la valeur d'enregistrement 30, définit les champs de projet globaux, tels que la date de début et la date de fin du projet. Les champs de cet enregistrement correspondent aux informations des boîtes de dialogue Informations sur le projet et Statistiques.
Les champs et onglets inclus dans cet enregistrement sont :

* Onglet Projet
* Compagnie
* Gestionnaire
* Calendrier (Standard utilisé si aucune entrée)
* Date de début (ce champ ou le champ suivant est calculé pour un fichier importé, selon le paramètre Planifier à partir de)
* Date de fin
* Horaire à partir de (0 # début, 1 # fin)
* Date actuelle*
* Commentaires
* Coût
* Coût de base
* Prix actuel
* Travailler
* Travail de base
* Vrai travail
* Travailler
* Durée*
* Durée de base *
* Durée réelle
* Pourcentage achevé
* Début de base
* Finition de base
* Début réel
* Finition réelle
* Écart de départ
* Écart de finition
* Matière
* Auteur
* Mots clés

**Définition de la table de ressources textuelles** : cet enregistrement répertorie les champs de ressources, dans l'ordre, qui sont importés ou exportés. Pour les fichiers importés, les noms doivent correspondre aux noms de champs utilisés dans Microsoft Project. Pour les fichiers exportés, cet enregistrement provient de la table d'exportation de la ressource. Cet enregistrement ou l'enregistrement Définition de la table des ressources numériques doit être utilisé. Lors de l'exportation à partir de Microsoft Project, ces deux enregistrements sont inclus.

**Définition de la table des ressources numériques :** Utilisant des nombres plutôt que des noms, cet enregistrement répertorie les champs de ressources, dans l'ordre, qui sont importés ou exportés. Il s'agit d'une méthode alternative pour identifier les champs de ressource inclus dans chaque enregistrement de ressource et est utile lors de la définition d'un fichier MPX créé par un produit en langue étrangère.

**Ressource :** Ces enregistrements contiennent les informations relatives à chaque ressource importée ou exportée. Chaque enregistrement de ressource décrit une ressource. Lorsque vous importez des informations, les champs qui sont inclus sont définis par l'enregistrement de définition de table de ressources textuelles ou l'enregistrement de définition de table de ressources numériques. Lorsque vous exportez des informations, les champs inclus sont ceux répertoriés dans la table d'exportation de la ressource.

**Notes de ressource :** Ces enregistrements contiennent des notes sur l'enregistrement de ressource immédiatement précédent. Pour une nouvelle ligne dans la note, le caractère ASCII 127 est utilisé. Si la note inclut le caractère séparateur de liste, placez la note entre guillemets.

**Définition du calendrier des ressources :** Ces enregistrements définissent les jours ouvrables pour la ressource spécifiée dans l'enregistrement de ressource immédiatement précédent. Pour les fichiers importés, s'il n'y a pas d'entrée pour le champ Nom du calendrier de base, Standard est utilisé. Aucune entrée pour le jour spécifique indique que le jour est défini sur la valeur par défaut (2). S'il n'existe aucun enregistrement de définition de calendrier de ressources, Standard est utilisé comme calendrier de base pour la ressource, la valeur par défaut étant utilisée pour les jours. Pour chacun des jours, une entrée de 0 indique que le jour est un jour chômé, 1 indique que le jour est un jour ouvré et 2 spécifie que la valeur par défaut est utilisée.

**Heures du calendrier de la ressource :** Ces enregistrements définissent les heures de travail de la ressource qui diffèrent du calendrier de base utilisé par la ressource. Ces enregistrements s'appliquent à l'enregistrement de définition du calendrier des ressources qui précède immédiatement cet enregistrement. Jusqu'à sept de ces enregistrements peuvent suivre chaque enregistrement de définition de calendrier de ressources.

**Exception du calendrier des ressources :** Ces enregistrements définissent les exceptions aux jours et heures spécifiés dans les deux types d'enregistrement précédents. Jusqu'à 250 de ces enregistrements peuvent suivre chaque enregistrement de définition de calendrier de ressources. Ces enregistrements doivent être classés par ordre chronologique. Si l'exception ne concerne qu'un jour, vous pouvez laisser le champ Jusqu'à ce jour vide. Si aucune heure n'est indiquée, les heures par défaut de 8h00 à 12h00 et de 13h00 à 17h00 sont utilisées.

**Définition du tableau des tâches textuelles :** Cet enregistrement répertorie les champs de tâche, dans l'ordre, qui sont importés ou exportés. Pour les fichiers importés, les noms doivent correspondre aux noms de champs utilisés dans Microsoft Project. Si le fichier est en cours d'exportation, cet enregistrement provient de la table d'exportation de la tâche. Lors de l'exportation à partir de Microsoft Project, ces deux enregistrements sont inclus. Les champs calculés par Microsoft Project, tels que Début planifié et Fin planifiée, sont ignorés s'ils sont importés. Si vous avez des dates de début ou de fin de tâche fixes, utilisez les champs Type de contrainte et Date de contrainte.

**Définition de la table des tâches numériques :** En utilisant des nombres plutôt que des noms, cet enregistrement répertorie les champs de tâche, dans l'ordre, qui sont importés ou exportés. Il s'agit d'une méthode alternative pour identifier les champs de tâche inclus dans chaque enregistrement de tâche et est utile lors de la définition d'un fichier MPX créé par un produit en langue étrangère.

**Tâche :** Ces enregistrements contiennent les informations relatives à chaque tâche importée ou exportée. Chaque enregistrement de tâche décrit une tâche. Lorsque vous importez des informations, les champs qui sont inclus sont définis par l'enregistrement Définition de la table des tâches de texte ou l'enregistrement Définition de la table des tâches numériques. Lorsque vous exportez des informations, les champs inclus sont ceux répertoriés dans la tâche Exporter le tableau.

**Notes de tâche :** Ces enregistrements contiennent des notes sur l'enregistrement de tâche immédiatement précédent. Utilisez le caractère ASCII 127 pour indiquer une nouvelle ligne dans la note. Si la note inclut le caractère séparateur de liste, placez la note entre guillemets.

**Affectation de ressources** : ces enregistrements répertorient les informations sur les ressources affectées à la tâche qui a été définie dans l'enregistrement de tâche précédent. Si vous fusionnez des fichiers et que vous souhaitez conserver les informations d'affectation des ressources, vous devez inclure les informations dans le fichier MPX. Si vous fusionnez, toutes les affectations existantes sur les tâches fusionnées seront supprimées. Si vous fusionnez des fichiers en fonction d'ID uniques, les ressources sont affectées à l'aide des ID uniques de ressource plutôt que des ID.

**Champs de groupe de travail d'affectation de ressources :** Ces enregistrements répertorient les informations stockées avec chaque affectation pour les fonctionnalités de groupe de travail de Microsoft Project 4.0 et 4.1. Si vous utilisez les fonctionnalités de groupe de travail, vous devez inclure cet enregistrement pour vous assurer qu'aucune information n'est perdue.

**Noms de projet :** Ces enregistrements répertorient tous les noms de lien DDE stockés dans le projet.

**Liens clients DDE et OLE :** Ces enregistrements répertorient les liens DDE dans le projet.

**Commentaires :** Ces enregistrements peuvent être utilisés pour ajouter des commentaires au fichier et peuvent apparaître à n'importe quel endroit du fichier. Chaque enregistrement de commentaires doit commencer par un "0".

## Problèmes pour ouvrir un fichier MPX ##

Voici la liste de certains problèmes courants qui peuvent survenir et entraîner un dysfonctionnement du format MPX :

* Absence de logiciel de support
* Fichier corrompu
* Fichier infecté à cause d'un virus
* Aucun droit d'accès dans le système pour ouvrir les fichiers
* Lecteur obsolète dans votre système
* L'extension du fichier est renommée

## Références ##

* [MPX - Base de connaissances Microsoft](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

