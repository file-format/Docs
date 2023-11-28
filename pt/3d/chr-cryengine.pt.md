{
"data":"11/10/2023",
   "keywords":[
"chr",
"arquivo chr",
"arquivo de caracteres chr cryengine",
"como abrir um arquivo chr",
"arquivo",
"extensão de arquivo chr",
"extensão",
"arquivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"Formato de arquivo CHR - Arquivo de caracteres CryENGINE",
   "description":"Aprenda sobre o formato de arquivo CHR CryENGINE Character e APIs que podem criar e abrir arquivos CHR.",
"linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
"parent":"3d"
}
},
"último mod":"11/10/2023"
}

## O que é um arquivo .CHR?

O arquivo CHR no contexto do CryENGINE refere-se a um **Arquivo de caracteres CryENGINE**. CryENGINE é um mecanismo de jogo desenvolvido pela Crytek e esses arquivos são usados para armazenar modelos de personagens e dados associados para uso em videogames e outras aplicações em tempo real.

## Arquivo de personagem CryENGINE

Um arquivo de caracteres CryENGINE normalmente contém os seguintes componentes:

1. **Modelo do Personagem**: Este é um modelo 3D do personagem, incluindo sua geometria, texturas e animações. Esses modelos geralmente são criados usando softwares como Autodesk Maya ou Blender e depois importados para o CryENGINE.
    




















2. **Dados de animação**: CryENGINE suporta animações complexas para personagens, portanto o arquivo ".chr" pode incluir várias animações, como caminhar, correr, pular e muito mais. Essas animações normalmente são armazenadas como dados de quadro-chave.
    




















3. **Informações sobre Rigging**: Rigging refere-se ao processo de criação da estrutura do esqueleto para o modelo do personagem, que permite que animações sejam aplicadas ao modelo. O arquivo ".chr" pode conter informações sobre a hierarquia dos ossos e como a malha do personagem está conectada a este esqueleto.
    




















4. **Dados de materiais e texturas**: Informações sobre materiais usados no modelo de personagem e mapas de textura associados podem ser incluídas no arquivo ".chr". CryENGINE suporta renderização baseada em física, então esses materiais podem ser bastante detalhados.
    




















5. **Dados físicos**: Se o personagem pretende interagir com o mundo do jogo, o arquivo ".chr" pode incluir dados físicos, como formas de colisão ou restrições para a física do ragdoll.
    




















6. **Definições de configuração**: Várias definições de configuração relacionadas ao comportamento do personagem no mundo do jogo, como comportamento de IA ou eventos com script, também podem fazer parte do arquivo ".chr".

## CryENGINE

CryENGINE é um poderoso motor de jogo desenvolvido pela Crytek, empresa alemã de videogames. É conhecido por suas capacidades gráficas de ponta e tem sido usado para criar alguns videogames visualmente impressionantes e tecnologicamente avançados. Aqui estão alguns recursos e informações importantes sobre o CryENGINE:

1. **Gráficos e Renderização**: CryENGINE é conhecido por seus recursos gráficos avançados. Ele suporta recursos como iluminação global em tempo real, iluminação e sombras dinâmicas de alta qualidade, renderização baseada em física (PBR) e texturas de alta resolução. Esses recursos contribuem para a criação de mundos de jogo visualmente impressionantes e realistas.
    




















2. **Mecanismo de Física**: O CryENGINE inclui um mecanismo de física integrado que permite interações realistas entre objetos no mundo do jogo. Ele suporta recursos como física de corpo rígido, física de corpo mole e física ragdoll, tornando-o adequado para a criação de ambientes dinâmicos e imersivos.
    




















3. **Terreno e Vegetação**: CryENGINE fornece ferramentas para criar ambientes externos vastos e detalhados. Ele suporta edição de terreno, posicionamento de vegetação e sistemas climáticos dinâmicos, permitindo que os desenvolvedores criem ambientes externos expansivos e realistas.
    




















4. **Animação de personagens**: CryENGINE inclui ferramentas robustas para animação de personagens. Ele suporta plataformas de personagens complexas, animação facial e sistema de árvore de mistura que permite aos desenvolvedores criar movimentos e animações de personagens realistas.
    




















5. **Sistema de IA**: O mecanismo possui um sistema de IA que permite a criação de NPCs (personagens não jogáveis) inteligentes e IA inimiga. Os desenvolvedores podem criar scripts de comportamento e interações de IA para criar experiências de jogo desafiadoras e envolventes.
       





















6. **Scripting**: CryENGINE usa uma linguagem de script chamada "Schematyc" que permite aos desenvolvedores criar lógica e interações de jogo. Além disso, ele oferece suporte a C++ para necessidades de programação mais avançadas.

## Formatos de arquivo usados pelo CryENGINE

Aqui estão alguns tipos de arquivos comuns associados ao CryENGINE:

1. **cryproj**: arquivos do projeto CryENGINE. Esses arquivos armazenam definições e configurações específicas do projeto para um projeto de jogo específico.
    




















2. **.level**: Os arquivos de nível contêm dados do mundo do jogo em 3D, incluindo terreno, objetos, iluminação e outras configurações específicas do nível. Os níveis são componentes fundamentais do design do jogo no CryENGINE.
    




















3. **.cgf**: Formato de geometria de caracteres. Esses arquivos contêm dados de modelos 3D para personagens, objetos e outros recursos do jogo. Os arquivos CGF podem incluir geometria, texturas e dados de animação.
    




















4. **.chrparams**: Arquivos de parâmetros de caracteres. Esses arquivos armazenam definições e configurações para modelos de personagens e suas animações.
    




















5. **.dds**: Formato de textura DirectX. CryENGINE normalmente usa arquivos DDS para armazenar texturas, incluindo mapas difusos, mapas normais e outros tipos de textura.
    




















6. **.cryshader**: Arquivos CryENGINE Shader. Esses arquivos definem como os materiais e objetos são renderizados no mundo do jogo, especificando shaders, propriedades dos materiais e muito mais.
    




















7. **.crytif**: Arquivo de informações de textura. Esses arquivos armazenam informações adicionais sobre texturas, como configurações de compactação, mipmaps e outros detalhes relacionados a texturas.
    




















8. **.cdf**: Arquivo de definição de caracteres. Os arquivos CDF são usados para definir ativos de personagens e suas propriedades, incluindo anexos, estados de animação e configurações relacionadas a personagens.
    




















9. **.dds**: CryENGINE também usa arquivos DDS (DirectDraw Surface) para vários mapas de textura, como mapas normais, mapas especulares e mapas difusos.
    




















10. **.anim**: Arquivos de animação. Esses arquivos armazenam dados de animação de personagens e objetos, incluindo quadros-chave, posições de ossos e sequências de animação.
    




















11. **.xml**: Arquivos XML podem ser usados para diversas configurações e definições de dados dentro do CryENGINE, como lógica de jogo, comportamento de IA e muito mais.
    




















12. **.pak**: [arquivos PAK](/pt/game/pak/) são arquivos usados para empacotar ativos e recursos do jogo, tornando-os mais eficientes para distribuição e carregamento de jogos.

## Como abrir o arquivo CHR?

Os programas que abrem arquivos CHR incluem

- **Crytek CryENGINE SDK** (avaliação gratuita) para Windows

**Subtipo:** Arquivos de imagem 3D

## Outros arquivos CHR

Aqui estão outros tipos de arquivo que usam a extensão de arquivo **.chr**.

**3D**
- [CHR - Arquivo de personagem CryENGINE](/pt/3d/chr-cryengine/)
- [CHR - Arquivo de caracteres do 3ds Max](/pt/3d/chr-3ds/)

**Fonte e Jogo**
- [CHR - Conjunto de caracteres Borland](/pt/font/chr/)
- [CHR - Clube de Literatura Doki Doki! Arquivo de personagem](/pt/game/chr-doki/)

## Referências
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

