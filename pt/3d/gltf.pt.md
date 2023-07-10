{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "arquivo", "extensão", "formato", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre arquivos GLTF e APIs que podem criar e abrir arquivos GLTF.",
  "title" :"GLTF - Formato de arquivo de transmissão GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo GLTF?

glTF (GL Transmission Format) é um formato de arquivo 3D que armazena informações do modelo 3D no formato JSON. O uso de JSON minimiza o tamanho dos ativos 3D e o processamento em tempo de execução necessário para descompactar e usar esses ativos. Foi adotado para a transmissão e carregamento eficiente de cenas e modelos 3D por aplicativos. glTF foi desenvolvido pelo Khronos Group 3D Formats Working Group e também é descrito como [JPEG](/pt/image/jpeg/) de 3D por seus criadores.

O formato de arquivo GLTF define um formato de publicação comum e extensível para ferramentas e serviços de conteúdo 3D que simplifica os fluxos de trabalho de autoria e permite o uso interoperável de conteúdo em todo o setor. A intenção por trás da criação do formato de arquivo glTF era definir um formato de publicação extensível e comum para ferramentas e serviços de conteúdo 3D que deveriam agilizar os fluxos de trabalho de autoria e permitir o uso interoperável de conteúdo em todo o setor. Ele minimiza o processamento em tempo de execução por aplicativos usando WebGL e outras APIs.

## Breve Histórico do Arquivo GLTF

As primeiras especificações para o formato de arquivo glTF 1.0 foram anunciadas em outubro de 2015. Isso veio como uma série de esforços que começaram em março de 2012 pela Khronos. O objetivo desses esforços era avaliar as oportunidades em torno da tração WebGL. Consequentemente, a primeira demonstração do formato glTF, baseado no formato JSON, foi apresentada no encontro WebGl em 2012. O formato foi adotado por várias empresas de tempos em tempos, incluindo Cesium, 3D Tiles, Oculus, Microsoft, Archilogic e outras.

glTF 2.0 foi publicado em 5 de junho de 2017 na Conferência Web3D 2017. Há uma longa lista de empresas que adotaram o formato de arquivo glTF depois disso.

## Formato de arquivo GLTF

As especificações de formato de arquivo para glTF 2.0 estão disponíveis [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) para referência e devem ser consultadas em qualquer implementação relacionada à leitura/gravação para suporte de formato de arquivo glTF.

glTF define ativos como arquivos JSON com suporte de dados externos. Representa modelos 3D com a ajuda de:

* Descrição completa da cena contida em um arquivo .glTF formatado em JSON que inclui informações sobre hierarquia de nós, materiais, câmeras, bem como informações de descritor para malhas, animações e outras construções
* Arquivos binários (.bin) contendo dados de geometria e animação e outros dados baseados em buffer
* Arquivos de imagem ([.jpg](/pt/image/jpeg/), [.png](/pt/image/png/)) para texturas

Quaisquer ativos externos, como imagens, são armazenados em arquivos externos referenciados via URI. Esses URIs são armazenados ao lado do contêiner GLB ou incorporados diretamente no JSON usando URIs de dados. Cada glTF válido deve especificar sua versão.

glTF foi projetado para atingir tamanho de arquivo pequeno, carregamento rápido, representação de cena 3D completa e extensibilidade. Esses objetivos de design exclusivos são as principais razões para a popularidade do formato de arquivo glTF no domínio 3D. A seguir estão os tipos mime suportados pelo formato de arquivo glTF para diferentes tipos de arquivo:

* Arquivos .gltf usam model/gltf+json
* Arquivos .bin usam application/octet-stream
* Os arquivos de textura usam o tipo oficial image/* com base no formato de imagem específico. Para compatibilidade com navegadores modernos, os seguintes formatos de imagem são suportados: image/jpeg, image/png.

### Codificação JSON

glTF impõe restrições adicionais no formato de arquivo JSON

Para simplificar a implementação do lado do cliente, o glTF tem restrições adicionais no formato e codificação JSON.

1. O JSON deve usar a codificação UTF-8 sem BOM.
1. Todas as strings definidas nesta especificação (nomes de propriedades, enumerações) usam apenas o conjunto de caracteres ASCII e devem ser escritas como texto simples, por exemplo, "buffer" em vez de `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Nomes (chaves) dentro de objetos JSON devem ser únicos, ou seja, chaves duplicadas não são permitidas.

### URIs

Buffers e recursos de imagem são referenciados por meio de URIs. Os dois tipos de URI a seguir devem ser suportados pelos clientes.

** URIs de dados:** os URIs de dados são definidos pela RFC 2397 e são usados pelo glTF para incorporar recursos no JSON.

**Caminhos de URI relativos:** ou path-noscheme conforme definido pela RFC 3986, [Seção 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — sem esquema, autoridade ou parâmetros. Os caracteres reservados devem ser codificados por porcentagem, conforme RFC 3986, [Seção 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Referências ##

* [GlTF 2.0 Specifications - Khronos](https://github.com/KhronosGroup/glTF)
* [formato de arquivo glTF - pela Wikipedia](https://en.wikipedia.org/wiki/GlTF)

