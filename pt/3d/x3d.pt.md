{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo x3d", "formato de arquivo x3d", "o que é um arquivo x3d", "arquivo", "exemplo x3d", "extensão de arquivo x3d", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - Arquivo de imagem 3D",
  "description":"Saiba mais sobre o formato de arquivo X3D e APIs que podem abrir e criar arquivos X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo X3D?
X3D é um formato de arquivo gráfico 3D baseado em [XML](/pt/web/xml/) para apresentação de informações 3D. É um padrão modular e é definido através de várias especificações ISO. O formato suporta gráficos vetoriais e raster, transparência, efeitos de iluminação e configurações de animação, incluindo rotações, fades e oscilações. Tornou-se o sucessor do formato de arquivo [VRML](/pt/3d/vrml/) em 2001. O X3D tem a vantagem de codificar informações de cores (diferentemente de [STL](/pt/cad/stl/)) que é usado durante a impressão do modelo em uma cor impressora 3d. O formato apresenta extensões para VRML, fornecendo a capacidade de codificar a cena usando uma sintaxe XML, bem como a sintaxe semelhante ao Open Inventor de VRML97 ou formatação binária.

A especificação abstrata para X3D (ISO/IEC 19775) foi aprovada pela ISO em 2004. As codificações XML e ClassicVRML para X3D (ISO/IEC 19776) foram aprovadas pela primeira vez em 2005.

## Formato de arquivo X3D

Os arquivos de cena X3D têm uma estrutura de arquivo comum:

* Cabeçalho do arquivo (XML, ClassicVRML ou binário compactado)
* Início do nó raiz X3D, incluindo atributos de versão e perfil
* Uma seção principal com instruções Component e Meta (ambas opcionais)
* O gráfico da cena X3D e seus nós filhos
* Fim do nó raiz X3D

## Exemplo de formato de arquivo X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## Referências ##

* [X3D - Por Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Site oficial do Consórcio Web3D](http://www.web3d.org/)
* [site oficial do X3D](http://www.web3d.org/x3d/what-x3d)

