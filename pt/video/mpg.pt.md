{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo MPG",
  "keywords" :[ "MPG", "arquivo", "extensão", "formato", "formato de vídeo", "o que é um formato de arquivo mpg", "formato de arquivo mpg", "reprodutor de arquivo mpg", "compactação mpeg", "vídeo ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Aprenda sobre o formato de arquivo MPG e APIs que podem criar e mostrar como abrir os arquivos MPG.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## O que é um formato de arquivo MPG? ##

O arquivo com extensão .mpg pertence ao grupo de extensões de arquivo para compressão de áudio e vídeo MPEG-1 ou MPEG-2. O vídeo MPEG-1 Part 2 não está facilmente disponível, e essa extensão (formato de arquivo MPG) normalmente aponta para um fluxo de programa MPEG definido em MPEG-1 e MPEG-2, ou um fluxo de transporte MPEG definido em MPEG-2 . Outras extensões como .m2ts também existem especificando o contêiner preciso, neste caso, MPEG-2 TS, mas isso tem pouca pertinência para a mídia MPEG-1. O [.mp3](/audio/mp3/) é a extensão mais comum para arquivos que contêm áudio MP3. Um arquivo MP3 é um fluxo típico de áudio bruto; a maneira tradicional de marcar arquivos MP3 é gravando dados de fluxo em segmentos "lixo" de cada quadro, que salvam as informações de mídia, mas são descartadas pelo **player de arquivos mpg**. Esta é uma técnica semelhante usada para marcar os arquivos AAC, mas menos suportada hoje em dia.

## Compressão MPEG ##

O nome MPEG significa Moving Pictures Experts Group. MPEG é uma ferramenta de compressão de vídeo, que envolve a compressão de imagens e sons, bem como a sincronização dos dois.
Atualmente existem vários padrões MPEG.

- MPEG-1 é proposto para taxas de dados intermediárias, da ordem de 1,5 Mbit/s.
- MPEG-2 é proposto para altas taxas de dados de pelo menos 10 Mbit/s.
- MPEG-3 foi proposto para compressão HDTV, mas foi considerado redundante e foi mesclado com MPEG-2.
- MPEG-4 é proposto para taxas de dados muito baixas, inferiores a 64 Kbit/s.


## Fluxo de programa de formato de arquivo MPG ##

O fluxo do programa é um contêiner para multiplexação de áudio digital, vídeo e muito mais. O formato Program Stream é especificado na 1ª parte do MPEG-1 (ISO/IEC 11172-1) e 1ª parte do MPEG-2, Sistemas (norma ISO/IEC 13818-1/ITU-T H.222.0). O fluxo de programa MPEG-2 é baseado em analógico e semelhante à camada de sistemas ISO/IEC 11172 e compatível com versões anteriores.

### Detalhes de codificação ###

Aqui estão os detalhes de codificação do formato de cabeçalho do pacote MPEG-2 Program Stream parcial:

| Nome | Número de bits | Descrição |
---|---|---|
| bytes de sincronização | 32 | 0x000001BA |
| bits de marcação | 2 | 01b para a versão MPEG-2. Os bits marcadores para a versão MPEG-1 são 4 bits com valor 0010b. |
| Relógio do sistema [32..30] | 3 | Bits 32 a 30 da Referência de Relógio do Sistema (SCR) |
| bit marcador | 1 | 1 Bit sempre definido. |
| Relógio do sistema [29..15] | 15 | Bits de clock do sistema 29 a 15 |
| bit marcador | 1 | 1 Bit sempre definido. |
| Relógio do sistema [14..0] | 15 | Bits de clock do sistema 14 a 0 |
| bit marcador | 1 | 1 Bit sempre definido. |
| Extensão SCR | 9 | |
| bit marcador | 1 | 1 Bit sempre definido. |
| taxa de bits | 22 | Em unidades de 50 bytes por segundo. |
| bits de marcação | 2 | 11 bits sempre definidos. |
| reservado | 5 | reservado para uso futuro |
| comprimento de enchimento | 3 | |
| bytes de enchimento | 8*comprimento de enchimento | |
| cabeçalho do sistema (opcional) | 0 ou mais | se o código de início do cabeçalho do sistema for o seguinte: 0x000001BB |

A tabela a seguir mostra o formato parcial do cabeçalho do sistema:

| Nome | Número de bytes | Descrição |
---|---|---|
| bytes de sincronização | 4 | 0x000001BB |
| comprimento do cabeçalho | 2 | |
| bits de limite e marcador de taxa | 3 | |
| áudio encadernado e bandeiras | 1 | |
| sinalizadores, marcador de bits e vídeo vinculado | 1 | |
| Restrição de taxa de pacotes e byte reservado | 1 | |


## Referências ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



