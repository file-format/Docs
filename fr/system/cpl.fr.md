{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extension", "fichier", "format", "système", "Fichier du panneau de configuration", "Windows", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Fichier du panneau de configuration",
  "description":"En savoir plus sur le format de fichier CPL et les API qui peuvent créer et ouvrir des fichiers CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier CPL ? ##

Un fichier CPL est un type de fichier "système". Il est utilisé par le système d'exploitation Windows. Un fichier CPL est l'abréviation de Control Panel File. Ces fichiers sont des fichiers binaires qui s'ouvrent avec le panneau de configuration dans un système d'exploitation Microsoft Windows et sont utilisés pour représenter et ouvrir les outils disponibles dans le panneau de configuration, tels que la souris, les écrans, la mise en réseau, entre autres. Les fichiers CPL sont généralement stockés dans le dossier système de votre appareil. Ces fichiers ne doivent pas être ouverts manuellement.


## Format de fichier CPL ##

Différents fichiers CPL de votre système d'exploitation Windows sont connectés pour représenter différents éléments du panneau de configuration. Tous les éléments du panneau de contrôle sont liés à un fichier CPL et ont le suffixe ".cpl" attaché à leurs éléments.

Certains types courants de fichiers CPL avec leurs formats sont :

* Inetcpl.cpl – Pour les propriétés Internet sur votre appareil
* Appwiz.cpl - Pour ajouter ou supprimer des propriétés de programmes sur votre appareil
* Desk.cpl – Pour les propriétés d'affichage
* Main.cpl – Pour les propriétés liées à la souris, aux polices, au clavier et aux imprimantes.
* Netcpl.cpl - Pour les propriétés liées au réseau
* System.cpl - Pour les propriétés liées au système et pour l'assistant Ajouter un nouveau matériel
* TimeDate.cpl – Pour les propriétés de date ou d'heure
* Mlcfg32.cpl – Pour les propriétés Microsoft Exchange ou Windows Messaging
* Intl.cpl - Cela concerne les propriétés des paramètres régionaux
* Modem.cpl - Pour les propriétés liées au modem
* Themes.cpl - Stocke les thèmes et les propriétés du bureau.
* Password.cpl – Pour les propriétés de mot de passe
* Mmsys.cpl – Pour les propriétés multimédias
* Wgpocpl.cpl – Concerne Microsoft Mail Post Office

## Bref historique ##

Le type de fichier CPL a été développé par Microsoft Windows et fait partie intégrante du système d'exploitation Windows depuis Windows 1.0. Il est toujours utilisé dans toutes les versions de Windows et toutes les propriétés des éléments du panneau de configuration sont stockées à l'aide de ce type de fichier.

## Exemple CPL ##

Un exemple de fichier CPL peut être vu ci-dessous :

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
