{
"data": "27/09/2023",
  "keywords": [
"cfg",
"arquivo cfg",
"arquivo de linguagem de marcação wesnoth cfg",
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
"title": "Formato de arquivo CFG - Arquivo de linguagem de marcação Wesnoth",
  "description":"Aprenda sobre o formato de arquivo CFG Wesnoth Markup Language e APIs que podem criar e abrir arquivos CFG.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent": "jogo"
}
},
"último mod": "27/09/2023"
}

## O que é um arquivo .CFG?

O arquivo CFG também é conhecido como **"Wesnoth Markup Language" (WML)**. É uma linguagem de marcação personalizada usada principalmente no jogo "Battle for Wesnoth", que é um jogo de estratégia baseado em turnos. WML é usado para definir e personalizar vários aspectos do jogo, incluindo cenários, campanhas, unidades e muito mais. É uma forma de modders e desenvolvedores criarem conteúdo para o jogo.

Ele é escrito em um formato que lembra uma combinação de XML e scripts simples. Aqui está uma visão geral de alguns elementos e estruturas comuns que você pode encontrar em um arquivo WML:

1. **Tags:** WML usa tags para definir diferentes elementos do jogo. As tags são colocadas entre colchetes angulares. Por exemplo:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Atributos:** Dentro das tags, você pode definir atributos para especificar propriedades ou valores associados ao elemento. No exemplo acima, “type” e “hitpoints” são atributos.
    










3. **Matrizes e Matrizes de Matrizes:** Você pode criar matrizes de dados e até mesmo matrizes de matrizes para definir listas de unidades, tipos de terreno ou outros elementos do jogo.
    










4. **Declarações Condicionais:** WML suporta declarações condicionais para controlar o fluxo do jogo. Por exemplo:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Loops:** você pode usar loops para percorrer listas de itens ou executar ações repetidamente.
    










6. **Inclui:** Você pode incluir outros arquivos WML em um arquivo WML principal para organizar e modularizar seu conteúdo.
    










7. **Manipuladores de eventos:** Você pode definir manipuladores de eventos para acionar ações quando eventos específicos ocorrem no jogo.
    











Aqui está um exemplo simplificado de um arquivo WML que define uma unidade personalizada:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## A Batalha por Wesnoth

"The Battle for Wesnoth" é um jogo de estratégia popular e de código aberto baseado em turnos. Está disponível para várias plataformas, incluindo Mac, Windows, Linux e muito mais. Desenvolvido por uma comunidade dedicada de voluntários, o jogo é conhecido por sua jogabilidade profunda e envolvente, bem como por seu rico mundo de fantasia.

Os principais recursos de "A Batalha por Wesnoth" incluem:

1. **Cenário de fantasia:** O jogo se passa em um mundo de fantasia com várias raças, incluindo humanos, elfos, anões, orcs e muito mais. A tradição e a narrativa do jogo são parte integrante de seu apelo.
    










2. **Estratégia baseada em turnos:** A jogabilidade é baseada em turnos, onde os jogadores dedicam seu tempo para planejar e executar seus movimentos em grades hexagonais. Combina combate tático com tomada de decisões estratégicas.
    










3. **Campanhas:** O jogo oferece uma ampla variedade de campanhas para um jogador, cada uma com seu próprio enredo, personagens e desafios. Os jogadores podem explorar diferentes narrativas e cenários.
    










4. **Multijogador:** "Wesnoth" oferece suporte ao modo multijogador online, permitindo que os jogadores compitam entre si em batalhas estratégicas. Os modos multijogador incluem jogo cooperativo e partidas competitivas.

## Como abrir o arquivo CFG?

Os arquivos CFG, que são comumente associados à Wesnoth Markup Language (WML) usada no jogo "The Battle for Wesnoth", podem ser facilmente editados usando qualquer editor de texto padrão. Esses arquivos contêm código legível escrito em WML, que define vários aspectos do jogo, incluindo cenários, unidades e campanhas.

Embora você possa usar qualquer editor de texto para modificar arquivos CFG, alguns editores de texto avançados como Emacs e Vi têm plug-ins de realce de sintaxe WML disponíveis. Esses plug-ins fornecem codificação de cores e formatação úteis para tornar mais fácil para os usuários distinguirem diferentes elementos e estruturas dentro do código WML.

Programas que abrem ou fazem referência a arquivos CFG incluem

- A Batalha por Wesnoth (Grátis) para (Windows, MAC, Linux)
- Bloco de notas da Microsoft

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
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
