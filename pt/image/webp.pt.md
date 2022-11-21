{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo webp", "formato de arquivo webp", "o que é um arquivo webp", "arquivo", "exemplo webp", "extensão de arquivo webp","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Formato de arquivo de imagem raster do Google",
  "description":"Saiba mais sobre o formato de arquivo WEBP e APIs que podem criar e abrir arquivos WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo WEBP?

O WebP, introduzido pelo Google, é um formato de arquivo de imagem da Web raster moderno baseado em compactação sem perdas e com perdas. Ele fornece a mesma qualidade de imagem enquanto reduz consideravelmente o tamanho da imagem. Como a maioria das páginas da web usa imagens como representação efetiva de dados, o uso de imagens WebP em páginas da web resulta em carregamento mais rápido das páginas da web. De acordo com o Google, as imagens sem perdas WebP são 26% menores em tamanho em comparação com [PNGs](/pt/image/png/), enquanto as imagens com perdas WebP são 25-34% menores que as imagens [JPEG](/pt/image/jpeg/) comparáveis. As imagens são comparadas com base no índice Structural Similarity (SSIM) entre WebP e outros formatos de arquivo de imagem. WebP é um projeto irmão do formato de contêiner multimídia [WebM](https://en.wikipedia.org/wiki/WebM).

## Visão geral dos recursos do WebP ##

As imagens WebP usam o processo de compactação com base na previsão de pixels de seus blocos circundantes, resultando em pixels a serem usados várias vezes em um único arquivo. Ele suporta imagens animadas e espera-se que suporte mais recursos no futuro. O Google disponibilizou o código-fonte [online](https://developers.google.com/speed/webp/download) para seu codificador e decodificador para ser usado quando necessário. A imagem WebP fornece suporte para:

* **Compressão com perdas:** a compressão com perdas é baseada na codificação do quadro-chave [VP8](http://en.wikipedia.org/wiki/VP8). VP8 é um formato de compressão de vídeo criado pela On2 Technologies como sucessor dos formatos VP6 e VP7.
* **Compressão sem perdas:** o formato de compressão sem perdas foi desenvolvido pela equipe WebP.
* **Transparência:** o canal alfa de 8 bits é útil para imagens gráficas. O canal Alpha pode ser usado junto com RGB com perdas, um recurso que atualmente não está disponível em nenhum outro formato.
* **Animação:** Suporta imagens animadas em cores reais.
* **Metadados:** pode conter metadados EXIF e XMP (usados por câmeras, por exemplo).
* **Perfil de cores:** pode ter um perfil ICC incorporado.

A compactação com perda WebP usa codificação preditiva para codificar uma imagem, o mesmo método usado pelo codec de vídeo VP8 para compactar quadros-chave em vídeos. A codificação preditiva usa os valores em blocos de pixels vizinhos para prever os valores em um bloco e, em seguida, codifica apenas a diferença.

A compressão WebP sem perdas usa fragmentos de imagem já vistos para reconstruir exatamente novos pixels. Ele também pode usar uma paleta local se nenhuma correspondência interessante for encontrada.

## Formato de arquivo ##

O formato de arquivo WebP é baseado no formato de documento RIFF (resource interchange file format). O contêiner WebP fornece suporte para recursos além e acima de conter apenas uma única imagem codificada como um quadro-chave VP8. O elemento básico de um arquivo RIFF é um pedaço que consiste em:


|Campo|Descrição
---|---|
|Chunk FourCC: 32 bits|Código ASCII de quatro caracteres usado para identificação de pedaços
|Tamanho do fragmento: 32 bits (uint32)|O tamanho do fragmento sem incluir este campo, o identificador do fragmento ou o preenchimento
|Carga útil do bloco: bytes do tamanho do bloco|A carga útil dos dados. Se o tamanho do bloco for ímpar, um único byte de preenchimento ~-~- que deve ser 0 ~-~- é adicionado
|ChunkHeader ('ABCD')|Usado para descrever o cabeçalho FourCC e Chunk Size de blocos individuais, onde 'ABCD' é o FourCC para o bloco. O tamanho deste elemento é de 8 bytes.

### Cabeçalho WebP ###

Um cabeçalho de arquivo WebP é o seguinte:

* Cabeçalho RIFF - 32 bits representando os caracteres ASCII 'R' 'I' 'F' 'F'
* Tamanho do arquivo - 32 bits (uint32) representando o tamanho do arquivo em bytes começando no deslocamento 8. O valor máximo deste campo é 2^32 menos 10 bytes e assim o tamanho do arquivo inteiro é no máximo 4GiB menos 2 bytes .
* 'WEBP' - 32 bits representando os caracteres ASCII 'W' 'E' 'B' 'P'

### Formato de arquivo com perdas ###

As imagens WebP usam o formato de arquivo com perdas se a imagem for baseada em codificação com perdas e não exigir nenhum recurso avançado/estendido, como transparência, animação, alfa, etc. As imagens com perdas são menores e também são suportadas pelos aplicativos mais antigos.

O arquivo WebP, neste caso, consiste em:

* Cabeçalho de arquivo WebP de 12 bytes
* VP8 pedaço

O [VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) ilustra as especificações do formato de fluxo de bits do VP8.

### Formato de arquivo sem perdas ###

Este layout é usado quando a imagem é baseada em codificação sem perdas e não há necessidade de recursos avançados fornecidos pelo formato externo. Os aplicativos mais antigos podem não conseguir ler esses arquivos.

O arquivo WebP, neste caso, consiste em:

* Cabeçalho de arquivo WebP de 12 bytes
* Bloco VP8L

## Referências ##

* [Referência do desenvolvedor WebP - do Google](https://developers.google.com/speed/webp/)
* [Formato de arquivo WebP - Por Wikipedia](https://en.wikipedia.org/wiki/WebP)

