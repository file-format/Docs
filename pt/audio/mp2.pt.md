{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "arquivo mp2", "extensão", "formato", "o que é um arquivo mp2", "música", "formato de arquivo mp2"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo MP2 e APIs que podem criar, converter e abrir arquivos MP2.",
  "title" :"MP2 - Formato de arquivo de áudio MPEG Layer 2",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## O que é um arquivo MP2?

Um arquivo MP2 que também é chamado de arquivo MPA é um arquivo de áudio compactado com Layer II de MPEG-1 ou MPEG-2; um formato de compressão de áudio com perdas definido pela ISO/IEC 11172-3 juntamente com MPEG-1 Audio Layer I e MPEG-1 Audio Layer III ([MP3](/pt/audio/mp3/)), para reduzir o tamanho do arquivo de áudio. Considerando que, o MP3 é mais popular do que o MP2 devido ao seu tamanho menor e disponibilidade na Internet. Portanto, o MP2 ainda é um padrão vital para transmissão de áudio.

## Formato de arquivo MP2

MPEG Audio Layer II (MP2) é o algoritmo central dos padrões MP3. A codificação MPEG-1 Audio Layer 2 foi obtida a partir do codec de áudio MUSICAM. Começou como o projeto Digital Audio Broadcast (DAB) na Alemanha como parte do programa de pesquisa EUREKA. O Eureka 147 continha três elementos principais: Codificação e Multiplexação de Transmissão, Modulação COFDM e Codificação de Áudio MUSICAM (Padrão de Máscara Universal Codificação Integrada e Multiplexação de Sub-banda). A MUSICAM foi uma das poucas codificações que conseguiu alcançar alta qualidade de áudio em taxas de bits na faixa de 64 a 192 kbit/s por canal monofônico. O objetivo era fornecer baixo atraso, baixa complexidade, robustez a erros, unidades de acesso curto e atender aos requisitos técnicos de transmissão, telecomunicações e gravação em mídia de armazenamento digital.

MP2 é um codificador de áudio de sub-banda, que pode ser comprimido no domínio do tempo com um banco de filtros de baixo atraso gerando 32 componentes de domínio de frequência. Em comparação, o MP3 é um codificador de áudio de transformação com banco de filtros híbrido, o que significa que a compressão aplicada no domínio da frequência após uma transformação híbrida do domínio do tempo. O codificador MP2 pode explorar redundâncias entre canais usando codificação de intensidade "joint stereo" opcional.

### Especificações de formato de arquivo MP2

O formato de arquivo MP2 é baseado em quadros digitais sucessivos de 1152 intervalos de amostragem com quatro formatos possíveis:

- formato mono
- formato estéreo
- formato estéreo comum codificado de intensidade (irrelevância estéreo)
- formato de canal duplo (não correlacionado)
Algumas especificações técnicas importantes do MP2 são fornecidas na tabela abaixo:

|Especificação| Descrição|
---|---|
|**Taxas de amostragem**| 32, 44,1 e 48 kHz|
|**Taxas de bits**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 e 384 kbit/s|
|**Taxas de amostragem adicionais**|16, 22,05 e 24 kHz|
|**Taxas de bits adicionais**|8, 16, 24, 40 e 144 kbit/s|
|**Suporte multicanal**|Até 5 canais de áudio de faixa completa e um canal LFE (canal de aprimoramento de baixa frequência)|

## Referências ##

* [MPEG-1 Audio Layer II - Por Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

