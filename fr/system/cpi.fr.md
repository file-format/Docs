{
"date": "2023-10-18",
   "keywords":[
"cpi",
"fichier cpi",
"fichier d'informations sur la page de codes cpi",
"comment ouvrir un fichier cpi",
"déposer",
"extension de fichier CPI",
"extension",
"déposer"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format de fichier CPI - Fichier d'informations de page de codes",
   "description":"Découvrez le format de fichier d'informations sur la page de code CPI et les API permettant de créer et d'ouvrir des fichiers CPI.",
"linktitle": "IPC",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
"parent" : "system"
}
},
"lastmod": "2023-10-18"
}

## Qu'est-ce qu'un fichier CPI ?

Un fichier `.cpi`, dans le contexte des systèmes d'exploitation Microsoft Windows et DOS, est généralement un **"Fichier d'informations sur la page de codes."** Ces fichiers contiennent des informations sur les pages de codes utilisées pour l'encodage de texte et les mappages de jeux de caractères. Les pages de codes sont essentielles pour afficher et traiter du texte dans différentes langues et jeux de caractères.

Dans le contexte de Windows et DOS, les pages de codes sont utilisées pour définir la manière dont les caractères sont représentés et codés dans différentes langues et régions. Ces pages de codes déterminent la manière dont les caractères sont stockés en mémoire et affichés à l'écran. Chaque page de codes possède un identifiant unique et les fichiers « .cpi » stockent des informations sur ces pages de codes, y compris des détails tels que les mappages de caractères et les informations sur les polices.

Les fichiers `.cpi` se trouvent généralement dans les répertoires système Windows ou DOS et jouent un rôle crucial en permettant au système d'exploitation d'afficher correctement le texte pour différents paramètres régionaux et jeux de caractères. Ils aident le système à comprendre comment interpréter et restituer les caractères de différentes langues et encodages.

## Fichiers d'informations sur les pages de codes

Examinons de plus près les fichiers d'informations de page de codes (.cpi) et leur fonctionnement dans le cadre de MS-DOS et des itérations antérieures de Microsoft Windows :

1. **Encodage de caractères et pages de codes** : les pages de codes sont un élément essentiel de la façon dont le texte est codé et affiché sur l'ordinateur. Ils définissent le codage des caractères pour une langue ou un jeu de caractères spécifique. Chaque page de codes attribue des valeurs numériques (points de code) aux caractères, permettant à l'ordinateur de les représenter et de les afficher. Par exemple, la page de codes 437 est couramment utilisée aux États-Unis et en Europe occidentale, tandis que la page de codes 850 est utilisée pour le codage Latin-1.
    







2. **Initialisation du système** : lors de l'initialisation du système (au démarrage de l'ordinateur), MS-DOS et les anciennes versions de Windows lisaient les fichiers `.cpi` pour déterminer les pages de codes à prendre en charge. Ces informations étaient cruciales pour le rendu du texte, la saisie au clavier et les conversions de jeux de caractères.
    







3. **Prise en charge de l'affichage et du clavier** : ces fichiers fournissent des informations sur la manière dont les caractères doivent être affichés à l'écran et sur les jeux de caractères ou les pages de codes qui doivent être pris en charge pour la saisie au clavier. Différentes pages de codes définissent différents jeux de caractères, de sorte que ces fichiers aident le système d'exploitation à savoir comment gérer les entrées de l'utilisateur et afficher correctement le texte.
    







4. **Localisation** : les fichiers `.cpi` sont essentiels pour la localisation du système d'exploitation. Ils permettent au système de s'adapter à différentes langues, régions et jeux de caractères, permettant ainsi aux utilisateurs du monde entier d'utiliser MS-DOS ou Windows dans leurs langues préférées.
    







5. **Plusieurs fichiers `.cpi`** : sur un ordinateur prenant en charge le multilingue, vous pouvez trouver plusieurs fichiers `.cpi` correspondant à différentes pages de codes. Par exemple, le système peut avoir « 437.cpi » pour les États-Unis, « 850.cpi » pour Latin-1, « 852.cpi » pour l'Europe centrale, etc. Le fichier approprié est chargé en fonction des paramètres régionaux de l'utilisateur ou de la page de codes sélectionnée.
    







6. **Informations sur les polices** : en plus des mappages de caractères, ces fichiers peuvent contenir des informations sur les polices, spécifiant les polices à utiliser pour chaque page de codes. Ceci est important pour rendre le texte dans un style et une taille appropriés.
    







7. **Systèmes hérités** : les fichiers `.cpi` étaient plus courants dans les anciennes versions de MS-DOS et Windows. Les versions modernes de Windows (telles que Windows 10 et versions ultérieures) utilisent généralement Unicode pour le codage du texte, qui prend en charge un large éventail de caractères et de langues. Unicode simplifie le traitement de texte pour les environnements multilingues et constitue la norme pour les logiciels modernes.

## Comment ouvrir le fichier CPI?

L’ouverture du fichier .CPI (Code Page Information) n’est pas une action utilisateur typique et ces fichiers ne sont généralement pas destinés à être ouverts manuellement. Ils sont utilisés par le système d'exploitation pour gérer l'encodage du texte et les jeux de caractères et leur contenu est accessible et utilisé automatiquement par le système.

Cependant, si vous souhaitez afficher le contenu du fichier .CPI à des fins d'information, vous pouvez essayer de l'ouvrir avec un éditeur de texte ou une visionneuse hexadécimale. Voici comment vous pouvez tenter d’ouvrir le fichier .CPI :

1. **Éditeur de texte** : vous pouvez utiliser un éditeur de texte comme le Bloc-notes (sous Windows) ou n'importe quel éditeur de texte brut sur d'autres systèmes d'exploitation pour ouvrir et afficher le fichier .CPI. Gardez à l’esprit que le contenu des fichiers .CPI n’est pas censé être lisible par l’homme et que vous pouvez voir des séries de caractères difficiles à interpréter.
    







2. **Visionneuse hexadécimale** : Une visionneuse hexadécimale ou un éditeur hexadécimal peut être utilisé pour ouvrir et inspecter le contenu du fichier .CPI dans sa forme binaire brute. Les éditeurs hexadécimaux fournissent une vue plus détaillée des données du fichier, ce qui peut être utile si vous essayez de comprendre sa structure. Des exemples de tels logiciels incluent HxD, Hex Fiend (pour macOS) et 010 Editor.

## Autres fichiers CPI

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.cpi**.

**Système vidéo**
- [CPI - Informations sur le clip vidéo AVCHD](/fr/video/cpi/)
- [CPI - Fichier d'informations sur la page de codes](/fr/system/cpi/)

## Les références
* [Page de codes](https://en.wikipedia.org/wiki/Code_page)

