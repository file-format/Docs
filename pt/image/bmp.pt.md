{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo bmp", "formato de arquivo bmp", "o que é um arquivo bmp", "arquivo", "exemplo bmp", "extensão de arquivo bmp", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo BMP e APIs que podem criar e abrir arquivos BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# O que é um arquivo BMP? #

Arquivos com extensão .BMP representam arquivos de imagem de bitmap que são usados para armazenar imagens digitais de bitmap. Essas imagens são independentes do adaptador gráfico e também são chamadas de formato de arquivo de bitmap independente de dispositivo (DIB). Essa independência serve para abrir o arquivo em várias plataformas, como Microsoft Windows e Mac. O formato de arquivo BMP pode armazenar dados como imagens digitais bidimensionais em formato monocromático e colorido com várias profundidades de cor.

## Especificações de formato de arquivo BMP ##

Os bitmaps independentes de dispositivo agem como uma ajuda para trocar bitmaps entre dispositivos e aplicativos. Devido à evolução contínua deste formato de arquivo, as informações contidas nos cabeçalhos podem ser diferentes conforme a versão do Bitmap. Um único arquivo de bitmap consiste em estruturas de tamanho fixo e variável em uma sequência específica.

As estruturas em um arquivo Bitmap são organizadas na seguinte ordem:


|Estrutura|Opcional|Tamanho|Propósito
---|---|---|---|
|File Header|No|14|Para armazenar informações gerais sobre o arquivo de imagem bitmap
|DIB Header|No|Fixed-Size|Para armazenar informações detalhadas sobre a imagem bitmap e definir o formato de pixel
|Extra Bit Masks|Sim|12 ou 16 bytes|Para definir o formato de pixel
|Paleta de cores|Semi-opcional|Tamanho variável|Para definir as cores usadas pelos dados da imagem bitmap
|Espaço1|Sim|Tamanho da variável|Alinhamento da estrutura
|Matriz de pixels|Não|Tamanho variável|O formato de pixel é definido pelo cabeçalho DIB ou pelas máscaras de bits extras.
|Espaço2|Sim|Tamanho variável|Alinhamento da estrutura
|Perfil de cores ICC|Sim|Tamanho variável|Para definir o perfil de cores para gerenciamento de cores

Quando uma imagem de bitmap é carregada na memória, ela se torna uma estrutura DIB, usada pelo Windows por meio de sua API GDI. O cabeçalho do arquivo não faz parte dessa estrutura de dados. A cor também pode consistir em entradas de 16 bits que constituem índices para a paleta referenciada no momento em vez de definições de cores RGB explícitas. Vamos dar uma olhada em alguns deles em detalhes, especialmente os cabeçalhos.

### Cabeçalho do arquivo bitmap ###

Um cabeçalho de arquivo de bitmap é semelhante a outros cabeçalhos de arquivo usados para identificar o arquivo. Como existem diferentes variantes do formato de arquivo BMP, os primeiros 2 bytes do formato de arquivo BMP são o caractere "B" e depois o caractere "M" na codificação ASCII. Todos os valores inteiros são armazenados no formato little-endian.

|Deslocamento hex|Deslocamento dec|Tamanho|Propósito
---|---|---|---|
|00|0|2 bytes|O campo de cabeçalho utilizado para identificar o arquivo BMP e DIB é 0x42 0x4D em hexadecimal, igual ao BM em ASCII. Pode seguir valores possíveis.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – matriz de bitmap de estrutura OS/2 * **CI** – estrutura OS/2 ícone de cor * **CP** – ponteiro de cor do OS/2 const * **IC** – ícone de estrutura do OS/2 * **PT** – ponteiro do OS/2
|02|2|4 bytes|O tamanho do arquivo BMP em bytes
|06|6|2 bytes|Reservado; o valor real depende do aplicativo que cria a imagem
|08|8|2 bytes|Reservado; o valor real depende do aplicativo que cria a imagem
|0A|10|4 bytes|O deslocamento, ou seja, o endereço inicial, do byte onde os dados da imagem bitmap (matriz de pixels) podem ser encontrados.

#### Cabeçalho DIB (cabeçalho de informações de bitmap) ####

As informações detalhadas sobre a imagem são representadas por este cabeçalho. Com base nessas informações, será determinado o aplicativo que será usado para exibir a imagem na tela. Todos esses cabeçalhos contêm um campo DWORD (32 bits), especificando seu tamanho, para que um aplicativo possa determinar facilmente o cabeçalho usado na imagem. Isso se deve basicamente ao fato de o formato DIB ter sofrido várias extensões. A seguir está o cabeçalho DIB com os campos listados.

#### Paleta de cores ####

Uma paleta de cores BMP é uma matriz de estruturas que especificam os valores de intensidade RGB de cada cor na paleta de cores de um dispositivo de exibição. Cada pixel nos dados de bitmap armazena um único valor usado como índice na paleta de cores. As informações de cor armazenadas no elemento nesse índice especificam a cor desse pixel. A disponibilidade de cores em um arquivo bitmap varia da seguinte forma:

* Um, 4 e 8 bits - espera-se que sempre contenha uma paleta de cores
* Dezesseis, 24 e 32 bits - nunca contêm paletas de cores
* Arquivos BMP de dezesseis e 32 bits - contêm valores de máscara de campos de bits no lugar da paleta de cores

#### Armazenamento de pixels ####

Os pixels de bitmap são armazenados como bits compactados em linhas onde o tamanho de cada linha é arredondado para um múltiplo de 4 bytes (um DWORD de 32 bits) por preenchimento. A quantidade total de bytes necessária para armazenar os pixels de uma imagem não pode ser calculada diretamente apenas contando os bits. Como há preenchimento envolvido, o efeito de arredondar o tamanho de cada linha para um múltiplo de 4 bytes é necessário. Os bytes de preenchimento (não necessariamente 0) devem ser anexados ao final das linhas para aumentar o comprimento das linhas para um múltiplo de quatro bytes. Quando a matriz de pixels é carregada na memória, cada linha deve começar em um endereço de memória múltiplo de 4.

A imagem é realmente descrita pela representação DWORDs de 32 bits da matriz de pixels. Normalmente os pixels são armazenados "de baixo para cima", começando no canto inferior esquerdo, indo da esquerda para a direita, e depois linha por linha de baixo para cima da imagem. Os formatos de pixel e suas implicações estão listados abaixo:

* O formato de 1 bit por pixel (1bpp) suporta 2 cores distintas (por exemplo: preto e branco).
* O formato de 2 bits por pixel (2bpp) suporta 4 cores distintas e armazena 4 pixels por 1 byte, sendo o pixel mais à esquerda nos dois bits mais significativos. Cada valor de pixel é um índice de 2 bits em uma tabela de até 4 cores.
* O formato de 4 bits por pixel (4bpp) suporta 16 cores distintas e armazena 2 pixels por 1 byte, sendo o pixel mais à esquerda no nibble mais significativo. Cada valor de pixel é um índice de 4 bits em uma tabela de até 16 cores.
* O formato de 8 bits por pixel (8bpp) suporta 256 cores distintas e armazena 1 pixel por 1 byte. Cada byte é um índice em uma tabela de até 256 cores.
* O formato de 16 bits por pixel (16bpp) suporta 65536 cores distintas e armazena 1 pixel por WORD de 2 bytes. Cada WORD pode definir as amostras alfa, vermelha, verde e azul do pixel.
* O formato de pixel de 24 bits (24bpp) suporta 16.777.216 cores distintas e armazena 1 valor de pixel por 3 bytes. Cada valor de pixel define as amostras de vermelho, verde e azul do pixel (8.8.8.0.0 em notação RGBAX). Especificamente, na ordem: azul, verde e vermelho (8 bits por cada amostra).
* O formato de 32 bits por pixel (32bpp) suporta 4.294.967.296 cores distintas e armazena 1 pixel por DWORD de 4 bytes. Cada DWORD pode definir as amostras alfa, vermelha, verde e azul do pixel.

## Referências ##

* [Formato Windows MetaFile](http://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Formato de arquivo BMP](https://en.wikipedia.org/wiki/BMP_file_format)

