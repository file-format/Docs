{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "arquivo", "extensão", "formato", "formato de arquivo de intercâmbio de áudio", "música" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo WAV e APIs que podem criar e abrir arquivos WAV.",
  "title" :"WAV - Formato de arquivo de áudio em forma de onda",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## O que é um arquivo WAV?

WAV, conhecido por WAVE (Waveform Audio File Format), é um subconjunto da especificação Resource Interchange File Format (RIFF) da Microsoft para armazenar arquivos de áudio digital. O formato não aplica nenhuma compactação ao fluxo de bits e armazena as gravações de áudio com diferentes taxas de amostragem e taxas de bits. Foi e é um dos formatos padrão para CDs de áudio. Os arquivos Wave são maiores em tamanho em comparação com os novos formatos de arquivo de áudio, como [MP3](/pt/audio/mp3/), que usa compactação com perdas para reduzir o tamanho do arquivo, mantendo a mesma qualidade de áudio. No entanto, os arquivos WAV podem ser compactados usando codecs Audio Compression Manager (ACM). Existem várias APIs e aplicativos disponíveis que podem converter arquivos WAV para outros formatos populares de arquivos de áudio.

**Você sabia?**
Você pode se tornar um colaborador em FileFormat.com para manter a comunidade de formatos de arquivo atualizada com suas descobertas. Se você precisar compartilhar algo sobre formatos de arquivo WAV ou de áudio, poderá postar suas descobertas na seção [Audio File Format News](https://news.fileformat.com/t/audio) para que as pessoas permaneçam atualizadas.

## Formato de arquivo WAV ##

O formato de arquivo WAVE, sendo um subconjunto da especificação RIFF da Microsoft, começa com um cabeçalho de arquivo seguido por uma sequência de blocos de dados. Um arquivo WAVE tem um único pedaço "WAVE" que consiste em dois sub-chunks:

* um pedaço "fmt" - especifica o formato de dados
* um pedaço de "dados" - contém os dados de amostra reais

### Cabeçalho do arquivo WAV ###

O cabeçalho de um arquivo WAV (RIFF) tem 44 bytes e tem o seguinte formato:


|Posições|Valor da amostra|Descrição
---|---|---|
|1 - 4|"RIFF"|Marca o arquivo como um arquivo riff. Os caracteres têm cada um 1 byte de comprimento.
|5 - 8|Tamanho do arquivo (inteiro)|Tamanho do arquivo geral - 8 bytes, em bytes (inteiro de 32 bits). Normalmente, você preencheria isso após a criação.
|9 -12|"WAVE"|Cabeçalho do tipo de arquivo. Para nossos propósitos, sempre é igual a "WAVE".
|13-16|"fmt "|Formatar marcador de bloco. Inclui nulo à direita
|17-20|16|Comprimento dos dados de formato conforme listado acima
|21-22|1|Tipo de formato (1 é PCM) - inteiro de 2 bytes
|23-24|2|Número de canais - inteiro de 2 bytes
|25-28|44100|Taxa de amostragem - inteiro de 32 bytes. Os valores comuns são 44100 (CD), 48000 (DAT). Taxa de Amostra = Número de Amostras por segundo, ou Hertz.
|29-32|176400|(Taxa de Amostra * BitsPor Amostra * Canais) / 8.
|33-34|4|(BitsPerSample * Canais) / 8.1 - 8 bits mono2 - 8 bits estéreo/16 bits mono4 - 16 bits estéreo
|35-36|16|Bits por amostra
|37-40|"dados"|"dados" cabeçalho do bloco. Marca o início da seção de dados.
|41-44|Tamanho do arquivo (dados)|Tamanho da seção de dados.
|Os valores de amostra são fornecidos acima para uma fonte estéreo de 16 bits.

## Referências ##

* [WAV - Por Wikipedia](https://en.wikipedia.org/wiki/WAV)

