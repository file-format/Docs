{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","arquivo", "formato", "tipo de arquivo", "extensão","o que é um arquivo ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo ASE e APIs que podem abrir e criar arquivos ASE.",
  "title" :"ASE - Arquivo de exportação de cena ASCII da Autodesk",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## O que é um arquivo ASE?

Um arquivo com extensão .ase é um formato de arquivo Autodesk ASCII Scene Export que é uma representação ASCII de uma cena, contendo informações 2D ou 3D ao exportar dados de cena usando o Autodesk. A Autodesk oferece opções para incluir componentes de cena ao exportar dados de cena. Você pode incluir definição de malha junto com informações de vértice e face, descrição de material, transformar dados de animação para os objetos, definição de malha completa de cada n quadros, dados de animação para câmeras e luzes e configurações de juntas IK.

## Formato de arquivo ASE - Mais informações

Os arquivos ASE são arquivos de texto armazenados no formato ASCII que podem ser abertos em qualquer editor de texto. Um arquivo ASE pode conter os seguintes tipos de informações fornecidas pela Autodesk.

### Opções de saída

* `Mesh Definition` - Exporta a definição de cada malha, incluindo informações de vértice e face para objetos geométricos. Além disso, ativar isso habilita os itens na caixa de grupo Mesh Options, descritos abaixo.
* `Materiais` - Inclui a descrição do material. Se um material não for atribuído a um objeto, sua cor de estrutura de arame será exportada. Todos os níveis de uma árvore de materiais estão incluídos, portanto, isso pode produzir muito texto.
* `Transform Animation Keys` - Inclui os dados de animação de transformação para os objetos. Se o objeto for uma câmera ou holofote de destino, isso incluirá dados de animação de destino.
* `Malha Animada` - Exporta uma definição de malha completa de cada n quadros. A frequência é especificada pelo spinner de saída do controlador, descrito abaixo. Cada bloco contém as mesmas informações especificadas na caixa de grupo Mesh Options, descrita abaixo. Ativar isso pode resultar em um arquivo enorme, mesmo para cenas pequenas.
* `Configurações de câmera/luz animadas` - Exporta os dados de animação para câmeras e luzes, como cor, intensidade, queda, polarização do mapa e assim por diante. Emite um bloco a cada n quadros, conforme especificado pelo girador de saída do controlador.
* `Inverse Kinematic Joints` - Exporta as configurações da junta IK na ramificação Hierarquia.

### Tipos de objeto

Os itens aqui permitem especificar qual categoria de objeto você deseja incluir na saída. Você pode incluir objetos geométricos, formas, câmeras, luzes e objetos auxiliares.

* Geométrico
* Formas
* Máquinas fotográficas
* Luzes
*Ajudantes

### Opções de malha

* `Mesh Normals` - Exporta as normais de face e vértice. A normal da face é listada primeiro, seguida pelas normais dos três vértices que suportam a face. Ativar isso resulta em um arquivo muito maior.
* `Mapping Coordinates` - Exporta uma lista de vértices e faces de mapeamento, de acordo com as estruturas TVert e TVFace descritas no 3ds Max Software Development Kit. Se um objeto usa mapeamento de face, uma lista de mapas de face é exportada contendo as coordenadas UVW para cada face.
* `Vertex Colors` - Exporta cores de vértices.

### Saída do controlador

* `Use Keys` - Exporta valores de chave. Se o controlador não usar chaves, o método Force Sample será usado. No caso de controladores de transformação, a opção Usar Chaves funciona somente se todos os controladores de transformação forem Linear/TCB ou Bezier. Se uma das trilhas de transformação usar um tipo diferente de controlador, o método Force Sample será usado para todas as trilhas de transformação.
* `Force Samples` - Amostra os valores do controlador com base na frequência especificada em Frames per Sample Controller.

## Referências

* [Autodesk - Exportando para ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

