{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo tga", "formato de arquivo tga", "o que é um arquivo tga", "arquivo", "exemplo tga", "extensão de arquivo tga", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo TGA - Um arquivo de imagem gráfica TARGA",
  "description":"Saiba mais sobre o formato de arquivo TGA e APIs que podem criar e abrir arquivos TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo TGA?

Um arquivo com extensão .tga é um formato gráfico raster e foi criado pela Truevision Inc. Ele foi projetado para as placas TARGA (Truevision Advanced Raster Adapter) e forneceu suporte de exibição Highcolor/truecolor para PCs compatíveis com IBM. Ele suporta 8, 16, 24 e 32 bits por pixel e canal alfa de 8 bits. Ele também suporta compressão RLE sem perdas que pode ser aplicada para reduzir o tamanho da imagem. Fotos e texturas digitais usam o formato de imagem TGA.

## Breve história

A formação do formato de arquivo TGA surgiu em 1984 pela AT&T EPICenter (mais tarde extraída e formada como uma entidade independente conhecida como Truevision) que estava trabalhando no marketing de novas tecnologias desenvolvidas pela AT&T para buffers de quadros coloridos. A EPICenter já estava trabalhando em suas duas primeiras placas, a VDA (Video Display Adapter) e a ICB (image capture board) para as quais já estava em andamento o trabalho em dois tipos de arquivos, .vda e .icb. Esses formatos de arquivo foram codificados e o formato de arquivo específico menos amplo TGA foi introduzido. O TGA era uma extensão do que já estava em uso, e fornecia informações como largura, altura, profundidade de pixel, mapa de cores associado e origem da imagem.

A versão 2.0 do TGA, publicada em 1989, incorporou vários recursos aprimorados, como:

* Miniaturas
*canal alfa
* Valor Gama
* Metadados textuais

Os principais contribuidores para a versão 2.0 da TGA incluem Shawn Steiner da Truevision, Kevin Fiedly e David Spoelstra.

## Especificações de formato de arquivo TGA TARGA

Um arquivo TGA consiste em 2 partes principais:

* Cabeçalho
* Informações de pixel de cor

Todos os valores em um arquivo TGA estão em littl-endian conforme as especificações de formato.

### Cabeçalho TGA

Um cabeçalho de arquivo TGA consiste nos 5 campos a seguir.

|Nº do campo|Comprimento |Nome do campo |Descrição|
---|---|---|---|
|1| 1 byte |Comprimento do ID| Comprimento do campo ID da imagem (0-255)|
|2| 1 byte |Tipo de mapa de cores| Se um mapa de cores está incluído (0 - indica que nenhum dado de mapa de cores está incluído nesta imagem. 1 - indica que um mapa de cores está incluído nesta imagem.)|
|3| 1 byte |Tipo de imagem| Tipos de compactação e cor (0- Nenhum dado de imagem incluído. 1- Não compactado, imagem mapeada em cores, 2- Não compactado, Imagem em cores reais, 9- Codificado em comprimento de execução, Imagem mapeada em cores, 11- Codificado em comprimento de execução, Imagem em preto e branco )|
|4| 5 bytes |Especificação do mapa de cores| Descreve o mapa de cores|
|5| 10 bytes |Especificação da imagem| Dimensões e formato da imagem|

### Dados do mapa de imagens e cores

| Campo nº. |Comprimento |Campo |Descrição|
---|---|---|---|
|6 |Do campo de comprimento do ID da imagem| ID da imagem| Campo opcional contendo informações de identificação|
|7 |Do campo de especificação do mapa de cores| Dados do mapa de cores| Tabela de consulta contendo dados do mapa de cores|
|8 |Do campo de especificação de imagem| Dados de imagem| Armazenado de acordo com o descritor da imagem|

### Área do desenvolvedor (opcional)

O TGA Versão 2.0 fornece suporte para aprimoramentos/extras adicionais que muitos desenvolvedores desejavam armazenar mais informações. A informação é opcional para que, se um decodificador TGA não for capaz de interpretá-la, ela será ignorada.

### Área de extensão (opcional)

|Campo nº.| Comprimento| Campo |Descrição|
---|---|---|---|
|10| 2 bytes |Tamanho da extensão |Tamanho em bytes da área de extensão, sempre 495|
|11| 41 bytes| Nome do autor |Nome do autor. Se não for usado, os bytes devem ser definidos como NULL (\0) ou espaços|
|12| 324 bytes| Comentário do autor| Um comentário, organizado em quatro linhas, cada uma composta por 80 caracteres mais um NULL|
|13| 12 bytes| Carimbo de data/hora |Data e hora em que a imagem foi criada|
|14| 41 bytes| ID do trabalho||
|15| 6 bytes| Tempo de trabalho| Horas, minutos e segundos gastos na criação do arquivo (para faturamento, etc.)|
|16| 41 bytes| ID do software |O aplicativo que criou o arquivo.|
|17| 3 bytes| Versão do software||
|18| 4 bytes| Cor chave||
|19| 4 bytes| Proporção de pixel||
|20| 4 bytes| Valor gama||
|21| 4 bytes| Deslocamento de correção de cor |Número de bytes desde o início do arquivo até a tabela de correção de cor, se presente|
|22| 4 bytes| Selo postal | Número de bytes desde o início do arquivo até a imagem do selo postal, se presente|
|23| 4 bytes| Deslocamento da linha de digitalização| Número de bytes desde o início do arquivo até a tabela de linhas de varredura, se presente|
|24| 1 byte| Tipo de atributos| Especifica o canal alfa|

### Rodapé do arquivo (opcional)

Os últimos 26 bytes do arquivo representam o rodapé, que se presente significa que provavelmente é um arquivo TGA versão 2.

|Nº do Campo| Comprimento| Campo| Descrição|
---|---|---|---|
|28| 4 bytes| Deslocamento de extensão| Deslocamento em bytes desde o início do arquivo|
|29| 4 bytes| Deslocamento da área do desenvolvedor| Deslocamento em bytes desde o início do arquivo|
|30| 16 bytes| Assinatura| Contém "TRUEVISION-XFILE"|
|31| 1 byte| | Contém "."|
|32| 1 byte| | Contém NULL|


## Referências

* [Especificações de formato de arquivo TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA pela Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

