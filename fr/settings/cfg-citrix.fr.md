{
"date": "2023-09-27",
  "keywords": [
"cfg",
"fichier cfg",
"fichier de connexion au serveur Citrix cfg",
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
"title": "Format de fichier CFG - Fichier de connexion au serveur Citrix",
  "description":"Découvrez le format de fichier de connexion au serveur Citrix CFG et les API permettant de créer et d'ouvrir des fichiers CFG.",
"linktitle": "CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix",
"parent" : "settings"
}
},
"lastmod": "2023-09-27"
}

## Qu'est-ce qu'un fichier CFG ?

Le fichier CFG est également connu sous le nom de **Fichier de connexion au serveur Citrix**. Il s’agit d’un composant essentiel utilisé pour établir la connexion au serveur Citrix. Ce fichier contient les informations essentielles nécessaires à une connexion réussie entre le périphérique client et le serveur Citrix. Il comprend généralement des détails tels que le nom d'hôte ou l'adresse IP du serveur, le port de serveur spécifique à utiliser et les informations d'identification requises pour l'authentification, qui comprennent souvent le nom d'utilisateur et le mot de passe.

Ces fichiers CFG jouent un rôle crucial dans la configuration du logiciel client Citrix, permettant aux utilisateurs de se connecter de manière transparente à divers serveurs Citrix. Ils agissent comme des fichiers de configuration qui rationalisent le processus de connexion en prédéfinissant les paramètres essentiels, réduisant ainsi le besoin pour les utilisateurs de saisir manuellement ces informations chaque fois qu'ils souhaitent accéder au serveur Citrix.

## Serveur Citrix

Un serveur Citrix, également connu sous le nom de serveur Citrix XenApp ou Citrix XenDesktop, est un serveur spécialisé utilisé dans les solutions de virtualisation Citrix. Citrix est une entreprise qui fournit une technologie pour l'accès à distance, la virtualisation des applications et la virtualisation des postes de travail. Les serveurs Citrix jouent un rôle central dans ces solutions en facilitant la fourniture d'applications et d'environnements de bureau aux utilisateurs distants ou aux appareils clients.

Voici comment fonctionne généralement le serveur Citrix :

1. **Livraison d'applications et de postes de travail** : les serveurs Citrix hébergent des applications et des environnements de bureau. Au lieu d'exécuter le logiciel directement sur l'appareil de l'utilisateur, l'application ou le bureau s'exécute sur le serveur Citrix et seule l'interface utilisateur est transmise à l'appareil client. Cela permet aux utilisateurs d'accéder aux applications et aux bureaux Windows à partir d'une large gamme d'appareils, notamment des PC, des Mac, des tablettes et des smartphones.
    















2. **Accès à distance** : les serveurs Citrix permettent un accès à distance aux applications et aux postes de travail, permettant ainsi aux utilisateurs de travailler de n'importe où avec une connexion Internet. Ceci est particulièrement utile pour les équipes distantes et distribuées, car cela offre une expérience informatique cohérente et sécurisée.
    















3. **Équilibrage de charge** : les serveurs Citrix fonctionnent souvent en clusters pour équilibrer la charge des connexions entrantes. L'équilibrage de charge garantit que les demandes des utilisateurs sont réparties uniformément entre les serveurs, optimisant ainsi les performances et la disponibilité.

## Fichier de connexion au serveur Citrix

Un fichier de connexion au serveur Citrix, souvent appelé fichier CFG, est un fichier de configuration utilisé dans les environnements Citrix pour établir des connexions entre les périphériques clients et les serveurs Citrix. Les détails clés généralement inclus dans le fichier de connexion au serveur Citrix peuvent inclure :

1. **Nom d'hôte ou adresse IP** : ceci spécifie l'emplacement réseau du serveur Citrix auquel le périphérique client doit se connecter. Il identifie l'emplacement où les ressources Citrix sont hébergées.
    















2. **Port du serveur** : numéro de port utilisé pour la communication avec le serveur Citrix. Cela garantit que les données sont transmises au service correct sur le serveur.
    















3. **Nom d'utilisateur et mot de passe** : les informations d'identification de l'utilisateur, y compris le nom d'utilisateur et le mot de passe, peuvent être incluses à des fins d'authentification. Ces informations d'identification permettent aux utilisateurs de prouver leur identité et d'accéder aux ressources Citrix.
    















4. **Paramètres de connexion** : les fichiers CFG peuvent contenir divers paramètres de connexion, tels que les paramètres de cryptage, les valeurs de délai d'expiration de session et les options d'affichage. Ces paramètres aident à configurer l’expérience utilisateur et les paramètres de sécurité.
    















5. **Configuration des ressources** : selon la configuration, le fichier CFG peut spécifier quelles ressources Citrix (applications ou bureaux) doivent être lancées lorsque la connexion est établie.

## Formats de fichiers utilisés par Citrix

Les serveurs Citrix et les technologies Citrix associées prennent en charge plusieurs formats de fichiers pour permettre la fourniture d'applications, de postes de travail et de contenu aux utilisateurs distants. Voici quelques formats de fichiers courants associés aux déploiements de serveurs Citrix :

1. **ICA (Architecture informatique indépendante)** :
    















- **.ica** : le fichier ICA est un composant essentiel de la fourniture d'applications et de postes de travail de Citrix. Il contient des informations sur la connexion au serveur Citrix, telles que l'adresse du serveur, le port, les paramètres de chiffrement et les préférences d'affichage. Lorsque l'utilisateur clique sur la ressource Citrix, le fichier [.ica](/fr/misc/ica/) est généré et utilisé par le client Citrix Receiver (ou Citrix Workspace) pour établir la connexion.
2. **Packages Citrix Receiver (ou Citrix Workspace)** :
    















- **.exe** : les packages d'installation Citrix Receiver ou Citrix Workspace sont souvent disponibles au format exécutable pour différents systèmes d'exploitation (par exemple, [.exe](/fr/executable/exe/) pour Windows, [.dmg](/fr/compression/dmg/) pour macOS). Ces packages permettent aux utilisateurs d'installer un logiciel client sur leurs appareils.
3. **Application Citrix Workspace (anciennement Citrix Receiver)** :
    















- **.app** : sur macOS, l'application Citrix Workspace est conditionnée sous forme de fichier d'application macOS [.app](/fr/executable/app/).
4. **Compatibilité avec les navigateurs Web** :
    















- Les solutions Citrix sont accessibles via des navigateurs Web, utilisant généralement HTML5 pour un accès Web. Les utilisateurs se connectent aux ressources Citrix via des URL sans nécessiter de formats de fichiers spécifiques.
5. **Images de disque de bureau virtuel** :
    















- **.vhd, .vhdx** : Citrix XenDesktop et XenApp peuvent fournir des bureaux et applications virtuels à l'aide d'un disque dur virtuel [VHD](/fr/disc-and-media/vhd/) ou [VHDX](/fr/disc-and-media/vhdx/).
6. **Métadonnées de publication de ressources** :
    















- **.xml** : les administrateurs Citrix utilisent souvent des fichiers [XML](/fr/web/xml/) pour définir les paramètres de publication des ressources, notamment les propriétés des applications, les stratégies d'accès et les affectations des utilisateurs.
7. **Fichiers du pilote d'imprimante** :
    















- Les environnements Citrix peuvent nécessiter des fichiers de pilote d'imprimante spécifiques (par exemple, .inf) pour garantir une fonctionnalité d'impression appropriée lors de l'utilisation d'applications distantes.
8. **Données de profil utilisateur** :
    















- **.upm** : Citrix Profile Management peut stocker les données de profil utilisateur dans des fichiers .upm pour offrir des expériences utilisateur cohérentes sur toutes les sessions et tous les appareils.
9. **Fichiers de configuration** :
    















- **.conf** : divers fichiers de configuration peuvent être utilisés pour définir les paramètres des composants Citrix, tels que les fichiers de configuration pour le serveur de licences Citrix (par exemple, CtxLicChk.conf).
10. **Configuration Citrix ADC (NetScaler)** :

- **.nsconfig :** Les fichiers de configuration pour Citrix Application Delivery Controllers (ADC), anciennement connus sous le nom de NetScaler, stockent les paramètres liés à l'équilibrage de charge, à la sécurité et à la gestion du trafic.

## Comment ouvrir le fichier CFG?

Programmes qui ouvrent ou référencent des fichiers CFG

- Client Citrix Access (Windows, MAC, Linux)

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
* [Citrix Virtual Apps](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)

