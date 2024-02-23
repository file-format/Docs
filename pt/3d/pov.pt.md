
{
  "date": "2023-01-05",
  "keywords": [
"arquivo pov",
"formato de arquivo pov",
"o que é um arquivo pov",
"arquivo",
"exemplo de ponto de vista",
"extensão de arquivo pov",
"extensão",
"formatar"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Saiba mais sobre o formato de arquivo POV e as APIs que podem abrir e criar arquivos POV.",
  "title": "POV - Arquivo de Persistência de Visão",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-ptv"
}
},
  "lastmod": "2023-01-05"
}

## O que é um arquivo .POV?

Um arquivo POV é um arquivo de texto simples que contém instruções para o software de rastreamento de raios POV-Ray. Estas instruções são escritas em uma linguagem de script especial específica do POV-Ray. Especifica a cena a ser renderizada, incluindo objetos 3D, materiais, iluminação e outras propriedades que definem a aparência da cena. Os arquivos POV usam uma linguagem de script especial específica do POV-Ray e pode ser usada para criar cenas 3D complexas e detalhadas. A extensão de um arquivo POV é normalmente .pov” ou .povray”. Quando você abre um arquivo POV no POV-Ray, o software lê as instruções do arquivo e as utiliza para gerar uma imagem renderizada da cena.

Os arquivos .pov são frequentemente usados por artistas e designers para criar gráficos e animações 3D para uma variedade de aplicações, incluindo filmes, televisão, videogames e materiais de marketing.

## Formato de arquivo POV

O arquivo **.pov** normalmente começa com uma série de instruções **#include**, que são usadas para incluir bibliotecas de cores, texturas e outros recursos predefinidos que podem ser usados na cena. Em seguida, o arquivo define os objetos, materiais e outras propriedades da cena usando uma série de blocos. Existem muitos outros tipos de objetos, materiais e outras propriedades que você pode especificar em um arquivo .pov, e você pode usar loops e instruções condicionais para criar cenas mais complexas e detalhadas.

## Aplicativos de software para POV

O formato de arquivo .pov é usado pelo software de rastreamento de raios POV-Ray, portanto, o principal aplicativo para abrir arquivos .pov é o próprio software POV-Ray. Você pode baixar a versão mais recente do POV-Ray no site oficial em https://www.povray.org/.

Além do POV-Ray, existem vários outros aplicativos que podem abrir e editar arquivos .pov, incluindo:

- BRL-CAD: um software de modelagem 3D de código aberto que pode importar e exportar arquivos .pov
- MeshLab: um software de processamento de malha 3D que pode importar e exportar arquivos .pov
- Blender: um popular software gráfico 3D de código aberto que pode importar e exportar arquivos .pov

Pode haver outros aplicativos de software que também podem abrir arquivos .pov, então você pode tentar usar um visualizador de arquivos ou uma ferramenta de conversão se não conseguir abrir um arquivo .pov com os aplicativos acima.

## Exemplo de ponto de vista

Por exemplo, aqui está um arquivo .pov de amostra que define uma cena com um único cilindro azul:

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

Neste exemplo, o bloco camera especifica a posição e orientação da câmera na cena, o bloco `light_source` declara uma fonte de luz e especifica sua posição e cor, e o bloco `cylinder` declara um objeto cilindro e especifica seus pontos finais, raio e propriedades do material. Ao abrir este arquivo .pov no software POV-Ray, ele renderizará a imagem de um único cilindro azul.

## Referências
 * [POV-Ray - Wikipédia](https://en.wikipedia.org/wiki/POV-Ray)
 * [Site de documentação do POV-Ray](http://www.povray.org/documentation/)

