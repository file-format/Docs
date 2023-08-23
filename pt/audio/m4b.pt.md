{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "arquivo", "extensão", "formato", "o que é formato de arquivo m4b", "música", "formato de arquivo m4b", "M4b vs MP3", "especificação do formato de arquivo m4b "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo M4B e APIs que podem criar, converter e abrir arquivos M4B.",
  "title" :"M4B - Formato de arquivo de audiolivro MPEG-4",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## O que é um arquivo M4B?

O arquivo com extensão .m4b é um audiolivro geralmente usado pelos livros da Apple e iTunes. O áudio usado neste formato é armazenado em MPEG-4 e compactado usando a codificação AAC. Um arquivo M4B é muito semelhante ao M4A, mas com suporte aos recursos relacionados ao audiolivro, como marcadores e quebras de capítulos. Os arquivos M4B estão disponíveis em versões habilitadas para DRM e sem DRM. Os audiolivros criptografados por DRM geralmente são audiolivros pagos da iTunes Store. Considerando que, o DRM gratuito pode ser encontrado facilmente na Internet.

## Formato de arquivo M4B

Os arquivos de audiolivro contendo metadados, imagens, marcadores e hiperlinks podem ser salvos com extensão .m4a, mas geralmente a extensão .m4b é usada ao salvar, apenas para especificar que o arquivo tem um formato de arquivo de audiolivro. Fairplay DRM (Gerenciamento de Direitos Digitais) é usado pelo aplicativo para proteger seus arquivos M4B. Portanto, os arquivos baixados do iTunes podem ser reproduzidos apenas em dispositivos ou computadores autorizados.


## M4B vs M4A

Tanto M4B quanto [MP3](/audio/mp3/) são formatos de arquivo somente de áudio.

**M4B**: Ganha quando comparado ao MP3 em termos de qualidade se codificar ambos na mesma taxa de bits. O M4B é um arquivo de audiolivro compactado usando a codificação AAC. É basicamente associado a “MPEG-4 Audio Layer”, arquivos com extensão .m4b são a camada de áudio de filmes MPEG-4, mas com recursos extras relacionados a audiolivros. Seu objetivo é ultrapassar o MP3 e se tornar o novo padrão em compressão de áudio. É muito próximo do MP3 em muitos aspectos, mas desenvolvido para ter uma qualidade melhor em um tamanho de arquivo igual ou até menor. O formato M4B foi introduzido pela primeira vez pela Apple. O tipo de formato também é realizado como o codificador sem perdas da Apple (ALE).

Portanto, atualmente o M4B não conseguiu o sucesso mainstream do MP3 porque o formato de áudio ainda não é comumente reproduzido.

**Mp3**: Um formato de áudio digital que é bem conhecido de todos. Um formato de compressão muito primeiro em cena e tornou-se muito famoso entre os ouvintes de música. Seu sucesso mainstream é tão rápido que o tipo de arquivo pode ser reproduzido universalmente e compatível com quase tudo, hardware ou software. De um modo geral, o M4A produzirá melhor qualidade de som, mas muitos argumentam que, seja verdade ou não, a diferença de som não é comparável, e seria uma perda de tempo tentar converter arquivos MP3 em arquivos M4A. Por fim, a conversão apenas fará com que você perca a qualidade do som original.

## Especificação do formato de arquivo M4B

Semelhante ao [M4A](/pt/audio/m4a/), os arquivos M4B também consistem em partes consecutivas. Cada pedaço tem um cabeçalho de 8 bytes e é subdividido como:
- Tamanho do bloco de 4 bytes (big-endian, byte alto primeiro)
- tipo de bloco de 4 bytes - uma das assinaturas pré-definidas: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT ", "scpt", "ssrc".

Semelhante ao M4A, o primeiro pedaço em M4B será do tipo "ftype" e possui um subtipo no deslocamento 8. O M4B definido pelo subtipo que deve ser "M4B_".

Iterando pedaços, até que pedaço de tipo desconhecido seja detectado, ele irá compor o arquivo M4B (MPEG-4 Audio).

## Referências

* [MPEG-4 Parte 14 - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemplo de formato e recuperação de áudio MPEG-4 Parte 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

