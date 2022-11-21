{
  "date" : "2021-08-16",
  "keywords" :[ "arquivo nrg", "formato de arquivo nrg", "o que é um arquivo nrg", "arquivo", "exemplo nrg", "extensão de arquivo nrg", "extensão", "formato", "rodapé nrg", "arquivo formato de nrg", "Nero Burning Rom", "Nero AG" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo NRG e as APIs que podem criar e abrir arquivos NRG.",
  "title" :"NRG - Formato de arquivo de imagem de disco",
  "linktitle" : "NRG",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-16"
}

## O que é um arquivo NRG?

Um formato de arquivo de imagem criado pelo uso de um disco óptico é considerado um formato de arquivo NRG. Este formato foi criado especificamente pelo Nero para o utilitário do Nero Burning Rom. Para o armazenamento de imagens de disco, considera-se que este formato é usado conforme apropriado para esses arquivos específicos. Esses arquivos podem estar na forma de uma cópia exata de um CD ou DVD ou podem ter vários arquivos que podem ser montados como um disco. Outros formatos de arquivo mais populares como os formatos de arquivo [ISO](/pt/compression/iso/) são aqueles nos quais esses arquivos podem ser convertidos em alguns utilitários básicos. Principalmente, os arquivos NRG são usados para criar backups ou cópias de alguns dados ou discos importantes.

## Formato de arquivo NRG ##

Este formato de arquivo foi desenvolvido pela Nero AG como um formato de imagem de disco. Ele tinha a propriedade específica do utilitário Nero Burning Rom, pois foi desenvolvido para armazenar imagens de disco. Sua primeira versão foi especificada para armazenar valores como inteiros de 32 bits. No entanto, sua segunda versão foi lançada e continha suporte para inteiros de 64 bits.

## Especificação técnica ##

No início do arquivo, esse formato não armazena seus dados como cabeçalho. Como um rodapé, ele é anexado no final do arquivo. Na forma de pedaços de IFF, as informações da imagem são armazenadas. O deslocamento do primeiro pedaço pode ser obtido lendo o rodapé NRG nos últimos 8 bytes a 12 bytes do arquivo. Em todas as versões do formato de arquivo NRG, há pedaços, DAOI, texto de CD, tipo de mídia de informações de sessão, informações de disco, Relo e final da cadeia anexado a ele. A ordem dos bytes é big-endian e todos os valores inteiros não têm sinal no momento do armazenamento.

### Partes principais ###

#### Folha de sugestões ####

Esta folha de sinalização está disponível facilmente em todas as versões de formato de arquivos NRG. A parte de **CUEX** significa os blocos de concatenação de tamanho fixo e cada um deles representa o ponto de sinalização.

#### Informações DAO ####

Esta informação também está presente em todas as versões do formato NRG. Os blocos de **DAOI** armazenam as informações específicas relevantes em 2 partes. Sua primeira parte consiste apenas nos dados específicos da sessão. Sua segunda parte apenas repete as informações cinza relacionadas ao rastreamento e é apenas uma vez para cada faixa.

#### CD-texto ####

Isso está disponível na segunda versão do NRG. A parte do **CDTX** consiste na concatenação bruta do pacote de texto de CD com 18 bytes para cada um.

#### Informações da faixa estendida ####

Isso está disponível em todas as versões do formato de arquivo do NRG. Esses blocos são utilizados para armazenar as informações de rastreamento para o rastreamento de sessões simultâneas. Esses dados são repetidos apenas uma vez no caso de cada faixa.

#### Informações da sessão ####

Isso também está disponível em todas as versões do formato de arquivo do NRG. As informações dos fragmentos de sessão precisam ser utilizadas para verificar a imagem da sessão rapidamente e, em seguida, rastrear a contagem.

#### Fim da cadeia ####

O pedaço de fim significa os sinais de que agora não há mais pedaços que precisam ser lidos e isso também está disponível em todas as versões do NRG.


## Referências ##

* [NRG - pela Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))


