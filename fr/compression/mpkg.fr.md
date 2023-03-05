{
  "date" : "2019-10-11",
  "keywords" :[ "fichier mpkg", "format de fichier mpkg", "qu'est-ce qu'un fichier mpkg", "fichier", "exemple mpkg", "extension de fichier mpkg","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier MPKG - Fichier de méta-paquet",
  "description":"En savoir plus sur le format de fichier MPKG et les API qui peuvent créer et ouvrir des fichiers MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Qu'est-ce qu'un fichier MPKG ?

Un fichier avec l'extension .mpkg est un fichier d'installation d'archive, principalement trouvé sur les systèmes d'exploitation MacOS. Il contient tous les fichiers d'installation requis de l'application sans qu'il soit nécessaire de conserver les fichiers associés séparément. Un seul fichier MPKG peut contenir des fichiers de package [PKG](/fr/compression/pkg/) comme l'un des fichiers d'installation en plus d'autres fichiers. Les fichiers MPKG ne peuvent être ouverts avec aucun logiciel général et sont exécutés automatiquement sur MacOS à l'aide d'Apple Installer.

## Format de fichier MPKG

Un fichier MPKG contient différents types de fichiers nécessaires à l'installation de plusieurs packages qu'il contient. Ceci est visible sur l'image ci-dessous qui est l'arborescence d'un exemple de fichier MPKG. Cette arborescence est exportée à l'aide de la commande `tree` sur le terminal MacOS.

{{< figure src="../mpkg.png" alt="Format de fichier MPKG" >}}

La description des différents éléments de l'image est la suivante.

`Répertoire des packages` - stocke une liste de fichiers pkg, c'est-à-dire une liste de sous-packages
`Resources Directory` - stocke les ressources utilisées par pkg, telles que les ressources et les images localisées, les documents Rtf, les documents pdf, etc.
`Fichier Distribution.dist` - Un document xml contenant des informations telles que les sous-packages à installer et les scripts d'exécution

Un exemple de fichier XML pour un fichier MPKG peut se présenter comme suit en fonction des sous-packages associés.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/fr/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - est le sous-paquet à installer. C'est un répertoire de la structure Bundle au format pkg. Il contient un sous-répertoire Contents.

## Références

* [Forfaits plats OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Gestionnaire de packages MPKG C++](https://github.com/puellavulnerata/mpkg)

