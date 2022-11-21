{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo tiff", "formato de arquivo tiff", "o que é um arquivo tiff", "arquivo", "exemplo tiff", "extensão de arquivo tiff", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo TIFF e APIs que podem criar e abrir arquivos TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo TIFF?

TIFF ou TIF, Tagged Image File Format, representa imagens raster que se destinam ao uso em uma variedade de dispositivos que estão em conformidade com este padrão de formato de arquivo. Ele é capaz de descrever dados de imagem de dois níveis, tons de cinza, cores de paleta e cores em vários espaços de cores. Ele suporta esquemas de compactação com e sem perdas para escolher entre espaço e tempo para aplicativos que usam o formato. O formato não depende da máquina e está livre de limites como processador, sistema operacional ou sistemas de arquivos.

## Breve História do Formato de Arquivo TIFF

O formato de arquivo TIFF foi inicialmente criado pela Aldus Corporation no outono de 1986, após uma série de reuniões com vários fabricantes de scanners e desenvolvedores de software. O objetivo principal do formato de arquivo TIFF era fornecer um formato de arquivo de imagem digitalizada comum para todos os fornecedores de scanners de mesa. Começando com suporte apenas para o formato de imagem binário, o formato evoluiu para o suporte de imagens em tons de cinza e coloridas com o passar do tempo. A versão inicial das especificações de formato de arquivo TIFF pode ser rotulada como Reivision 3.0, pois havia duas versões preliminares anteriores. Uma grande revisão 5.0 foi publicada em 1988 que adicionou suporte para imagens de cores de paleta e compressão LZW. A revisão 6.0 dos formatos de arquivo TIFF foi publicada em 1992 depois disso. Em 1994, a Adobe Systems adquiriu a Aldus e as especificações agora estão disponíveis e mantidas pela Adobe Systems.

## Especificações de formato de arquivo TIFF

O formato de arquivo TIFF é extensível e passou por várias revisões que permitem a inclusão de uma quantidade ilimitada de informações privadas ou para fins especiais. Um arquivo TIFF começa com um cabeçalho de 8 bytes onde os bytes são números de 0 a N. O maior arquivo TIFF possível tem 2**32 bytes de comprimento. O arquivo começa com um cabeçalho de arquivo de imagem de 8 bytes que aponta diretamente para um arquivo de imagem (IFD). Um IFD contém informações sobre a imagem, bem como ponteiros para os dados reais da imagem.

### Cabeçalho do arquivo TIFF

O cabeçalho do arquivo TIFF de 8 bytes contém as seguintes informações:

**Bytes 0-1:** a ordem de bytes usada no arquivo. Os valores legais são:“II”(4949.H)“MM” (4D4D.H).

No formato “II”, a ordem dos bytes é sempre do byte menos significativo para o byte mais significativo, para inteiros de 16 bits e 32 bits. Isso é chamado de ordem de bytes little-endian. No formato “MM”, a ordem dos bytes é sempre do mais significativo para o menos significativo, tanto para inteiros de 16 bits quanto de 32 bits. Isso é chamado de ordem de bytes big-endian.

**Bytes 2-3:** Um número arbitrário, mas cuidadosamente escolhido (42) que identifica ainda mais o arquivo como um arquivo TIFF. A ordem dos bytes depende do valor dos Bytes 0-1.

**Bytes 4-7:** O deslocamento (em bytes) do primeiro IFD. O diretório pode estar em qualquer local no arquivo após o cabeçalho, mas deve começar em um limite de palavra. Em particular, um diretório de arquivos de imagem pode seguir os dados de imagem que descreve. Os leitores devem seguir os ponteiros onde quer que eles levem. O termo deslocamento de byte é sempre usado neste documento para se referir a um local em relação ao início do arquivo TIFF. O primeiro byte do arquivo tem um deslocamento de 0.

### Diretório de arquivos de imagem

Um IFD contém informações sobre a imagem, bem como ponteiros para os dados reais da imagem. , seguido por um deslocamento de 4 bytes do próximo IFD (ou 0 se nenhum). Deve haver pelo menos 1 IFD em um arquivo TIFF e cada IFD deve ter pelo menos uma entrada.

#### Entrada IFD

Cada entrada IFD de 12 bytes está no formato a seguir.


|Bytes|Descrição
---|---|
|0-1|A Tag que identifica o campo
|2-3|O tipo de campo
|4-7|Contagem do tipo indicado
|8-11|O Deslocamento do Valor, o deslocamento do arquivo (em bytes) do Valor para o campo. Espera-se que o Valor comece em um limite de palavra; o Deslocamento de Valor correspondente será, portanto, um número par. Este deslocamento de arquivo pode apontar para qualquer lugar no arquivo, mesmo após os dados da imagem

Um campo TIFF é uma entidade lógica que consiste na tag TIFF e seu valor. Este conceito lógico é implementado como uma Entrada IFD, mais o valor real caso não se enquadre na parte valor/deslocamento, os últimos 4 bytes da Entrada IFD. Os termos campo TIFF e entrada IFD são intercambiáveis na maioria dos contextos.

### TIFF de linha de base ###

O TIFF de linha de base é o núcleo do TIFF, o essencial que todos os desenvolvedores de TIFF convencionais devem oferecer suporte em seus produtos. A conformidade com o formato TIFF está sujeita ao cumprimento dos requisitos de Baseline TIFF. Esses requisitos estão bem documentados no documento de especificações 6.0.

#### Várias imagens por arquivo ####

Pode haver mais de um IFD em um arquivo TIFF. Cada IFD define um subarquivo. Um uso potencial de subarquivos é descrever imagens relacionadas, como as páginas de uma transmissão de fac-símile. Um leitor Baseline TIFF não é necessário para ler nenhum IFD além do primeiro.

#### Tipos de imagem ####

A imagem TIFF de linha de base tem os seguintes tipos:

**Bilevel:** uma imagem de dois níveis contém duas cores: preto e branco. TIFF permite que um aplicativo grave dados de dois níveis em um formato branco é zero ou preto é zero. O campo que registra essas informações chama-se **PhotometricInterpretation**.

* RGB colorido

As informações de PhotometricInterpretation para imagens Bilevel são as seguintes:

Etiqueta = 262 (106.H)
Tipo = CURTO
**Valores**

|Valor|Descrição|
---|---|
|0|Para imagens de dois níveis e tons de cinza: 0 é representado como branco. O valor máximo é representado em preto. Este é o valor normal para Compression#2|
|1|PretoIsZero. Para imagens de dois níveis e em tons de cinza: 0 é representado como preto. O valor máximo é representado como branco. Se esse valor for especificado para Compression#2, a imagem deverá ser exibida e impressa invertida.|

**GrayScale:** imagens em tons de cinza são uma generalização de imagens de dois níveis. Imagens de dois níveis podem armazenar apenas dados de imagem em preto e branco, mas imagens em tons de cinza também podem armazenar tons de cinza. Para descrever tais imagens, você deve adicionar ou alterar os seguintes campos. Os outros campos obrigatórios são os mesmos necessários para imagens de dois níveis. Para imagens em tons de cinza, Compression # 1 ou 32773 (PackBits). No Baseline TIFF, as imagens em tons de cinza podem ser armazenadas como dados não compactados ou compactadas com o algoritmo PackBits.

As informações de **BitsPerSample** para imagens em tons de cinza são as seguintes:

Etiqueta = 258 (102.H)
Tipo = CURTO

O número de bits por componente. Os valores permitidos para imagens em escala de cinza TIFF de linha de base são 4 e 8, permitindo 16 ou 256 tons de cinza distintos.

**Cor da paleta:** imagens de cores da paleta são semelhantes às imagens em tons de cinza. Eles ainda têm um componente por pixel, mas o valor do componente é usado como um índice em uma tabela de pesquisa RGB completa. Para descrever essas imagens, você precisa adicionar ou alterar os campos a seguir. Os outros campos obrigatórios são os mesmos das imagens em tons de cinza.
As informações de PhotometricInterpretation para a imagem Palette-Color são as seguintes:

Interpretação Fotométrica = 3 (Cor da Paleta).
ColorMapTag = 320 (140.H)
Tipo = CURTO
N = 3 * (2 bits por amostra)

Este campo define um mapa de cores Vermelho-Verde-Azul (geralmente chamado de tabela de pesquisa) para imagens de cores da paleta. Em uma imagem de cores de paleta, um valor de pixel é usado para indexar em uma tabela de pesquisa RGB. Por exemplo, um pixel de cor de paleta com valor 0 seria exibido de acordo com o 0º trio Vermelho, Verde e Azul. No ColorMap, o preto é representado por 0,0,0 e o branco é representado por 65535, 65535, 65535.

**RGB colorido:** em uma imagem RGB, cada pixel é composto por três componentes: vermelho, verde e azul. Não há ColorMap. Para descrever uma imagem RGB, você precisa adicionar ou alterar os seguintes campos e valores. Os outros campos obrigatórios são os mesmos necessários para imagens de cores de paleta.

BitsPorAmostra = 8,8,8. Cada componente tem 8 bits de profundidade em uma imagem Baseline TIFF RGB.

PhotometricInterpretation = 2 (RGB) e não há ColorMap.

Etiqueta = 277 (115.H)
Tipo = CURTO
O número de componentes por pixel. Esse número é 3 para imagens RGB, a menos que amostras extras estejam presentes.

## Referências ##

* [Formato de arquivo TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

