{
  "date" : "2020-03-16",
  "keywords" :[ "Arquivo DXF", "Formato de arquivo", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DXF e as APIs que podem criar e abrir arquivos DXF.",
  "title" :"Formato de arquivo DXF",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DXF?

DXF, Drawing Interchange Format ou Drawing Exchange Format, é uma representação de dados marcados do arquivo de desenho do AutoCAD. Cada elemento no arquivo tem um número inteiro de prefixo chamado código de grupo. Esse código de grupo na verdade representa o elemento que segue e indica o significado de um elemento de dados para um determinado tipo de objeto. O DXF torna possível representar quase todas as informações especificadas pelo usuário em um arquivo de desenho.

O formato de arquivo DXF foi desenvolvido pela Autodesk como formato de arquivo de dados CAD para interoperabilidade de dados entre o AutoCAD e outros aplicativos. Assim, os dados podem ser importados de outros formatos para DXF para AutoCAD de acordo com as especificações de interoperabilidade do formato de arquivo DXF.

## Breve história ##


A história do formato de arquivo DXF remonta a 1982, quando foi introduzido como parte do AutoCAD 1.0. As versões iniciais do AutoCAD suportam apenas o formato de arquivo ASCII de DXF. Com a versão 10 do AutoCAD (e superior) em 1988, o suporte para o formato de arquivo ASCII e DXF binário foi introduzido no AutoCAD. Nos estágios anteriores, a Autodesk não compartilhava nenhuma especificação de formato de arquivo e, devido a isso, a importação correta de arquivos DXF não era fácil. No entanto, a Autodesk agora publica as especificações DXF e está disponível para o público em geral.

## Especificações de formato de arquivo ##

O formato de arquivo DXF usa os pares de código e valor de grupo para organizar o conteúdo em seções. Cada seção é composta de registros onde cada registro consiste em um código de grupo e item de dados. Cada código e valor de grupo estão em sua própria linha no arquivo DXF. Cada seção começa com um código de grupo 0 seguido pela string SECTION. Isso é seguido por um código de grupo 2 e uma string indicando o nome da seção (por exemplo, SECTION1). Cada seção é composta por códigos de grupo e valores que definem seus elementos. Uma seção termina com um 0 seguido pela string ENDSEC.

O formato de arquivo DXF considera objetos diferentes de entidades. Os objetos não têm representação gráfica aqui, mas as entidades a têm. Assim, as entradas em DXF são referidas como objetos gráficos, enquanto os objetos objetos são referidos como objetos não gráficos. As seções BLOCO e ENTIDADES do arquivo DXF contêm Entidades e o uso de códigos de grupo nessas duas seções é idêntico. O fim de uma entidade é indicado pelo próximo grupo 0, que inicia a próxima entidade ou indica o fim da seção.

### Estrutura do arquivo ###

As seções em um arquivo DXF são organizadas na seguinte ordem:

|Seção|Descrição básica
---|---|
|Cabeçalho|Esta seção contém informações gerais sobre o desenho. É como a funcionalidade Configurações do seu telefone, que contém as diferentes variáveis associadas ao desenho e seus valores associados. Por exemplo, a seção Cabeçalho definirá qual versão do AutoCAD o arquivo DXF usa (a variável $ACADVER) ou a unidade usada para medir os ângulos no arquivo (a variável $AUNITS)
|Classes|A seção CLASSES contém as informações para classes definidas pelo aplicativo cujas instâncias aparecem nas seções BLOCKS, ENTITIES e OBJECTS do banco de dados.
|Tabelas|Esta seção contém definições para várias tabelas diferentes, cada uma das quais contém várias entradas de símbolos diferentes. Por exemplo, o [tipo de linha](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A- 847B-5BBE36EC6FDF-htm.html) (LTYPE) define o padrão de traços, pontos, texto e símbolos no arquivo DXF e como eles são dimensionados. Aqui está uma lista completa de tabelas encontradas nesta seção:<ul><li> Tabela de ID do aplicativo (APPID)</li><li> Tabela de registro de bloco (BLOCK_RECORD)</li><li> Tabela de estilo de dimensão (DIMSTYPE)</li><li> Tabela de camadas (CAMADA)</li><li> Tabela de tipo de linha (LTYPE)</li><li> Tabela de estilo de texto (STYLE)</li><li> Tabela do Sistema de Coordenadas do Usuário (UCS)</li><li> Ver (VER) tabela</li><li> Tabela de configuração da janela de visualização (VPORT)</li></ul>
|Blocks|Esta seção contém os objetos gráficos e entidades de desenho que compõem cada referência de bloco no desenho.
|Entidades|Esta seção contém os dados reais do objeto e as entidades gráficas do desenho. Isso pode incluir dados brutos – por exemplo, uma entidade de círculo é definida por sua espessura, ponto central, raio e direção de extrusão.
|Objetos|Aqui, você encontrará as partes não gráficas do desenho. Por exemplo, os dicionários do AutoCAD são armazenados aqui.

## Referências ##

* [Especificações do arquivo DXF](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF pela Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)

