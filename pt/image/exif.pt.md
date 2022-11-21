{
  "date" : "2019-10-11",
  "keywords" :[ "exif file", "exif file format", "o que é um exif file", "file", "exif example", "exif file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Saiba mais sobre o formato de arquivo EXIF e APIs que podem criar e abrir arquivos EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo EXIF?
EXIF significa “Exchangeable Image File Format”, a definição dada pela primeira vez pela [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) em 1985. O padrão é gerenciado pela Japan Electronics and Associação das Indústrias de Tecnologia da Informação (JEITA) a partir de hoje. EXIF é um padrão para especificações de formatos de imagem e som usados principalmente por câmeras digitais e scanners.

O padrão EXIF inclui as informações de marcação e metadados com o arquivo de imagem. Os metadados podem conter informações como modelo da câmera, velocidade do obturador, data e hora, abertura, fabricante, tempo de exposição, resolução X, resolução Y etc. Normalmente, os dados EXIF ficam ocultos por padrão. Para visualizar os dados EXIF, é preciso selecionar as propriedades de visualização no aplicativo de visualização de imagens. Os metadados Exif também podem incluir miniaturas junto com dados técnicos e de imagem primária em um único arquivo de imagem.

## Histórico e Versões ##

* Em outubro de 1995, a JEIDA estabeleceu a Versão 1. Nesta versão, a JEIDA definiu a estrutura, que consiste em formato de dados de imagem e informações de atributos e tags básicas.
* Em novembro de 1997, a versão 1.1 foi introduzida com a maioria das tags da versão 1, mas também adicionou provisões para informações de atributos opcionais e operação de formato.
* Junho de 1998, Versão 2 com espaço de cor sRGB, miniaturas compactadas e arquivos de áudio.
* Dezembro de 1998, Versão 2.1 com armazenamento aprimorado e informações de atributos.
* Fevereiro de 2002, Versão 2.2, versão 2.1 melhorada com adição de acabamento de impressão.
* Setembro de 2003, Versão 2.21 com espaço de cor opcional conhecido como Adobe RGB.

## Formato de arquivo EXIF

EXIF usa os seguintes formatos de arquivo com a adição de metadados específicos.

1. [JPEG](/pt/image/jpeg/) - transformação discreta de cosseno (DCT) para arquivos de imagem compactados.
1. [TIFF](/pt/image/tiff/) Rev. 6.0 (RGB ou YCbCr) para arquivos de imagem não compactados.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) para arquivos de áudio (Linear [PCM](https:/ /en.wikipedia.org/wiki/Pulse-code_modulation) ou ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM para dados de áudio não compactados e [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) para dados de áudio compactados).

### Marcador usado por EXIF ###

O marcador 0xFFE0~~0xFFEF é "Application Marker", usado pelo aplicativo do usuário. Por exemplo, câmeras digitais mais antigas usam JFIF (JPEG File Interchange Format) para armazenar imagens. JFIF usa o Marcador APP0 (0xFFE0) para inserir dados de configuração da câmera digital e imagem em miniatura. Além disso, EXIF também usa um marcador de aplicativo para inserir dados, mas EXIF usa o marcador APP1 (0xFFE1) para evitar um conflito com o formato JFIF. Todos os formatos de arquivo EXIF começam nesse formato.


|Marcador SOI|Marcador APP1|Dados APP1|Outro marcador
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Ele começa no marcador SOI (0xFFD8), portanto, é um arquivo JPEG. Então APP1 Marker segue imediatamente. Todos os dados do EXIF são armazenados nesta área de dados APP1. A parte de "SSSS" na tabela superior significa o tamanho da área de dados APP1 (área de dados EXIF). Observe que o tamanho "SSSS" também inclui o tamanho do próprio descritor. Após o "SSSS", os dados do APP1 são iniciados. A primeira parte é um dado especial para a identificação se EXIF ou não, são usados o caractere ASCII "EXIF" e 2 bytes de 0x00. Após a área do Marcador APP1, seguem os outros Marcadores JPEG.

### Estrutura de dados Exif ###

Uma estrutura aproximada de dados EXIF (APP1) é mostrada abaixo. Conforme discutido acima, os dados EXIF começam a partir do caractere ASCII "EXIF" e 2 bytes de 0x00, seguidos pelos dados EXIF. EXIF usa o formato TIFF para armazenar dados.


|FFE1|APP1 Marcador
---|---|
|SSSS|APP1 Data|APP1 Data Size
|45786966 0000|Cabeçalho Exif
|49492A00 08000000|Cabeçalho TIFF
|XXXX. . . .|IFD0 (imagem principal)|Diretório
|LLLLLLLL|Link para IFD1
|XXXX. . . .|Área de dados do IFD0
|XXXX. . . .|Exif SubIFD|Diretório
|00000000|Fim do link
|XXXX. . . .|Área de dados do Exif SubIFD
|XXXX. . . .|IFD1(imagem em miniatura)|Diretório
|00000000|Fim do link
|XXXX. . . .|Área de dados do IFD1
|FFD8XXXX. . . XXXXFFD9|Imagem em miniatura

#### Cabeçalho TIFF ####

O cabeçalho do arquivo [TIFF](/pt/image/tiff/) de 8 bytes contém as seguintes informações:

`Bytes 0-1:` A ordem de bytes usada no arquivo. Os valores legais são:“II”(4949.H)“MM” (4D4D.H).

No formato “II”, a ordem dos bytes é sempre do byte menos significativo para o byte mais significativo, para inteiros de 16 bits e 32 bits. Isso é chamado de ordem de bytes little-endian. No formato “MM”, a ordem dos bytes é sempre do mais significativo para o menos significativo, tanto para inteiros de 16 bits quanto de 32 bits. Isso é chamado de ordem de bytes big-endian.

`Bytes 2-3:` Um número arbitrário, mas cuidadosamente escolhido (42) que identifica o arquivo como um arquivo TIFF. A ordem dos bytes depende do valor dos Bytes 0-1.

`Bytes 4-7:` O deslocamento (em bytes) do primeiro IFD. O diretório pode estar em qualquer local no arquivo após o cabeçalho, mas deve começar em um limite de palavra. Em particular, um diretório de arquivos de imagem pode seguir os dados de imagem que descreve. Os leitores devem seguir os ponteiros onde quer que eles levem. O termo deslocamento de byte é sempre usado neste documento para se referir a um local em relação ao início do arquivo TIFF. O primeiro byte do arquivo tem um deslocamento de 0.

#### Diretório de arquivos de imagem ####

Um IFD contém informações sobre a imagem, bem como ponteiros para os dados reais da imagem. , seguido por um deslocamento de 4 bytes do próximo IFD (ou 0 se nenhum). Deve haver pelo menos 1 IFD em um arquivo TIFF e cada IFD deve ter pelo menos uma entrada.

##### Entrada IFD #####

Cada entrada IFD de 12 bytes está no formato a seguir.


|Bytes|Descrição
---|---|
|0-1|A Tag que identifica o campo
|2-3|O tipo de campo
|4-7|Contagem do tipo indicado
|8-11|O Deslocamento do Valor, o deslocamento do arquivo (em bytes) do Valor para o campo. Espera-se que o Valor comece em um limite de palavra; o Deslocamento de Valor correspondente será, portanto, um número par. Este deslocamento de arquivo pode apontar em qualquer lugar no arquivo, mesmo após os dados da imagem

Um campo TIFF é uma entidade lógica que consiste na tag TIFF e seu valor. Este conceito lógico é implementado como uma Entrada IFD, mais o valor real caso não se enquadre na parte valor/deslocamento, os últimos 4 bytes da Entrada IFD. Os termos campo TIFF e entrada IFD são intercambiáveis na maioria dos contextos.

#### Imagem em miniatura ####

O formato Exif contém miniatura da imagem (exceto Ricoh RDC-300Z). Geralmente está localizado próximo ao IFD1. Existem 3 formatos para miniaturas; Formato JPEG (JPEG usa YCbCr), formato RGB TIFF, formato YCbCr TIFF.

##### Miniatura em formato JPEG #####

Se o valor de Compression(0x0103) Tag em IFD1 for '6', o formato da imagem em miniatura será JPEG. A maioria das imagens Exif usa o formato JPEG para miniatura. Nesse caso, você pode obter o deslocamento da miniatura pela tag JpegIFOffset(0x0201) em IFD1, tamanho da miniatura pela tag JpegIFByteCount(0x0202). O formato de dados é o formato JPEG comum, começa em 0xFFD8 e termina em 0xFFD9. Parece que o formato JPEG e 160x120pixels de tamanho são formatos de miniaturas recomendados para Exif2.1 ou posterior.

##### Miniatura do formato TIFF #####

Se o valor de Compression(0x0103) Tag em IFD1 for '1', o formato da imagem em miniatura não será compactado (chamado de imagem TIFF). O ponto inicial dos dados da miniatura é a Tag StripOffset(0x0111), o tamanho da miniatura é a soma da TagStripByteCounts(0x0117).

## Referências ##

* [EXIF - Pela Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [Formato de arquivo EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

