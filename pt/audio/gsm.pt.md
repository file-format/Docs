{
  "date" : "2021-08-05",
  "keywords" :[ "gsm", "arquivo", "extensão", "formato", "Áudio", "Sistema global para áudio móvel", "extensão gsm", "arquivos gsm"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo GSM e APIs que podem criar e abrir arquivos GSM.",
  "title" :"GSM - Sistema Global para Formato de Arquivo de Áudio Móvel",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-05"
}

## O que é um arquivo GSM?

GSM é uma extensão de arquivo associada ao Global System for Mobile Audio Format Files. Arquivos contendo extensões GSM podem ser abertos em plataformas Linux, Windows e Mac OS. O formato de arquivo GSM pertence à categoria de arquivos de áudio.

Um arquivo GSM é codificado com um codec de compressão de som CBR (taxa de bits constante) com perdas. A taxa de amostragem em um arquivo de áudio GSM é de 8.000 amostras/segundo, enquanto a taxa de dados é de cerca de 13 kbps. A taxa de bits nos arquivos GSM garante qualidade durante a gravação de voz. Além disso, o formato de arquivo GSM também é conhecido como o formato padrão global a ser usado em telefones celulares e os arquivos WAV também podem ser facilmente codificados usando um formato de arquivo GSM. Quaisquer problemas com um arquivo GSM podem ser facilmente resolvidos pelo próprio usuário sem recorrer a um especialista.

Os usuários também podem converter arquivos GSM nos formatos [MP3](/pt/audio/mp3/) e [MP4](/pt/video/mp4/).

## Breve História do Formato de Arquivo GSM

GSM é um formato de arquivo de áudio que foi criado para telefonia via Internet na Europa. Foi desenvolvido pelo European Telecommunications Standard Institute (ETSI) para ser usado como um celular digital 2G usado em telefones celulares e tablets. Hoje é usado para armazenar gravações de conversas telefônicas e mensagens de voz.

## Especificações de formato de arquivo GSM ##

GSM funciona em uma rede estruturada que consiste nas seguintes seções:

- **Modulação** : É um processo de transformação dos dados de entrada em um formato que pode ser facilmente transmitido. Os dados transmitidos são demodulados na extremidade receptora
- **Taxa de transmissão** : GSM é um sistema digital que tem uma taxa de bits acima de 270 kbps
- **Faixa de frequência de uplink**: 933-960 MHz
- **Faixa de frequência de downlink**: 890 – 915 MHz
- **Espaçamento de Canais** : Significa o espaçamento entre barreiras adjacentes que deve ser de cerca de 200 kHz
- **Distância Duplex** : É o espaço entre as frequências de uplink e downlink que deve ser de 80 MHz
- **Codificação de Fala**: GSM usa Codificação Preditiva Linear (LPC). LPC comprime a taxa de bits. Quando o sinal de áudio passa por um filtro e imita o trato vocal. Fala de codificação GSM a 13kbps

| Formato de compressão de áudio | Algoritmo | Taxa de amostragem | Transformação da taxa de bits | Latência | CBR | VBR | Estéreo | Multicanal |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8kHz | 5,6 kbit/s | 25 ms | Sim | Não | Não | Não |
| GSM-FR | RPE-LTP | 8kHz | 13 kbit/s | 20–30 ms | Sim | Não | Não | Não |
| GSM-EFR | ACELP | 8kHz | 12,2 kbit/s | 20–30 ms | Sim | Não | Não | Não |

## Referências ##

* [GSM - Por Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)

