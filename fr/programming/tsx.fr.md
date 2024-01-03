{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Fichier TSX - Fichier React TypeScript - Qu'est-ce que le fichier .tsx et comment l'ouvrir?",
  "description":"Découvrez le fichier TSX React TypeScript et comment l'ouvrir.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-fr-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Qu'est-ce qu'un fichier TSX ?

L'extension de fichier « .tsx » est généralement associée aux fichiers TypeScript contenant du code **React**. **TypeScript est un sur-ensemble de JavaScript** qui ajoute un typage statique au langage, et **React est une bibliothèque JavaScript permettant de créer des interfaces utilisateur**. Lorsqu'ils travaillent ensemble avec React et TypeScript, les développeurs utilisent souvent l'extension « .tsx » pour leurs fichiers pour indiquer qu'ils contiennent à la fois TypeScript et JSX (l'extension de syntaxe de React pour JavaScript).

## Exemple de fichier TSX

TypeScript vous permet de définir des types pour vos variables, paramètres de fonction et plus encore. Vous verrez souvent du code TypeScript dans un fichier ".tsx" spécifiant les types d'accessoires, d'état et d'autres variables utilisés dans les composants React.

```
// Exemple : code TypeScript dans un composant React
interface MesComponentProps {
   nom : chaîne ;
   âge : nombre ;
}
const MyComponent : React.FC<MyComponentProps> = ({ nom, âge }) => {
   // Logique du composant ici
   return <div>{name} a {age} ans.</div> ;
} ;
```

## JSX (extension de syntaxe React)

JSX est une extension de syntaxe pour JavaScript recommandée par React. Il ressemble à XML/HTML et est utilisé pour décrire à quoi devrait ressembler l'interface utilisateur.

```
// Exemple : JSX dans un composant React
const MyComponent : React.FC<MyComponentProps> = ({ nom, âge }) => {
   return <div>{name} a {age} ans.</div> ;
} ;
```

Le fichier « .tsx » contiendra généralement la définition d'un composant React utilisant des composants fonctionnels ou des composants de classe.

```
// Exemple : Définition du composant React dans un fichier ".tsx"
const MonComponent : React.FC = () => {
   return <div>Bonjour, Réagissez !</div> ;
} ;
```

Vous verrez souvent des instructions d'importation au début du fichier, apportant les dépendances et les modules nécessaires.

```
// Exemple : Importer des instructions dans un fichier ".tsx"
importer React depuis « react » ;
```

## Comment ouvrir un fichier TSX ?

Les fichiers TSX sont des fichiers texte brut, vous pouvez donc les ouvrir dans n'importe quel éditeur de texte, par ex. Bloc-notes. Cependant, ce sont des fichiers de codage destinés à être ouverts par l'IDE, par ex. Code Visual Studio.