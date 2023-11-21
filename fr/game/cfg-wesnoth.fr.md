{
"date": "2023-09-27",
  "keywords": [
"cfg",
"fichier cfg",
"fichier de langage de balisage cfg wesnoth",
"qu'est-ce qu'un fichier cfg",
"comment ouvrir le fichier cfg",
"déposer",
"extension de fichier cfg",
"extension"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc" : true,
"title": "Format de fichier CFG - Fichier de langage de balisage Wesnoth",
  "description":"Découvrez le format de fichier CFG Wesnoth Markup Language et les API permettant de créer et d'ouvrir des fichiers CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent": "jeu"
}
},
"lastmod": "2023-09-27"
}

## Qu'est-ce qu'un fichier CFG ?

Le fichier CFG est également connu sous le nom de **"Wesnoth Markup Language" (WML)**. Il s'agit d'un langage de balisage personnalisé utilisé principalement dans le jeu "Battle for Wesnoth", qui est un jeu de stratégie au tour par tour. WML est utilisé pour définir et personnaliser divers aspects du jeu, notamment les scénarios, les campagnes, les unités, etc. C'est un moyen pour les moddeurs et les développeurs de créer du contenu pour le jeu.

Il est écrit dans un format qui ressemble à une combinaison de XML et de scripts simples. Voici un aperçu de certains éléments et structures courants que vous pourriez trouver dans un fichier WML :

1. **Tags :** WML utilise des balises pour définir différents éléments du jeu. Les balises sont placées entre crochets. Par exemple:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Attributs :** Dans les balises, vous pouvez définir des attributs pour spécifier les propriétés ou les valeurs associées à l'élément. Dans l'exemple ci-dessus, « type » et « points de repère » sont des attributs.
    










3. **Tableaux et tableaux de tableaux :** Vous pouvez créer des tableaux de données et même des tableaux de tableaux pour définir des listes d'unités, des types de terrain ou d'autres éléments de jeu.
    










4. **Instructions conditionnelles :** WML prend en charge les instructions conditionnelles pour contrôler le flux du jeu. Par exemple:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Boucles :** Vous pouvez utiliser des boucles pour parcourir des listes d'éléments ou effectuer des actions à plusieurs reprises.
    










6. **Inclut :** Vous pouvez inclure d'autres fichiers WML dans un fichier WML principal pour organiser et modulariser votre contenu.
    










7. **Gestionnaires d'événements :** Vous pouvez définir des gestionnaires d'événements pour déclencher des actions lorsque des événements spécifiques se produisent dans le jeu.
    











Voici un exemple simplifié de fichier WML qui définit une unité personnalisée :

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## La bataille de Wesnoth

"The Battle for Wesnoth" est un jeu de stratégie au tour par tour populaire et open source. Il est disponible pour plusieurs plates-formes, notamment Mac, Windows, Linux, etc. Développé par une communauté dévouée de bénévoles, le jeu est connu pour son gameplay profond et engageant, ainsi que pour son monde fantastique riche.

Les principales caractéristiques de « La bataille de Wesnoth » incluent :

1. **Cadre fantastique :** Le jeu se déroule dans un monde fantastique avec diverses races, notamment des humains, des elfes, des nains, des orcs et bien plus encore. L'histoire et la narration du jeu font partie intégrante de son attrait.
    










2. **Stratégie au tour par tour :** Le gameplay est au tour par tour, où les joueurs prennent leur temps pour planifier et exécuter leurs mouvements sur des grilles hexagonales. Il combine combat tactique et prise de décision stratégique.
    










3. **Campagnes :** Le jeu propose un large éventail de campagnes solo, chacune avec son propre scénario, ses personnages et ses défis. Les joueurs peuvent explorer différents récits et scénarios.
    










4. **Multijoueur :** "Wesnoth" prend en charge le mode multijoueur en ligne, permettant aux joueurs de s'affronter dans des batailles stratégiques. Les modes multijoueurs incluent le jeu coopératif et les matchs compétitifs.

## Comment ouvrir le fichier CFG?

Les fichiers CFG, qui sont généralement associés au Wesnoth Markup Language (WML) utilisé dans le jeu « The Battle for Wesnoth », peuvent être facilement modifiés à l'aide de n'importe quel éditeur de texte standard. Ces fichiers contiennent du code lisible par l'homme écrit en WML, qui définit divers aspects du jeu, notamment les scénarios, les unités et les campagnes.

Bien que vous puissiez utiliser n'importe quel éditeur de texte pour modifier les fichiers CFG, certains éditeurs de texte avancés comme Emacs et Vi disposent de plugins de coloration syntaxique WML. Ces plugins fournissent un codage couleur et un formatage utiles pour permettre aux utilisateurs de distinguer plus facilement les différents éléments et structures dans le code WML.

Les programmes qui ouvrent ou font référence aux fichiers CFG incluent

- La bataille de Wesnoth (gratuit) pour (Windows, MAC, Linux)
- Bloc-notes Microsoft

## Autres fichiers CFG

Voici d'autres types de fichiers qui utilisent l'extension de fichier **.cfg**.

**Paramètres**
- [CFG - Fichier de configuration Celestia](/fr/settings/cfg-celestia/)
- [CFG - Fichier de connexion au serveur Citrix](/fr/settings/cfg-citrix/)
- [CFG - Fichier de configuration MAME](/fr/settings/cfg-mame/)
- [CFG - Fichier de configuration LightWave](/fr/settings/cfg-lightwave/)

**Jeu**
- [CFG - Fichier de langage de balisage Wesnoth](/fr/game/cfg-wesnoth/)
- [CFG - Fichier de configuration MUGEN](/fr/game/cfg-mugen/)
- [CFG - Fichier de configuration du moteur source](/fr/game/cfg-sourceengine/)

**Système et divers**
- [CFG - Fichier CFG](/fr/system/cfg/)
- [CFG - Fichier de configuration du modèle Cal3D](/fr/misc/cfg-cal3d/)

## Les références
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
