{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo gif", "formato de arquivo gif", "o que é um arquivo gif", "arquivo", "exemplo gif", "extensão de arquivo gif", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GIF - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo GIF e APIs que podem criar e abrir arquivos GIF.",
  "linktitle" : "GIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GIF? ##

Um GIF ou Graphical Interchange Format é um tipo de imagem altamente compactada. De propriedade da Unisys, o GIF usa o algoritmo de compactação LZW que não degrada a qualidade da imagem. Para cada imagem, o GIF normalmente permite até 8 bits por pixel e até 256 cores são permitidas na imagem. Em contraste com uma imagem [JPEG](/pt/image/jpeg/), que pode exibir até 16 milhões de cores e atinge os limites do olho humano. Quando a internet surgiu, os GIFs continuaram sendo a melhor escolha porque exigiam baixa largura de banda e compatível com os gráficos que consomem áreas sólidas de cor. Um GIF animado combina várias imagens ou quadros em um único arquivo e os exibe em uma sequência para gerar um clipe animado ou um vídeo curto. As limitações de cores são de até 256 para cada quadro e provavelmente serão as menos adequadas para reproduzir outras imagens e fotografias com gradiente de cores.

## Formato de arquivo GIF ##

Conceitualmente, os arquivos GIF têm uma área gráfica de tamanho fixo preenchida por zero ou mais imagens. Alguns arquivos GIF dividem a área gráfica ou blocos de tamanho fixo em sub-imagens capazes de funcionar como quadros animados no caso de GIF animado. O formato GIF usa as profundidades de pixel de 1 a 8 bits para armazenar os dados de bitmap. O modelo de cores RGB e os dados da paleta são sempre usados para armazenar as imagens. Dependendo da versão, um cabeçalho de tamanho fixo ("GIF87a" ou "GIF89a") define o início de um arquivo GIF típico.

Atualmente, duas versões do GIF: 87a e 89a estão disponíveis. O primeiro é o formato GIF original, enquanto o último é o novo formato GIF. Nesse formato de arquivo, as características dos blocos e as dimensões dos pixels são mencionadas em um Descritor de Tela Lógica de tamanho fixo. A existência e o tamanho de uma Tabela Global de Cores podem ser especificados pelo descritor de tela, que rastreia mais detalhes se houver. O trailer é o último byte do arquivo que contém um único byte de um ponto e vírgula ASCII. Um layout de arquivo GIF87a típico é o seguinte:

### Cabeçalho ###

O Header contém seis bytes e é usado para especificar o tipo de arquivo como GIF. Embora o Descritor de Tela Lógica seja separado do cabeçalho real, às vezes ele é considerado como o segundo cabeçalho. A mesma estrutura que é usada para armazenar o cabeçalho pode armazenar o Descritor de Tela Lógica. Todos os arquivos GIF começam com a assinatura de 3 bytes e usam os caracteres “GIF” como identificador. A versão também tem três bytes de tamanho e declara a versão do arquivo GIF.

### Descritor de tela lógica ###

Um descritor de imagem de comprimento fixo especifica a tela e as informações de cor necessárias para criar a imagem GIF. Os campos Altura e Largura incluem o menor valor de resolução da tela, obrigatório para mostrar os dados da imagem. Se o dispositivo de exibição for incapaz de exibir a resolução especificada, será necessário dimensionar para exibir a imagem adequadamente. As informações de tela e mapa de cores são exibidas pelos quatro subcampos da tabela abaixo (enquanto o bit 0 é o bit menos significativo):


|Bits|Subcampos
---|---|
|0-2|Tamanho da tabela de cores global
|3|Sinalizador de classificação da tabela de cores
|4-6|Resolução de cores
|7|Bandeira de tabela de cores global

#### Tabela Global de Cores ####

Uma Tabela de Cores Global opcional é colocada logo após o Descritor de Tela Lógica. Esta tabela mapeada para indexar os dados de cor do pixel dentro dos dados da imagem. Na ausência de uma tabela de cores global, cada imagem no arquivo GIF usa sua cor local. É melhor fornecer uma tabela de cores padrão se a Tabela de cores global e local estiver ausente. Uma série de triplos de três bytes compõe os elementos da tabela de cores. Cada byte caracteriza um valor de cor RGB. As cores vermelha, verde e azul são utilizadas como valores de cada elemento da tabela de cores. As entradas na Tabela Global de Cores atingem no máximo 256 entradas e sempre representam em potência de dois.

#### Dados de imagem ####

Os dados de imagem armazenam um byte de símbolos não codificados seguidos por uma lista encadeada de sub- junto com os dados codificados em LZW.

#### Reboque ####

Trailer representa um único byte de dados que é o último caractere no arquivo. O valor deste byte é permanentemente 3Bh e especifica o fim do fluxo de dados. Todo arquivo GIF deve ter o trailer no final de cada arquivo.

## Referências ##

* [formato de arquivo GIF](https://en.wikipedia.org/wiki/GIF)

