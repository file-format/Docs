{
"data": "27/09/2023",
  "keywords": [
"cfg",
"arquivo cfg",
"arquivo de configuração cfg celestia",
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
"title": "Formato de arquivo CFG - Arquivo de configuração do Celestia",
  "description":"Aprenda sobre o formato do arquivo de configuração CFG Celestia e APIs que podem criar e abrir arquivos CFG.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "configurações"
}
},
"último mod": "2023/09/27"
}

## O que é um arquivo .CFG?

Um arquivo de configuração do Celestia é um arquivo de texto simples usado pelo Celestia, programa de simulação de universo 3D. Esses arquivos são vitais para personalizar o comportamento do Celestia, quais objetos celestes são exibidos e como o programa aparece. No entanto, a edição desses arquivos requer muita atenção, pois alterações inadequadas podem atrapalhar o processo de carregamento do Celestia, impedindo-o de funcionar corretamente.

## Celestia

Celestia é um software de simulação de astronomia 3D gratuito e de código aberto que permite aos usuários explorar e visualizar o universo de maneira altamente realista e interativa. Foi desenvolvido por Chris Laurel e lançado pela primeira vez no início dos anos 2000. Celestia está disponível para sistemas operacionais Windows, macOS e Linux.

Os principais recursos e aspectos do Celestia incluem:

- **Visualização 3D realista:** Celestia fornece representação detalhada e precisa de nosso sistema solar, bem como de estrelas, galáxias e outros objetos celestes. Ele usa modelos e texturas 3D de alta qualidade para criar uma experiência visualmente envolvente.

- **Extenso banco de dados celestial:** O software vem com um vasto banco de dados integrado de objetos celestes conhecidos, incluindo estrelas, planetas, luas, asteróides, cometas e naves espaciais. Os usuários podem localizar e explorar facilmente esses objetos.

- **Precisão Científica:** Embora o Celestia seja uma ferramenta de visualização, seu objetivo é representar objetos e fenômenos celestes com a maior precisão possível, com base nos dados científicos disponíveis.

## Formatos de arquivo usados pelo Celestia

Celestia utiliza vários formatos de arquivo para diferentes aspectos de sua simulação astronômica 3D. Aqui estão alguns dos principais formatos de arquivo empregados pela Celestia:

1. **Arquivos de configuração (.cel)**
- *Descrição*: Arquivos de texto simples que permitem aos usuários personalizar o comportamento, a aparência e o conteúdo do Celestia.
- *Objetivo*: Personalizar configurações, definir locais e especificar objetos celestes.

2. **Modelos e malhas 3D**
- *Formatos*: [.3ds](/pt/3d/3ds/), [.obj](/pt/3d/obj/), [.dae](/pt/3d/dae/), .ac
- *Descrição*: Formatos de arquivo de modelo 3D suportados usados para renderizar corpos celestes e naves espaciais.
- *Objetivo*: Exibir objetos 3D no Celestia.

3. **Arquivos de Textura**
- *Formatos*: [.jpg](/pt/image/jpeg/), [.png](/pt/image/png/), [.dds](/pt/image/dds/)
- *Descrição*: Esses arquivos fornecem texturas de superfície para corpos celestes.
- *Objetivo*: Mapear texturas em modelos 3D para obter uma aparência realista.

4. **Catálogos Star e arquivos de dados**
- *Formatos*: formatos personalizados, [.csv](/pt/planilha/csv/), [.tsv](/pt/planilha/tsv/)
- *Descrição*: Arquivos de dados usados para representar estrelas e outros objetos celestes, garantindo uma simulação precisa.
- *Objetivo*: Representação precisa de objetos celestes.

5. **Mapas de Cubo de Textura**
- *Descrição*: Mapas cúbicos são usados para simular a aparência de objetos celestes distantes, como galáxias.
- *Objetivo*: Renderizar objetos distantes com texturas realistas.

6. **Arquivos de script**
- *Descrição*: Esses arquivos contêm scripts personalizados escritos na linguagem de script do Celestia.
- *Objetivo*: Permitir que os usuários criem eventos e animações dinâmicas dentro do universo Celestia.

## Arquivo de configuração Celestia

Aqui está uma visão geral básica do que você pode fazer com o arquivo de configuração do Celestia:

1. **Definindo sua localização**: você pode especificar sua localização na Terra usando parâmetros de latitude, longitude e altitude. Isso permite que o Celestia exiba com precisão o céu noturno a partir da sua posição.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Personalizando suas opções de visualização:** Você pode ajustar diversas opções de visualização, como campo de visão, configurações de tempo e preferências de renderização.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Carregando objetos celestes:** Você pode adicionar objetos celestes como estrelas, planetas, asteróides, naves espaciais e muito mais à sua simulação. Cada objeto é definido no arquivo de configuração com suas propriedades.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Definindo naves espaciais:** Você pode criar sua própria nave espacial fictícia ou usar naves reais especificando seus parâmetros como posição, orientação e modelos 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Criação de scripts:** Você pode escrever scripts na linguagem de script personalizada do Celestia para criar eventos e animações dinâmicas.

## Como abrir o arquivo CFG?

Programas que abrem ou fazem referência a arquivos CFG

- Celestia (grátis) para (Windows, Mac, Linux)

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
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

