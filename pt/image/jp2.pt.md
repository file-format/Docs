{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo jp2", "formato de arquivo jp2", "o que é um arquivo jp2", "arquivo", "exemplo jp2", "extensão de arquivo jp2", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo JP2 e APIs que podem criar e abrir arquivos JP2.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## O que é um arquivo JP2? ##

JPEG 2000 (**JP2**) é um sistema de codificação de imagem e padrão de compressão de imagem de última geração. Ele usa a tecnologia wavelet para codificar conteúdo sem perdas em qualquer qualidade de uma só vez. Além disso, sem nenhuma penalidade substancial na eficiência de codificação, o JPEG 2000 tem a capacidade de acessar e decodificar o mesmo conteúdo de forma eficaz em uma variedade de outras resoluções e qualidades. Os fluxos de código em JPEG 2000 são significativamente escaláveis com regiões de interesse que fornecem a facilidade de acesso espacial aleatório.

JPEG 2000 destaca-se por ser um dos padrões mais escaláveis. Diferentes partes de uma imagem podem ser armazenadas usando diversas qualidades. Uma escalada de desempenho notável pode ser alcançada ordenando o fluxo de código de várias maneiras. No entanto, o JP2 requer codificadores/decodificadores complexos e computacionalmente desafiadores, como resultado dessa flexibilidade. Em comparação com o JPEG, o JPEG 2000 produz apenas artefatos de toque que fazem anéis perto da borda da imagem e podem ficar desfocados, enquanto o JPEG usa blocos de artefatos visuais 8×8 que podem ser artefatos de toque e bloqueio. Possuindo até 16384 componentes diversos com as dimensões em terapixels, e precisão que pode chegar a 38 bits/amostra.

## História ##

Em 2000, o comitê do Joint Photographic Experts Group projetou o JP2 com o objetivo de melhorar seu próprio padrão JPEG baseado em transformada de cosseno discreto com este novo método baseado em wavelet. O comitê do JPEG pretendia fornecer seus métodos básicos livres de taxas de licença. Na licença JP2, ganhando concorrência entre 20 empresas, eles venceram por um triz. O JPEG 2000 foi declarado como um padrão ISO, embora a maioria dos navegadores da Web não esteja pronta para dar uma mão ao JPEG 2000 desde 2017.

## Partes do sistema de codificação de imagem JPEG 2000 ##

A seguir estão as partes principais que constituem o conjunto completo de padrões para JPEG 2000.


|Parte|Título|Descrição|Número
---|---|---|---|
|Parte 1|Sistema de codificação do núcleo| Define a sintaxe do fluxo de código. Diferentes etapas envolvidas na decodificação de imagens JPEG 2000. Explica o formato de arquivo básico JP2, metadados e direitos de IP a serem fornecidos.|ISO/IEC 15444-1
|Parte 2|Extensões|Define extensões para fluxo de código de formato de arquivo e permite demonstrações de amostra HDR, especificação de espaço de cores, corte, transformações geométricas; diversas animações, metadados e vários fluxos de código.|ISO/IEC 15444-2
|Parte 3|Motion JPEG 2000 (MJ2 ou MJP2)|Introduza um formato de arquivo para sequências de movimento, codificando imagens em um fluxo de código independente.|ISO/IEC 15444-3
|Parte 4|Conformidade|Informa técnicas de teste para codificação e decodificação e verifica arquivos para fluxos de código simples e arquivos JP2.|ISO/IEC 15444-4
|Parte 5|Software de referência|Compreende dois pacotes de código-fonte (Java, C) que implementam o sistema de codificação Core e estão disponíveis sob licenças de código aberto.|ISO/IEC 15444-5
|Parte 6|Formato de arquivo de imagem composta|Define o formato de arquivo JPM e permite imagens de documentos de várias páginas para aplicativos semelhantes a fax. Suporta o uso de JBIG2 e JPEG.|ISO/IEC 15444-6
|Parte 8|JPEG 2000 Secured (JPSEC)|Assegura a segurança de transações, conteúdos e tecnologias, e permite fluxos de bits JPEG 2000 seguros.|ISO/IEC 15444-8
|Parte 9|JPIP|Define ferramentas em um ambiente de rede para acessar metadados e imagens, e declara Protocolos interativos e eficientes|ISO/IEC 15444-9
|Parte 10|JP3D|Extensão volumétrica da Parte 1 e introduz a dimensão Z. Estende o conceito de blocos, blocos de código, recintos e recursos de acessibilidade 3D de região de interesse.|ISO/IEC 15444-10
|Parte 11|JPWL|Lida com transmissão bem organizada em uma rede sem fio propensa a erros. Esta extensão é compatível com decodificadores|ISO/IEC 15444-11
|Parte 13|Codificador de nível básico|Define uma implementação de codificador de nível básico do sistema de codificação Core.|ISO/IEC 15444-13
|Parte 14|JPXML|Uma representação em XML e explica os segmentos de marcadores e métodos para acessar os dados internos de imagens.|ISO/IEC 15444-14
|Parte 15|HTJ2K (Em desenvolvimento)|Especifica um algoritmo de codificação de bloco alternativo. O algoritmo oferece uma taxa de transferência dez vezes maior e codificação/decodificação sem perdas.|

## Formato de arquivo JP2 ##

O JPEG 2000 define o formato do arquivo e o fluxo de código da mesma forma que o JPEG-1. Embora as amostras de imagem sejam descritas exclusivamente pelo JPEG 2000, o JPEG-1 inclui outras informações adicionais sobre o espaço de cores e a resolução essenciais para codificar a imagem. Se uma imagem armazenada como arquivo JPEG 2000, o **.jp2** é usado como extensão. Esse formato de arquivo é aprimorado ainda mais pela extensão JPEG 2000 part-2, que define mecanismos de animação e configuração de vários fluxos de código em uma única imagem. A extensão **.jpx** é usada quando as imagens são salvas usando este formato de arquivo estendido. Como os dados de fluxo de código não são considerados salvos principalmente em arquivos, nenhuma extensão padrão é definida para essa finalidade. Embora para fins de teste, ele frequentemente recebe a extensão **.jpc** ou **.j2k**. Ao contrário do JPEG-1, o JPEG 2000 escolhe uma maneira diferente de codificar metadados no formato XML. O padrão 12234-1.4 (pelo comitê ISO TC42) é usado como referência entre as tags Exif e os componentes XML. JPEG 2000 pode conter um padrão ISO, XMP dentro.

### Pedaços ###
Os arquivos JPEG 2000 consistem em pedaços consecutivos. Cada bloco tem um cabeçalho de 8 bytes: tamanho de bloco de 4 bytes (big-endian, byte alto primeiro) e tipo de bloco de 4 bytes - uma das assinaturas pré-definidas: "jP" ou "jP2".

O segundo bloco deve ser do tipo "ftyp" e ter um subtipo no deslocamento 8. JPEG 2000 definido pelo subtipo que deve ser um dos valores: "jp2 "(tipo de arquivo \*.JP2), "jp20" (arquivo tipo \*.JPA), "jpm " (tipo de arquivo \*.JPM), "jpx " (tipo de arquivo \*.JPX).

Iterando pedaços, até que um tipo desconhecido seja detectado, compomos o arquivo de imagem/vídeo JPEG 2000.

### Transformação de cor ###

Inicialmente, é necessária a transformação das imagens do espaço de cores RGB para outro espaço de cores. Para isso, existem duas formas: Transformação de Cor Irreversível (ICT) e Transformação de Cor Reversível (RCT). O primeiro usa o espaço de cores YC,,B,,C,,R,, e deve ser implementado em ponto fixo/flutuante, enquanto mais tarde um espaço de cores YUV modificado e de natureza reversível.// //Não restrito ao modelo RGB, JPEG A linguagem 2000 usa a transformação de vários componentes.

### Revestimento ###

Quando a transformação de cor é feita, a imagem é convertida em regiões retangulares chamadas de ladrilhos que podem ser transformadas e codificadas separadamente. O tamanho de todos os blocos terá o mesmo ou a imagem inteira pode ser considerada como um único bloco. O decodificador aproveita a vantagem do ladrilho e consome menos memória ou pode codificar parcialmente alguns ladrilhos. Embora esta técnica tenha uma desvantagem de degradação da qualidade da imagem.

### Transformação wavelet ###

A imagem após o ladrilho é transformada em wavelet que pode ser irreversível ou reversível e implementada usando o esquema de convolução ou levantamento.

### Taxa de compressão ###

Dependendo das características físicas de uma imagem, é obtido um ganho de compressão de 20% A previsão de redundância espacial do JPEG 2000 desempenha um papel vital no processo de compressão e as imagens de alta resolução tendem a ganhar mais vantagens.

## Aplicativos atendidos pelo padrão ##

* Gravação, edição e armazenamento de vídeos HD baseados em quadros
* Imagens médicas e biometria
* imagens de satélite, sensoriamento remoto e detecção de movimento
* Comunicação cliente/servidor, distribuição e armazenamento em rede.
* Cinema digital, contribuição de alimentação HDTV ao vivo, material audiovisual digitalizado

## Referências ##

* [Visão geral do JPEG 2000](https://jpeg.org/jpeg2000/)
* [Sistema de codificação de imagem JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

