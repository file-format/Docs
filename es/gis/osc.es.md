{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSC - Formato de archivo de cambio de OpenStreetMap",
  "description":"Obtenga más información sobre el formato de archivo OSC y las API que pueden crear y abrir archivos OSC",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## ¿Qué es un archivo OSC?

Un archivo OSC es un formato de archivo de cambio que contiene datos de mapas de calles modificados para un mapa de calles .osm existente. Contiene información sobre los cambios que se realizarán en el [archivo OSM](/es/gis/osm/). El archivo OSC puede tener tres tipos posibles de operaciones de modificación en los datos OSM, es decir, `insertar`, `modificar` o `eliminar`. Estos archivos de cambios se usan comúnmente para exportar datos fuera del editor OSM e importarlos a otro editor.

Puede abrir archivos OSC con Merkaartar y el software osmchange.

## Formato de archivo OSC

Los archivos OSC se guardan comúnmente en formato de archivo JOSM, donde los cambios se representan mediante etiquetas. Comienza con la etiqueta `osmChange` que indica el comienzo del archivo. Las etiquetas secundarias especifican si se trata de una operación de inserción, modificación o eliminación que se realizará en el nodo correspondiente en el archivo OSM. El contenido de un nodo en realidad contiene el contenido de una etiqueta osm.

### Ejemplo de formato de archivo OSC

A continuación se muestra un ejemplo de operación de modificación en un nodo. Cada elemento debe tener un ID de conjunto de cambios y un número de versión.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referencias

* [Formato de archivo JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)

