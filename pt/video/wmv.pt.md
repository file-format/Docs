{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo WMV",
  "description":"Saiba mais sobre o formato de arquivo WMV e APIs que podem criar e abrir arquivos WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## O que é um arquivo WMV?

O Advanced Systems Format (ASF) é um contêiner multimídia digital projetado principalmente para armazenar e transmitir fluxos de mídia. Microsoft Windows Media Video (WMV) é o formato de vídeo compactado e Microsoft Windows Media Audio (WMA) é o formato de áudio compactado junto com metadados adicionais no contêiner ASF desenvolvido pela Microsoft. Depois que os arquivos WMV ou WMA são codificados com os codecs Windows Media Video e Windows Media Audio, eles são representados com a extensão .asf. O WMV compacta arquivos grandes para uma melhor taxa de transmissão em uma rede, mantendo a qualidade do vídeo. O WMV foi projetado especificamente para ser executado em todos os dispositivos Windows. Após a padronização pela Society of Motion Picture and Television Engineers (SMPTE), o WMV agora é considerado um formato padrão aberto.

## História ##

Com a ajuda de codecs proprietários da Microsoft, um novo formato de vídeo compactado foi desenvolvido em 1999, conhecido como WMV7, que foi baseado em MPEG-4 Parte 2. Melhorias foram adicionadas em outras duas versões, ou seja, WMV8 e 9. A Microsoft enviou uma versão 9^^th^^ de WMV para SMPTE para padronização em 2003, que acabou sendo padronizado em 2006 como SMPTE 421M também conhecido como VC-1. A ideia por trás do WMV era desenvolver um formato de mídia que pudesse ser suportado por todos os hardwares e softwares suportados pela Microsoft. Além disso, outro objetivo principal era transmitir fluxos de vídeo pela internet em um cenário ideal. Após a padronização do SMPTE, o WMV também se tornou um formato de vídeo para discos Blu-ray.

## Especificações de formato de arquivo

### Contêiner

Geralmente, o WMV é embalado em um contêiner ASF, mas, além disso, o contêiner Matroska ou AVI também pode suportá-lo com extensões de .mkv e .avi, respectivamente.

### Vídeo do Windows Media 9

Embora existam vários codecs de áudio e vídeo disponíveis na série Windows Media Video 9 para autoria e reprodução de mídia digital, o codec WMV-9 é o codec de vídeo mais recente e melhor, pois pode atingir a compactação ideal a partir de taxas de bits muito baixas, ou seja, 160 x 120 a 10 Kbps a 1920 x 1080 a 4-8 Mbps para uma variedade de vídeos HD.

### Estrutura do Codec

WMV-9 tem um formato de cor interna de 8 bits 4:2:0. Como todos os outros padrões populares de compressão de vídeo MPEG-1 e H.261, o WMV-9 usa uma compensação de movimento baseada em blocos e um esquema de transformação espacial. Em geral, podemos dizer que esses padrões realizam a compensação de movimento bloco a bloco do quadro reconstruído anterior com a ajuda de uma quantidade 2-D chamada vetor de movimento (MV) para sinalizar o deslocamento espacial. O bloco atual é formado com a ajuda da previsão dos valores do mesmo tamanho do quadro reconstruído anterior que é deslocado da posição atual pelo vetor de movimento. Eventualmente, o erro residual é calculado como a diferença entre o bloco previsto com compensação de movimento e o bloco real. Este erro residual é transformado usando uma transformação linear de compactação de energia, então quantizada e codificada por entropia.

Os coeficientes de transformada quantificados são decodificados por entropia, desquantizados e transformados inversamente para produzir uma aproximação do erro residual no lado do decodificador, que é então adicionado à previsão compensada por movimento para gerar a reconstrução. A descrição de alto nível do codec é mostrada na imagem a seguir.

O restante da seção discutirá as novas melhorias no WMV-9 que o diferenciam do restante das soluções de codificação de vídeo, como os padrões MPEG. O WMV-9 possui quadros intra (I), previstos (P) e previstos bidirecionalmente (B). Intra frames são aqueles que são codificados independentemente e não dependem de outros frames. Quadros previstos são quadros que dependem de um quadro no passado. A decodificação de um quadro previsto pode ocorrer somente após todos os quadros de referência anteriores ao quadro atual, começando pelo quadro (I) mais recente, terem sido decodificados. Os quadros B são quadros que têm duas referências – uma no passado temporal e outra no futuro temporal. Os quadros B são transmitidos após suas referências, o que significa que os quadros B são enviados fora de ordem para garantir que suas referências estejam disponíveis no momento da decodificação. Os quadros B em WMV-9 não são usados como referência para quadros subsequentes. Isso coloca os quadros B fora do loop de decodificação, permitindo que atalhos sejam usados durante a decodificação de quadros B sem desvios ou artefatos visuais de longo prazo. A definição acima de quadros I, P e B vale para sequências progressivas e entrelaçadas.

O desempenho dos codecs de vídeo é comparado ao gráfico de distorção de taxa (RD). É uma curva 2-D que mostra a distorção produzida pela compressão em uma determinada taxa de bits.

O WMV-9 abordou esse problema com a introdução de uma variedade de técnicas listadas abaixo:

1. Transformação de tamanho de bloco adaptável

2. Conjunto de transformação de precisão limitada

3. Compensação de movimento

4. Quantização e desquantização

5. Codificação de entropia avançada

6. Filtragem de loop

7. Codificação avançada do quadro B

8. Codificação entrelaçada

9. Suavização de sobreposição

10. Ferramentas de baixo custo

11. Compensação de desvanecimento

## Referências ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html )
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


