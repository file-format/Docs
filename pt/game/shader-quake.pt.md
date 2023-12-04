{
"data":"11/10/2023",
   "keywords":[
"sombreador",
"arquivo de sombreamento",
"arquivo de shader do mecanismo shader quake 3",
"como abrir um arquivo shader",
"arquivo",
"extensão de arquivo shader",
"extensão",
"arquivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"Formato de arquivo SHADER - Arquivo Shader do Quake 3 Engine",
   "description":"Aprenda sobre o formato de arquivo SHADER Quake 3 Engine Shader e APIs que podem criar e abrir arquivos SHADER.",
"linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
"parent" : "game"
}
},
"última modificação":"11/10/2023"
}

## O que é um arquivo .SHADER?

O formato de arquivo SHADER é usado no **mecanismo Quake 3** para definir shaders para texturas e materiais no jogo. Shaders são usados para especificar como uma superfície deve ser renderizada, incluindo sua aparência, refletividade, transparência e outras propriedades visuais.

## Arquivo SHADER do motor Quake 3

Aqui está uma visão geral básica da estrutura e sintaxe do arquivo shader do mecanismo Quake 3:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

No arquivo de shader do mecanismo Quake 3, você pode definir vários shaders, cada um com seu próprio conjunto de propriedades e estágios. Esses shaders são usados para definir a aparência de diferentes texturas e materiais no mundo do jogo. O mecanismo usa essas informações para renderizar superfícies com efeitos visuais e comportamentos especificados.

Os arquivos shader no mecanismo Quake 3 são arquivos de texto simples que contêm instruções sobre como as texturas e os materiais devem aparecer no jogo. Esses arquivos podem ser abertos e editados com um editor de texto normal e normalmente são encontrados no diretório **"/scripts"** do pacote .PK3 do jogo.

## Motor Quake 3

O mecanismo Quake 3 é um mecanismo de jogo altamente influente e versátil desenvolvido pela id Software. Foi introduzido pela primeira vez com o lançamento do jogo "Quake III Arena" em 1999 e desde então tem sido usado em vários outros jogos. O motor é conhecido por seus gráficos avançados, capacidades multijogador e capacidade de modificação.

Aqui estão alguns recursos e aspectos principais do motor Quake 3:

1. **Mecanismo Gráfico:** O mecanismo Quake 3 era conhecido por sua tecnologia gráfica de ponta na época. Introduziu recursos avançados, como superfícies curvas, shaders e iluminação dinâmica, que foram inovadores no final da década de 1990.
    





2. **Foco multijogador:** Quake 3 Arena foi projetado principalmente como um jogo de tiro em primeira pessoa multijogador. O código de rede do mecanismo e o suporte para jogos multijogador online foram excepcionais, tornando-o uma escolha popular para jogos online competitivos.
    





3. **Modificabilidade:** O mecanismo do Quake 3 é conhecido por sua modificabilidade. A id Software lançou o código-fonte do mecanismo sob licença GNU General Public License (GPL) de código aberto. Isso incentivou a criação de vários mods e mapas personalizados, levando a uma vibrante comunidade de modding.
    





4. **Jogabilidade com script:** O mecanismo usava um sistema baseado em script para definir as regras e o comportamento do jogo, tornando relativamente fácil para modders e mapeadores criarem modos de jogo personalizados e experiências únicas.
    





5. **Suporte para conteúdo personalizado:** O mecanismo do Quake 3 suportava conteúdo personalizado, incluindo texturas, modelos e arquivos de som, o que permitia um alto grau de personalização em mapas e mods criados pelo usuário.
    





6. **Level Design:** O mecanismo usava um sistema de design de níveis baseado em pincel, onde os mapas eram construídos esculpindo espaços em pincéis sólidos. Essa abordagem foi bem documentada e fácil de usar para designers de níveis.


Ao longo dos anos, o motor Quake 3 tem sido usado como base para muitos outros jogos e mods, incluindo "Return to Castle Wolfenstein", "Star Wars Jedi Knight II: Jedi Outcast" e "Urban Terror", entre outros. Deixou um legado duradouro no mundo do desenvolvimento de jogos e ajudou a moldar o gênero de tiro em primeira pessoa. Embora motores mais novos e avançados tenham surgido desde então, o motor Quake 3 continua a ser respeitado por sua contribuição à indústria de jogos.

## Como abrir o arquivo SHADER?

Programas que abrem ou fazem referência a arquivos SHADER incluem

- **id Software Quake 3** (pago) para (Windows, Mac, Linux)
- Bloco de notas da Microsoft
- Bloco de notas ++
- Qualquer editor de texto

## Outros arquivos SHADER

Aqui estão outros tipos de arquivo que usam a extensão de arquivo **.shader**.

**Arquivos do jogo**
- [SHADER - Arquivo de sombreamento do Godot Engine](/pt/game/shader-godot/)
- [SHADER - Arquivo de sombreamento do motor Quake 3](/pt/game/shader-quake/)
- [SHADER - Ativo do Unity Shader](/pt/game/shader-unity/)

## Referências
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

