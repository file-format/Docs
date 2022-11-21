{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Formato de arquivo", "CAD", "Abrir", "Criar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo DWG e APIs que podem criar e abrir arquivos DWG.",
  "title" :"Formato de arquivo DWG",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DWG?

Arquivos com extensão DWG representam arquivos binários proprietários usados para conter dados de projeto 2D e 3D. Assim como DXF, que são arquivos ASCII, DWG representa o formato de arquivo binário para desenhos CAD (Computer Aided Design). Contém imagem vetorial e metadados para representação do conteúdo de arquivos CAD. Existem visualizadores gratuitos disponíveis para visualização de arquivos DWG no sistema operacional Windows, como o DWG TrueView gratuito da Autodesk. Existem outros aplicativos de terceiros que suportam o acesso a arquivos DWG. Os arquivos DWG contêm informações criadas pelo usuário e incluem:

* Projetos
* Dados geométricos
* Mapas e fotos

Este formato é amplamente utilizado por arquitetos, engenheiros e designers para vários propósitos de projeto.

## Breve história ##

O formato de arquivo DWG evoluiu com o tempo desde sua introdução formal em 1982. Uma breve visão geral dos eventos passados da perspectiva histórica é a seguinte.

**1982:** A Autodesk licenciou o formato de arquivo DWG , que foi desenvolvido por Mike Riddle em 1970, como base para o AutoCAD.

**1998:** Com o lançamento do AutoCAD R14.01, a Autodesk adicionou a verificação de arquivos por meio de uma função chamada DWGCHECK, que incorporava uma soma de verificação criptografada e um código de produto, chamado WaterMark pela Autodesk, em arquivos DWG criados pelo programa.

**2006:** A Autodesk modificou o AutoCAD 2007 para incluir a "tecnologia TrustedDWG" para incorporar a string de texto "Autodesk DWG. Este arquivo é um DWG confiável salvo pela última vez por um aplicativo Autodesk ou aplicativo licenciado da Autodesk" nos arquivos DWG. O objetivo disso era ajudar os usuários do software Autodesk a garantir que esses arquivos fossem criados por um aplicativo Autodesk ou RealDWG, o que definitivamente deve ajudar a reduzir o risco de incompatibilidades.

## Estrutura do arquivo ##

DWG tem sido um dos formatos de arquivo amplamente utilizados por uma variedade de aplicativos e possui uma estrutura de arquivo robusta. Como o DWG é um formato de arquivo binário, ele não é legível por humanos como o formato de arquivo ASCII [DXF](/pt/cad/dxf/) simples. Os arquivos DWG geralmente incluem informações sobre as coordenadas da imagem e quaisquer metadados associados a ela. [especificações](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) completas do formato de arquivo DWG estão disponíveis para download pela OpenDesign. A estrutura de arquivo do formato de arquivo DWG é resumida a seguir.

**Cabeçalho**: O cabeçalho do arquivo consiste em variáveis de cabeçalho DWG e informações sobre Verificação de redundância cíclica (CRC) que é usada para a detecção de erros. Cada subseção é um vetor especializado onde diferentes comprimentos de bits são usados para representar diferentes rótulos. Por exemplo, os primeiros 6 bits da variável DWG Header representam a string de versão.

**Definições de classe:** Um arquivo DWG pode conter várias classes dependendo da finalidade específica do arquivo .dwg. Informações como tamanho dos metadados da classe da área de dados da classe, número da classe e soma de verificação, além de outras.

**Modelo**: Isso é opcional e para as versões R15 e R15, esta seção está abaixo da seção Espaço Livre do Objeto.

**Preenchimento**: Os metadados são sufixados e pós-fixados com um número específico de bytes, o que torna as versões mais antigas do software AutoCAD compatíveis com o novo formato de arquivo DWG.

**Image Data**: Os metadados para esta seção dependem do tipo .dwg específico. Para usuários R14 e R15, esta seção é opcional.

**Dados do objeto**: Os dados do objeto consistem em uma lista completa de entidades de tabela, entradas de dicionário, etc. correspondentes à lista de objetos existente.

**Mapa de Objetos**: A localização de cada objeto no arquivo é especificada nesta seção do arquivo. A maioria dos metadados nesta seção são identificadores de arquivo que desempenham um papel na identificação e renderização do objeto.

**Espaço livre de objetos**: esta seção é opcional para todos os usuários

**Segundo Cabeçalho**: uma duplicata da seção do cabeçalho do arquivo no final do arquivo DWG

## Referências ##

* [Especificações de formato de arquivo DWG](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [A especificação do arquivo DWG](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - Por Wikipedia](https://en.wikipedia.org/wiki/.dwg)

