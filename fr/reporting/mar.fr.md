{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Fichier de rapports Microsoft Access",
  "keywords" :[ "mar", "fichier mar", "format de fichier mar", "qu'est-ce que le rapport d'accès", "rapport d'accès", "rapport d'accès microsoft"],
  "description":"En savoir plus sur le format de fichier Acess Report (MAR) utilisé par le logiciel Microsoft Access pour créer un raccourci ou un lien vers Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Qu'est-ce que le rapport d'accès (fichier MAR) ? ##
Un fichier créé par Microsoft Access en tant que raccourci de son rapport est enregistré avec l'extension de fichier .mar. Un **rapport Microsoft Access** permet de formater, d'afficher et de résumer les informations de la base de données Microsoft Access. Ces rapports vous permettent de mettre en forme vos données dans une mise en page précise et informative pour visualisation à l'écran ou impression. Le rapport affiche uniquement les données statiques, ce qui signifie que nous ne pouvons pas modifier les données dans les tableaux lors de l'affichage du rapport Access. Le rapport affiche les données les plus récentes lorsqu'il est ouvert.

## Format de fichier Microsoft Access Report (MAR)

Le format de fichier MAR est utilisé par le logiciel Microsoft Access pour créer un raccourci ou un lien vers le rapport Microsoft Access qui est un objet de base de données qui devient utile lorsque vous devez présenter les informations de votre base de données pour l'une des utilisations suivantes :

- Afficher un résumé des données.
- Archiver des instantanés des données.
- Afficher les détails sur les enregistrements individuels.
- Créer des étiquettes.

## Parties du rapport d'accès
La conception d'un rapport Access est divisée en différentes sections qui peuvent être visualisées dans la vue Conception. Le tableau suivant explique le fonctionnement de chaque section et peut vous aider à créer des rapports.
| Rubrique | Comment la section est affichée lors de l'impression | Où la section peut être utilisée |
---------|----|------|
| En-tête du rapport | Au début du rapport. | Utilisez l'en-tête du rapport pour les informations qui peuvent normalement apparaître sur une page de garde, telles qu'un logo, un titre ou une date. Lorsque vous placez un contrôle calculé qui utilise la fonction d'agrégation Somme dans l'en-tête du rapport, la somme calculée est pour l'ensemble du rapport. L'en-tête du rapport est imprimé avant l'en-tête de la page. |
| En-tête de page | En haut de chaque page. | Utilisez un en-tête de page pour répéter le titre du rapport sur chaque page. |
| En-tête de groupe | Au début de chaque nouveau groupe d'enregistrements. | Utilisez l'en-tête de groupe pour imprimer le nom du groupe. Par exemple, dans un rapport regroupé par produit, utilisez l'en-tête de groupe pour imprimer le nom du produit. Lorsque vous placez un contrôle calculé qui utilise la fonction d'agrégation Somme dans l'en-tête de groupe, la somme est pour le groupe actuel. Vous pouvez avoir plusieurs sections d'en-tête de groupe dans un rapport, selon le nombre de niveaux de regroupement que vous avez ajoutés. Pour plus d'informations sur la création d'en-têtes et de pieds de groupe, consultez la section Ajouter un regroupement, un tri ou des totaux. |
| Détail | Apparaît une fois pour chaque ligne de la source d'enregistrement. | C'est là que vous placez les contrôles qui constituent le corps principal du rapport. |
| Pied de page de groupe | A la fin de chaque groupe d'enregistrements. | Utilisez un pied de groupe pour imprimer les informations récapitulatives d'un groupe. Vous pouvez avoir plusieurs sections de pied de groupe dans un rapport, selon le nombre de niveaux de regroupement que vous avez ajoutés. |
| Pied de page | A la fin de chaque page. | Utilisez un pied de page pour imprimer des numéros de page ou des informations par page. |
| Pied de page du rapport | A la fin du rapport. Remarque : En mode Conception, le pied de page du rapport s'affiche sous le pied de page. Cependant, dans toutes les autres vues (mode Mise en page, par exemple, ou lorsque le rapport est imprimé ou prévisualisé), le pied de page du rapport apparaît au-dessus du pied de page, juste après le dernier pied de groupe ou ligne de détail sur la dernière page. | Utilisez le pied de page du rapport pour imprimer les totaux du rapport ou d'autres informations récapitulatives pour l'ensemble du rapport. |






## Références ##

- [Introduction aux rapports dans Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Conception de rapports dans Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

