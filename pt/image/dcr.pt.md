{
  "date" : "2021-26-08",
  "keywords" :[ "arquivo dcr", "formato de arquivo dcr", "o que é um arquivo dcr", "arquivo", "exemplo dcr", "extensão de arquivo dcr", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - Arquivo de imagem RAW de câmera digital",
  "description":"Saiba mais sobre o formato de arquivo DCR e as APIs que podem criar e abrir arquivos DCR.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## O que é um arquivo DCR? ##
Um arquivo com extensão dcr contém o conteúdo de uma fotografia digital salva no formato Kodak Digital Camera RAW (DCR). O DCR é a abreviação de **Digital Camera Raw**; contém a versão sem compressão e sem perdas dos dados das imagens capturadas por uma câmera digital Kodak. Os fotógrafos profissionais gostam de usar esses arquivos, porque eles armazenam imagens com qualidade superior aos formatos de imagem compactados de baixa qualidade.

## Formato de arquivo DCR
O DCR é um formato proprietário desenvolvido pela Eastman Kodak Company; referido simplesmente como Kodak. Um arquivo de imagem Digital Camera Raw (DCR) contém dados minimamente processados do sensor de imagem de uma câmera digital. Esses arquivos ainda não foram processados e, portanto, não estão prontos para serem impressos ou editados com um editor gráfico de bitmap.
Normalmente, um conversor raw processa a imagem em um espaço de cores interno de ampla gama, onde a precisão e o refinamento podem ser feitos antes da conversão para um formato de arquivo raster, como TIFF ou JPEG, para armazenamento, impressão ou manipulação adicional.
### Conteúdo do arquivo
A estrutura dos arquivos brutos geralmente segue um padrão genérico:
- Um cabeçalho de arquivo curto que contém um indicador da ordenação de bytes do arquivo.
- Metadados do sensor da câmera que são necessários para interpretar os dados da imagem do sensor, incluindo os atributos do CFA, o tamanho do sensor e seu perfil de cores.
- Metadados de imagem que podem ser úteis para inclusão em qualquer ambiente CMS ou banco de dados. Alguns arquivos brutos contêm uma seção de metadados padronizada com dados no formato Exif.
- Uma miniatura de imagem.
- Uma conversão JPEG de tamanho completo da imagem, que é usada para visualizar o arquivo no painel LCD da câmera.
- No caso de varreduras de filmes cinematográficos, o código de tempo, o código de chave ou o número do quadro na sequência do arquivo que representa a sequência do quadro em uma bobina digitalizada.
- Os dados da imagem do sensor
### Dados da imagem do sensor
O arquivo bruto desempenha um papel na fotografia digital semelhante ao que o filme fotográfico desempenha na fotografia cinematográfica. Arquivos brutos, portanto, contêm os dados de resolução total lidos de cada um dos pixels do sensor de imagem da câmera. O sensor da câmera é quase constantemente sobreposto com um CFA (Color Filter Array. Ele pode ser usado na conversão de imagens de alta faixa dinâmica quando dados em formato bruto estão disponíveis; como uma alternativa mais simples à abordagem HDI de exposição múltipla de capturar três imagens separadas.


## Referências ##

* [Formato de imagem bruta - pela Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [O que é um arquivo DCR](https://expertphotography.com/dcr-file/)

