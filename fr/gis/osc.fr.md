{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSC - OpenStreetMap Modifier le format de fichier",
  "description":"En savoir plus sur le format de fichier OSC et les API qui peuvent créer et ouvrir des fichiers OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## Qu'est-ce qu'un fichier OSC ?

Un fichier OSC est un format de fichier de modification qui contient des données de plan de rue modifiées pour un plan de rue .osm existant. Il contient des informations sur les modifications à apporter au [fichier OSM](/fr/gis/osm/). Le fichier OSC peut avoir trois types possibles d'opérations de modification sur les données OSM, à savoir "insérer", "modifier" ou "supprimer". Ces fichiers de modifications sont couramment utilisés pour exporter des données hors de l'éditeur OSM et les importer dans un autre éditeur.

Vous pouvez ouvrir les fichiers OSC avec les logiciels Merkaartar et osmchange.

## Format de fichier OSC

Les fichiers OSC sont généralement enregistrés au format de fichier JOSM où les modifications sont représentées par des balises. Il commence par la balise `osmChange` qui indique le début du fichier. Les sous-balises précisent s'il s'agit d'une opération d'insertion, de modification ou de suppression à effectuer sur le nœud correspondant dans le fichier OSM. Le contenu d'un nœud contient en fait le contenu d'une balise osm.

### Exemple de format de fichier OSC

Voici un exemple d'opération de modification sur un nœud. Chaque élément doit avoir un ID d'ensemble de modifications et un numéro de version.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Références

* [Format de fichier JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

