{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "fichier", "extension", "format de fichier", "Script Visual Basic", "Guide de programmation", "exemple vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Fichier de script Visual Basic",
  "description":"En savoir plus sur le format de fichier VBS et les API qui peuvent créer et ouvrir des fichiers VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Qu'est-ce qu'un fichier VBS ?

VBS ou VBScript est connecté à l'édition de script de Microsoft Visual Basic. Dans l'environnement informatique, l'utilisateur est autorisé à accéder et à contrôler de nombreux aspects de celui-ci. VBScript est autorisé à utiliser un modèle nommé **Component Object Model** pour utiliser les éléments et les outils de l'environnement. Cet environnement est spécifié pour travailler et exécuter VBScript.

Il sert comme Javascript lorsqu'il est accédé par le client dans le domaine du développement Web. Il est également utilisé par les serveurs pour le traitement des pages Web. Il peut être pris en compte dans d'autres types de fichiers de script tels que les applications de [HTML](/fr/web/html/).


## Bref historique ##

Il a été lancé pour la première fois en 1996, dans le cadre des technologies utilisées par Microsoft spécifiées pour les scripts Windows. Il a été spécialement développé pour l'aide des développeurs Web initialement. La même année, l'explorateur de Microsoft Windows nommé Internet Explorer est sorti avec les fonctionnalités de Visual Basic Script.

Avec les progrès de la technologie et du développement Web, de nombreuses versions de VBScript ainsi que de nombreuses fonctionnalités avancées ont été lancées. De plus, dans l'année à venir, ce langage de script fera partie de Microsoft Windows avec de nouvelles fonctionnalités.

## Spécification technique ##

Pour les pages Web côté serveur, les outils tels que **Active Server Pages** sont utilisés avec VBScript. Ce langage de script peut également être utilisé dans le composant de script de Windows. Les fichiers de cette langue sont stockés avec une extension .vbs dans Windows.

Il existe de nombreuses structures de contrôle telles que des boucles qui sont utilisées dans le code de ce langage. Il inclut également des arguments qui sont en ligne de commande et qui peuvent être nommés ou non. Les fichiers de cette langue peuvent être stockés simplement dans les dossiers ou sur le bureau d'un système d'exploitation Windows. Bien qu'il n'y ait pas d'environnement de développement intégré spécifique pour les programmes VBScript comme Microsoft Script Editor, il offre la possibilité de développer ce langage.

Lorsque VBScript est hébergé par l'hôte de script de Windows, il fournit diverses fonctionnalités assez communes aux langages de script mais qui ne sont pas disponibles dans Visual Basic 6.0. Les fonctionnalités qui impliquent un accès facile ou direct impliquent des imprimantes réseau, des arguments de ligne de commande sans nom et nommés, stdout et stdin, des partages réseau, Windows Management Instrumentation, des informations utilisateur sur des réseaux comme l'appartenance à un groupe, et bien plus encore.

## Exemple de format de fichier VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Référence ##

* [VBS - par Wikipédia](https://en.wikipedia.org/wiki/VBScript)



