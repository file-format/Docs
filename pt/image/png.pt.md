{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo png", "formato de arquivo png", "o que é um arquivo png", "arquivo", "exemplo png", "extensão de arquivo png","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PNG - arquivo de imagem raster",
  "description":"Saiba mais sobre o formato de arquivo PNG e APIs que podem criar e abrir arquivos PNG.",
  "linktitle" : "PNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PNG?

Um arquivo **PNG** (Portable Network Graphics) é um formato de arquivo de imagem raster que usa compactação sem perdas. Este formato de arquivo foi criado como uma substituição do Graphics Interchange Format ([GIF](/pt/image/gif/)) e não tem limitações de direitos autorais. No entanto, o formato de arquivo PNG não suporta animações. O formato de arquivo PNG suporta compressão de imagem sem perdas que o torna popular entre seus usuários. Com o passar do tempo, o PNG evoluiu como um dos formatos de arquivo de imagem amplamente utilizados.

## Breve História do Formato de Arquivo PNG

A principal razão por trás da criação do formato de arquivo PNG foi o algoritmo de compressão patenteado, Lempel-Ziv-Welch, usado no formato de arquivo GIF. Isso, juntamente com outras limitações de GIF, criou a necessidade de substituição do formato de arquivo [**GIF**](/pt/image/gif/). A primeira proposta e nome para o formato de arquivo PNG veio em janeiro de 1995. Os principais eventos relacionados aos formatos de arquivo PNG estão listados abaixo:

* Outubro de 1996: as especificações do PNG Versão 1.0 foram lançadas e mais tarde apareceram como [RFC](https://en.wikipedia.org/wiki/Request_for_Comments) 2083. O mesmo se tornou uma Recomendação do W3C em outubro de 1996.
* Dezembro de 1998: A versão 1.1, com algumas pequenas mudanças e a adição de três novos pedaços, foi lançada.
* Agosto de 1999: A versão 1.2, adicionando um pedaço extra, foi lançada.
* Novembro de 2003: PNG tornou-se uma Norma Internacional (ISO/IEC 15948:2003). Esta versão do PNG difere apenas ligeiramente da versão 1.2 e não adiciona novos pedaços.
* Março de 2004: ISO/IEC 15948:2004

## Comparação funcional de GIF e PNG

O formato de arquivo PNG foi projetado para ser simples e portátil, legalmente desimpedido, intercambiável, flexível e robusto. A tabela a seguir lista os recursos GIF que são herdados pelo formato de arquivo PNG, além dos novos recursos.

|Recurso|GIF|PNG|
---|---|---|
|Imagens em cores de índice de até 256 cores|Sim|Sim|
|Suporte para streaming|Sim|Sim|
|Transparência|Sim|Sim|
|Informações auxiliares|Sim|Sim|
|Independência de hardware e plataforma|Sim|Sim|
|Eficaz|Sim|Sim|
|Imagens Truecolor de até 48 bits por pixel|Não|Sim|
|Imagens em tons de cinza de até 16 bits por pixel|Não|Sim|
|Canal alfa completo (máscaras de transparência geral)|Não|Sim|
|Informações de gama da imagem|Não|Sim|
|Confiabilidade|Não|Sim|
|Apresentação inicial mais rápida|Não|Sim|

## Estrutura do arquivo PNG

Quase todos os sistemas operacionais têm suporte para abrir arquivos PNG. Por exemplo, o visualizador do Microsoft Windows tem a capacidade de abrir arquivos PNG, pois o sistema operacional tem, por padrão, o suporte disponível como parte da instalação. Um arquivo PNG consiste em uma `assinatura` PNG seguida por uma série de //pedaços//.

### Cabeçalho do arquivo PNG

Os primeiros oito bytes de um arquivo PNG sempre contêm os seguintes valores (decimais):

{{{137 80 78 71 13 10 26 10 }}}

Essa assinatura indica que o restante do arquivo contém uma única imagem PNG, consistindo em uma série de partes começando com uma parte IHDR e terminando com uma parte IEND.

### Pedaços ###

Cada pedaço consiste em quatro partes:

**Length:** um inteiro sem sinal de 4 bytes que fornece o número de bytes no campo de dados do bloco. O comprimento conta apenas o campo de dados, não ele mesmo, o código do tipo de bloco ou o CRC. Zero é um comprimento válido. Embora codificadores e decodificadores devam tratar o comprimento como sem sinal, seu valor não deve exceder 231 bytes.

**Tipo de fragmento:** um código de tipo de fragmento de 4 bytes. Por conveniência na descrição e no exame de arquivos PNG, os códigos de tipo são restritos a consistir em letras ASCII maiúsculas e minúsculas (AZ e az, ou 65-90 e 97-122 decimal). No entanto, codificadores e decodificadores devem tratar os códigos como valores binários fixos, não como cadeias de caracteres. Por exemplo, não seria correto representar o código de tipo IDAT pelos equivalentes EBCDIC dessas letras. Convenções de nomenclatura adicionais para tipos de blocos são discutidas na próxima seção.

**Dados do fragmento:** os bytes de dados apropriados ao tipo do fragmento, se houver. Este campo pode ter comprimento zero.

**CRC:** um CRC (Cyclic Redundancy Check) de 4 bytes calculado nos bytes anteriores no bloco, incluindo o código do tipo de bloco e os campos de dados do bloco, mas não incluindo o campo de comprimento. O CRC está sempre presente, mesmo para blocos que não contêm dados.

O comprimento dos dados do bloco pode ser qualquer número de bytes até o máximo; portanto, os implementadores não podem assumir que os pedaços estão alinhados em quaisquer limites maiores que bytes.

Os pedaços podem aparecer em qualquer ordem, sujeitos às restrições impostas a cada tipo de pedaço. (Uma restrição notável é que IHDR deve aparecer primeiro e IEND deve aparecer por último; portanto, o bloco IEND serve como um marcador de fim de arquivo.) Vários blocos do mesmo tipo podem aparecer, mas somente se permitido especificamente para esse tipo.

#### Tipos de pedaços

Os tipos de bloco são categorizados em blocos **críticos** e **auxiliares** com base no valor ASCII com diferenciação de maiúsculas e minúsculas de 4 bytes atribuído ao tipo de bloco. Todas as implementações devem entender e renderizar com sucesso os fragmentos críticos padrão. Uma imagem PNG válida deve conter um fragmento IHDR, um ou mais fragmentos IDAT e um fragmento IEND.

### Compressão

O método de compactação PNG 0 (o único método de compactação atualmente definido para PNG) especifica a compactação deflate/inflate com uma janela deslizante de no máximo 32.768 bytes. A compressão Deflate é um derivado do LZ77 usado em zip, gzip, pkzip e programas relacionados. Uma extensa pesquisa foi feita apoiando seu status livre de patentes. Os dados compactados no fluxo de dados zlib são armazenados como uma série de blocos, cada um dos quais pode representar dados brutos (não compactados), dados compactados LZ77 codificados com códigos Huffman fixos ou dados compactados LZ77 codificados com códigos Huffman personalizados. Um bit marcador no bloco final o identifica como o último bloco, permitindo que o decodificador reconheça o final do fluxo de dados compactado.

#### Filtragem de pré-compressão

Filtros de pré-compressão são aplicados para preparar os dados da imagem para a compressão ideal. O método de filtro PNG define cinco tipos básicos de filtro da seguinte forma:

|Tipo de filtro|Nome|Valor previsto|
---|---|---|
|0|Nenhum|A linha de varredura é transmitida sem modificação|
|1|Sub|Transmite a diferença entre cada byte e o valor do byte correspondente do pixel anterior.|
|2|Up|O filtro Up() é como o filtro Sub(), exceto que o pixel imediatamente acima do pixel atual, em vez de apenas à sua esquerda, é usado como preditor.|
|3|Average|O filtro Average() usa a média dos dois pixels vizinhos (esquerda e acima) para prever o valor de um pixel.|
|4|Paeth|O filtro Paeth() calcula uma função linear simples dos três pixels vizinhos (esquerda, acima, superior esquerdo), então escolhe como preditor o pixel vizinho mais próximo do valor calculado.|

Os algoritmos de filtragem são aplicados a 'bytes', não a pixels, independentemente da profundidade de bits ou do tipo de cor da imagem. Os algoritmos de filtragem trabalham na sequência de bytes formada por uma linha de varredura. Se a imagem incluir um canal alfa, os dados alfa serão filtrados da mesma forma que os dados da imagem.

Quando a imagem é entrelaçada, cada passagem do padrão entrelaçado é tratada como uma imagem independente para fins de filtragem. Os filtros funcionam nas sequências de bytes formadas pelos pixels realmente transmitidos durante uma passagem, e a "linha de varredura anterior" é aquela transmitida anteriormente na mesma passagem, não a adjacente na imagem completa. Observe que a subimagem transmitida em qualquer passagem é sempre retangular, mas tem largura e/ou altura menor que a imagem completa. A filtragem não é aplicada quando esta subimagem está vazia.

## Referências ##

* [PNG - Página inicial](http://www.libpng.org/pub/png/)

