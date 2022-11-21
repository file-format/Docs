{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "arquivo", "extensão", "formato", "o que é formato de arquivo m4p", "música", "formato de arquivo m4p", "M4b vs MP3", "especificação do formato de arquivo m4p"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo M4P e APIs que podem criar, converter e abrir arquivos M4P.",
  "title" :"M4P - Formato de arquivo de audiolivro MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## O que é um arquivo M4P?
O arquivo com extensão .m4p é um arquivo de áudio que geralmente está disponível na loja iTunes da Apple para download. Em outras palavras, podemos dizer que o M4P é um arquivo AAC, mas protegido contra cópia usando um Gerenciamento de Direitos Digitais (DRM). Isso significa que os arquivos M4P podem ser reproduzidos apenas em sistemas ou dispositivos autorizados. Normalmente, os arquivos M4P são específicos para dispositivos multimídia da Apple. Portanto, esses arquivos podem ser reproduzidos apenas em macbooks da Apple, podcasts, smartphones como iPhone 6 ou iPhone 7.

## Formato de arquivo M4P
O M4P significa MPEG 4 Protected (áudio) e codifica o áudio com codec de áudio avançado (AAC) e protege o arquivo do uso não autorizado do arquivo. Este formato de arquivo é geralmente considerado como um formato de arquivo de áudio da iTunes Music Store. A Apple usa seu sistema FairPlay Digital Rights Management (DRM) para proteger arquivos M4P. O FairPlay DRM é baseado na tecnologia desenvolvida pela Veridisc. Seu mecanismo de proteção funciona criptografando o fluxo de áudio AAC usando a criptografia AES. O usuário recebe uma chave mestra que é atribuída à sua conta para descriptografia. Este formato de arquivo foi introduzido como uma substituição do formato de arquivo MP3, porque o MP3 não foi originalmente concebido como um arquivo de áudio, mas como camada III em um arquivo de vídeo MPEG 1 ou 2.


## Especificações de formato de arquivo M4P

Semelhante ao [M4A](/pt/audio/m4a/), os arquivos M4P também consistem em partes consecutivas. Cada pedaço tem um cabeçalho de 8 bytes e é subdividido como:
- Tamanho do bloco de 4 bytes (big-endian, byte alto primeiro)
- tipo de bloco de 4 bytes - uma das assinaturas pré-definidas: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2 ", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt" ", "ctab", "ssrc".

Semelhante ao M4A, o primeiro pedaço em M4P será do tipo "ftype" e possui um subtipo no deslocamento 8. O M4P definido pelo subtipo que deve ser "M4P_".

Iterando pedaços, até que pedaço de tipo desconhecido seja detectado, ele irá compor o arquivo M4P (MPEG-4 Audio).

## Referências ##

* [MPEG-4 Parte 14 - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Exemplo de formato e recuperação de áudio MPEG-4 Parte 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

