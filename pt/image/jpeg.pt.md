{
  "date" : "2019-11-25",
  "keywords" :[ "arquivo jpeg", "formato de arquivo jpeg", "o que é um arquivo jpeg", "arquivo", "exemplo jpeg", "extensão de arquivo jpeg", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPEG - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo JPEG e APIs que podem criar e abrir arquivos JPEG.",
  "linktitle" : "JPEG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-08"
}

## O que é um arquivo JPEG? ##

Um JPEG é um tipo de formato de imagem que é salvo usando o método de compactação com perdas. A imagem de saída, como resultado da compactação, é uma compensação entre o tamanho do armazenamento e a qualidade da imagem. Os usuários podem ajustar o nível de compactação para atingir o nível de qualidade desejado e, ao mesmo tempo, reduzir o tamanho do armazenamento. A qualidade da imagem é afetada de forma insignificante se a compressão 10:1 for aplicada à imagem. Quanto maior o valor de compactação, maior a degradação na qualidade da imagem.

## Especificações de formato de arquivo ##

O formato de arquivo de imagem JPEG foi padronizado pelo Joint Photographic Experts Group e, portanto, o nome JPEG. O formato tem sido a escolha de armazenamento e transmissão de imagens fotográficas na web. Quase todos os sistemas operacionais agora têm visualizadores que suportam a visualização de imagens JPEG, que geralmente também são armazenadas com extensão JPG. Até os navegadores da web suportam a visualização de imagens JPEG. Antes de entrar nas especificações do formato de arquivo JPEG, o processo geral das etapas envolvidas na criação do JPEG precisa ser mencionado.

### Etapas de compactação JPEG ###

**Transformação:** as imagens coloridas são transformadas de RGB em uma imagem de luminância/crominância (o olho é sensível à luminância, não à crominância, de modo que a parte de crominância pode perder muitos dados e, portanto, pode ser altamente compactada.

**Amostragem descendente:** A amostragem descendente é feita para o componente colorido e não para o componente de luminância. A amostragem descendente é feita na proporção 2:1 horizontalmente e 1:1 verticalmente (2h 1 V). Assim, a imagem reduz de tamanho, uma vez que o componente 'y' não é tocado, não há perda perceptível de qualidade de imagem.

**Organização em grupos:** os pixels de cada componente de cor são organizados em grupos de 8 × 2 pixels chamados "unidades de dados" se o número de linhas ou colunas não for múltiplo de 8, a linha inferior e as colunas mais à direita serão duplicadas.

**Transformação de Cosseno Discreta:** A Transformação de Cosseno Discreta (DCT) é então aplicada a cada unidade de dados para criar um mapa 8×8 de componentes transformados. A DCT envolve alguma perda de informação devido à precisão limitada da aritmética do computador. Isso significa que mesmo sem o mapa haverá alguma perda de qualidade de imagem, mas normalmente é pequena.

**Quantização:** cada um dos 64 componentes transformados na unidade de dados é dividido por um número separado chamado "Coeficiente de quantização (QC)" e arredondado para um número inteiro. É aqui que a informação é perdida irremediavelmente, o CQ grande causa mais perda. Em geral, a maioria dos implementos JPEG permite o uso de tabelas de CQ recomendadas pelo padrão JPEG.

**Codificação:** Os 64 coeficientes transformados quantizados (que agora são inteiros) de cada unidade de dados são codificados usando uma combinação de codificação RLE e Huffman.

**Adicionando cabeçalho:** a última etapa adiciona o cabeçalho e todos os parâmetros JPEG usados e gera o resultado.

O decodificador JPEG usa as etapas inversas para gerar a imagem original a partir da compactada.

### Estrutura do arquivo ###

Uma imagem JPEG é representada como uma sequência de segmentos onde cada segmento começa com um marcador. Cada marcador começa com o byte 0xFF seguido pelo sinalizador do marcador para representar o tipo de marcador. A carga útil seguida pelo marcador é diferente de acordo com o tipo de marcador. Os tipos comuns de marcadores JPEG estão listados abaixo:

|Nome abreviado|Bytes|Carga útil|Nome|Comentários
---|---|---|---|---|
|SOI|0xFF, 0xD8|nenhum|Início da imagem|
|S0F0|0xFF, 0xC0|tamanho variável|Início do quadro|
|S0F2|0xFF, 0xC2|tamanho variável|Iniciar quadro|
|DHT|0xFF, 0xC4|tamanho variável|Definir tabelas Huffman|
|DQT|0xFF, 0xDB|tamanho da variável|Definir Tabela(s) de Quantização|
|DRI|0xFF, 0xDD|4 bytes|Definir intervalo de reinicialização|
|SOS|0xFF, 0xDA|tamanho variável|Início da verificação|
|RSTn|0xFF, 0xD//n//(/pt//n//#0..7)|nenhum|Reiniciar|
|APPn|0xFF, 0xE//n//|tamanho da variável|Especifico do aplicativo|
|COM|0xFF, 0xFE|tamanho variável|Comentário|
|EOI|0xFF, 0xD9|nenhum|Fim da imagem|

Dentro dos dados codificados por entropia, após qualquer byte 0xFF, um byte 0x00 é inserido pelo codificador antes do byte seguinte, para que não pareça haver um marcador onde não se pretenda nenhum, evitando erros de enquadramento. Os decodificadores devem pular este byte 0x00. Essa técnica, chamada [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (consulte a seção de especificação JPEG F.1.2.3), é aplicada apenas aos dados codificados por entropia, não aos dados de carga útil do marcador . Observe, no entanto, que os dados codificados por entropia têm alguns marcadores próprios; especificamente os marcadores Reset (0xD0 a 0xD7), que são usados para isolar pedaços independentes de dados codificados por entropia para permitir a decodificação paralela, e os codificadores são livres para inserir esses marcadores Reset em intervalos regulares (embora nem todos os codificadores façam isso).

