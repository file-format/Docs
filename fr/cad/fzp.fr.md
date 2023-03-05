{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"En savoir plus sur le format de fichier FZP et les API qui peuvent créer et ouvrir des fichiers FZP.",
  "title" :"Format de fichier FZP - Fichier de description de partie XML Fritzing",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Qu'est-ce qu'un fichier FZP ?

Un fichier FZP est un fichier XML créé par [Fritzing](https://fritzing.org/) application de prototypage et de conception de circuits électroniques. Il contient des informations sur les propriétés, les connecteurs et les bus du composant au format de fichier [XML](/fr/web/xml/). Les fichiers FPZ ne peuvent pas être utilisés indépendamment dans Fritzing. Au lieu de cela, ils sont importés dans le cadre du fichier d'archive FZPZ.

## Format de fichier FZP - Plus d'informations

Les fichiers FZP sont des fichiers XML qui contiennent des informations sur les propriétés, les connecteurs et les bus de la pièce. En plus de cela, les fichiers FZP contiennent également des informations sur le titre, la description, l'auteur et la date de publication du fichier FZP. Lorsqu'un fichier de pièce Fritzing est exporté, l'application Fritzing crée une archive compressée [FZPZ](/fr/compression/fzpz/) qui contient un fichier FZP et quatre fichiers [SVG](/fr/image/svg/).

Les [spécifications du format de fichier FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) sont disponibles sur Github par Fritzing.

## Exemple de structure de fichier FZP

Un fichier FZP typique a la structure XML suivante.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Références

* [Spécifications du format de fichier FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Nouvelles pièces avec extension fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

