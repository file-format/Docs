{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - Formato de arquivo de alteração do OpenStreetMap",
  "description":"Saiba mais sobre o formato de arquivo OSC e APIs que podem criar e abrir arquivos OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-pt",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## O que é um arquivo .OSC?

Um arquivo OSC é um formato de arquivo de alteração que contém dados de mapa de ruas modificados para um mapa de ruas .osm existente. Ele contém informações sobre as alterações a serem incorridas no [OSM file](/gis/osm/). O arquivo OSC pode ter três tipos possíveis de operações de modificação nos dados OSM, ou seja, `insert`, `modify` ou `delete`. Esses arquivos de alteração são comumente usados para exportar dados do editor OSM e importá-los para outro editor.

Você pode abrir arquivos OSC com software Merkaartar e osmchange.

## Formato de arquivo OSC

Os arquivos OSC são comumente salvos no formato de arquivo JOSM, onde as alterações são representadas por tags. Começa com a tag `osmChange` que indica o início do arquivo. As subtags especificam se é uma operação de inserção, modificação ou exclusão que deve ser executada no nó correspondente no arquivo OSM. O conteúdo de um nó contém, na verdade, o conteúdo de uma tag osm.

### Exemplo de formato de arquivo OSC

A seguir está um exemplo de operação de modificação em um nó. Cada elemento deve ter um ID de conjunto de alterações e um número de versão.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## Referências

* [Formato de arquivo JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


