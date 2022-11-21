{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "arquivo amf", "formato de arquivo amf", "formato de arquivo", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo AMF e APIs que podem abrir e criar arquivos AMF.",
  "title" :"AMF - Arquivo de Manufatura Aditiva",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo AMF?
Um arquivo AMF consiste em diretrizes para descrição de objetos a serem utilizados pelos processos de Manufatura Aditiva. Contém uma abertura<amf> tag XML e termina com um</amf> elemento. Isso é precedido por uma linha de declaração XML especificando a versão XML e a codificação do arquivo. As declarações podem incluir informações de unidades de medida e, na ausência de tais informações, os milímetros são usados como unidade padrão.


## Formato de arquivo AMF

O formato de arquivo de manufatura aditiva (**AMF**) define padrões abertos para descrição de objetos para serem utilizados por processos de manufatura aditiva, como impressão 3D. Os programas CAD utilizam o formato de arquivo AMF fazendo uso das informações como geometria, cor e material dos objetos. AMF é diferente do formato STL, pois a lateral não suporta cores, materiais, treliças e constelações.

### Elementos de um arquivo AMF

Os cinco elementos de nível superior definidos com o<AMF> as tags estão detalhadas abaixo. A presença de um único elemento de objeto é obrigatória para um arquivo AMF totalmente funcional.

`<object> ` - O elemento object define um volume ou volumes de material, cada um dos quais está associado a um ID de material para impressão. Pelo menos um elemento de objeto deve estar presente no arquivo. Objetos adicionais são opcionais.

`<material> ` - O elemento material opcional define um ou mais materiais para impressão com um ID de material associado. Se nenhum elemento de material for incluído, um único material padrão será assumido.

`<texture> ` - O elemento de textura opcional define uma ou mais imagens ou texturas para mapeamento de cores ou texturas, cada uma com um ID de textura associado.

`<constellation> ` - O elemento de constelação opcional combina hierarquicamente objetos e outras constelações em um padrão relativo para impressão.

`<metadata> ` - O elemento de metadados opcional especifica informações adicionais sobre o(s) objeto(s) e os elementos contidos no arquivo.

## Exemplo AMF

A seguir está um exemplo de arquivo AMF que pode ser copiado para um arquivo [texto](/pt/word-processing/txt/) e salvo como arquivo compactado [zip](/pt/compression/zip/) para abertura.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Referências

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [especificações AMF sobre ISO](https://www.iso.org/standard/67472.html)

