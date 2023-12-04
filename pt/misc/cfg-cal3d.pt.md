{
"data": "27/09/2023",
  "keywords": [
"cfg",
"arquivo cfg",
"arquivo de configuração do modelo cfg cal3d",
"o que é um arquivo cfg",
"como abrir arquivo cfg",
"arquivo",
"extensão de arquivo cfg",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo CFG - Arquivo de configuração do modelo Cal3D",
  "description":"Aprenda sobre o formato do arquivo de configuração do modelo CFG Cal3D e APIs que podem criar e abrir arquivos CFG.",
"linktitle": "CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d",
"parent" : "misc"
}
},
"último mod": "27/09/2023"
}

## O que é um arquivo .CFG?

Um arquivo de configuração de modelo Cal3D é um arquivo baseado em texto usado pela biblioteca Cal3D, que é um kit de ferramentas de código aberto para animação de personagens. Este arquivo serve como modelo para a montagem de um modelo tridimensional (3D). Inclui referências a vários componentes do modelo, como estrutura do esqueleto, materiais, animações e muito mais. Essencialmente, atua como um documento central que ajuda a organizar e definir como todas as partes do modelo 3D se encaixam na estrutura Cal3D.

Cal3D é uma biblioteca de animação esquelética frequentemente usada em computação gráfica e desenvolvimento de jogos. Para trabalhar com modelos Cal3D, normalmente você precisa criar um arquivo de configuração que descreva a estrutura, os materiais, as animações e outros atributos do modelo. Abaixo está um exemplo da aparência de um arquivo de configuração de modelo Cal3D.

```
<MODEL>
  <HEADER MAGIC="C3D" VERSION="1050" />

  <!-- Skeleton -->
  <SKELETON>
    <BONE ID="0" NAME="Root">
      <TRANSLATION>0.0 0.0 0.0</TRANSLATION>
      <ROTATION>0.0 0.0 0.0</ROTATION>
      <SCALE>1.0 1.0 1.0</SCALE>
    </BONE>
    <!-- Add more bone definitions here -->
  </SKELETON>

  <!-- Mesh -->
  <MESH>
    <SUBMESH>
      <MATERIAL>MATERIAL_NAME</MATERIAL>
      <VERTEX>
        <!-- Vertex data for the first vertex -->
        <POSITION>0.0 0.0 0.0</POSITION>
        <NORMAL>0.0 0.0 1.0</NORMAL>
        <TEXCOORD>0.0 0.0</TEXCOORD>
        <!-- Add more vertices here -->
      </VERTEX>
      <FACE>
        <!-- Face data for the first face -->
        <VERTEXID>0 1 2</VERTEXID>
        <!-- Add more faces here -->
      </FACE>
      <!-- Add more submeshes here -->
    </SUBMESH>
  </MESH>

  <!-- Animation -->
  <ANIMATION>
    <SKELETON>
      <!-- Define animations and keyframes here -->
    </SKELETON>
  </ANIMATION>

</MODEL>
```

## Cal3D

Cal3D é uma biblioteca de animação de personagens de código aberto usada em computação gráfica 3D e desenvolvimento de jogos. Fornece ferramentas e funcionalidades para criar e animar personagens ou modelos 3D. Cal3D é frequentemente usado para trazer animações de personagens realistas para aplicativos e jogos interativos.

Os principais recursos e componentes do Cal3D incluem:

1. **Malha:** O componente de malha define a geometria 3D de um personagem ou objeto, incluindo vértices, normais e coordenadas de textura. Ele forma a representação visual do modelo.

2. **Esqueleto:** Cal3D permite a criação de uma hierarquia de esqueleto para modelos de personagens. Este esqueleto define a estrutura óssea, e cada osso pode estar associado a uma porção da malha. Os esqueletos são cruciais para animar personagens através da manipulação de ossos.

3. **Materiais:** Os materiais definem como a superfície do modelo deve aparecer quando renderizada. Isso inclui informações sobre texturas, sombreadores e outras propriedades de renderização.

4. **Animações:** Cal3D oferece suporte a diversas técnicas de animação que podem ser aplicadas ao esqueleto. Essas animações definem como os ossos se movem ao longo do tempo para criar animações realistas de personagens, como caminhar, correr ou realizar outras ações.

5. **Arquivos de configuração:** Para usar o Cal3D de maneira eficaz, os modelos geralmente são acompanhados por arquivos de configuração em formato de texto simples. Esses arquivos descrevem a estrutura do modelo, incluindo hierarquia óssea, dados de malha, materiais e informações de animação. Os arquivos de configuração servem como referências para que o Cal3D carregue e interaja corretamente com o modelo.

## Formatos de arquivo usados pelo Cal3D

Cal3D usa vários formatos de arquivo para diferentes finalidades, como armazenamento de dados de modelo, animações e informações de configuração. Aqui estão alguns dos formatos de arquivo comuns usados pelo Cal3D:

1. **Arquivos de modelo binário Cal3D (.cmf):** Esses arquivos armazenam a representação binária de modelos 3D, incluindo geometria de malha, hierarquia óssea e materiais. Os arquivos CMF são usados para carregar e renderizar com eficiência modelos Cal3D em aplicativos.

1. **Arquivos de modelo XML Cal3D (.cmx):** arquivos baseados em XML que armazenam a representação textual de modelos Cal3D. Eles contêm informações sobre a estrutura do modelo, animações, materiais e muito mais. Arquivos [CMX](/pt/image/cmx/) são frequentemente usados para edição e depuração mais legíveis por humanos.

1. **Arquivos de animação Cal3D (.caf):** Esses arquivos armazenam dados de animação, incluindo quadros-chave e transformações ósseas. Os arquivos CAF são essenciais para definir como personagens ou objetos devem se mover e animar dentro de um modelo Cal3D.

1. **Arquivos de meta de metamorfose do Cal3D (.crf):** Usados para definir alvos de metamorfose, que permitem expressões faciais e outras deformações não esqueléticas da malha.

1. **Arquivos de materiais Cal3D (.cfm):** Esses arquivos armazenam informações de materiais para modelos Cal3D. Eles especificam como a superfície do modelo deve ser sombreada, incluindo referências de textura, sombreadores e propriedades de renderização.

1. **Arquivos esqueleto do Cal3D (.csf):** Os arquivos esqueleto armazenam informações sobre a hierarquia óssea e a estrutura de um modelo Cal3D. Eles definem como os ossos são conectados e criados dentro do esqueleto.

1. **Arquivos de configuração Cal3D (.cfg):** Esses arquivos de texto simples servem como arquivos de configuração para modelos Cal3D. Eles contêm referências a vários componentes do modelo, incluindo hierarquia de ossos, dados de malha, materiais e animações. Os arquivos de configuração ajudam o Cal3D a carregar e usar o modelo corretamente.

1. **Formatos de imagem:** Embora não sejam específicos do Cal3D, formatos de arquivo de imagem como [JPEG](/pt/image/jpeg/), [PNG](/pt/image/png/), [BMP](/pt/image/bmp/ ) ou [TGA](/pt/image/tga/) são comumente usados para texturas aplicadas a modelos Cal3D.

## Como abrir o arquivo CFG?

Os programas que abrem arquivos CFG incluem

- Cal3dViewer
- Bloco de notas da Microsoft
- Apple TextEditar
- Qualquer editor de texto

## Outros arquivos CFG

Aqui estão outros tipos de arquivo que usam a extensão de arquivo **.cfg**.

**Configurações**
- [CFG - Arquivo de configuração do Celestia](/pt/settings/cfg-celestia/)
- [CFG - Arquivo de conexão do servidor Citrix](/pt/settings/cfg-citrix/)
- [CFG - Arquivo de configuração MAME](/pt/settings/cfg-mame/)
- [CFG - Arquivo de configuração LightWave](/pt/settings/cfg-lightwave/)

**Jogo**
- [CFG - Arquivo de linguagem de marcação Wesnoth](/pt/game/cfg-wesnoth/)
- [CFG - Arquivo de configuração do MUGEN](/pt/game/cfg-mugen/)
- [CFG - Arquivo de configuração do mecanismo de origem](/pt/game/cfg-sourceengine/)

**Sistema e Diversos**
- [CFG - Arquivo CFG](/pt/system/cfg/)
- [CFG - Arquivo de configuração do modelo Cal3D](/pt/misc/cfg-cal3d/)

## Referências
* [CAL3D](https://github.com/mp3butcher/Cal3D)
