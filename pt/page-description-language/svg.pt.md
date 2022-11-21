{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "arquivo", "formato de arquivo", "Linguagem de descrição de página", "Escalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo SVG e APIs que podem criar e abrir arquivos SVG.",
  "title" :"O que é um arquivo SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## O que é um arquivo SVG? ##

Um arquivo SVG é um arquivo Scalar Vector Graphics que usa o formato de texto baseado em XML para descrever a aparência de uma imagem. A palavra Escalável refere-se ao fato de que o SVG pode ser dimensionado para diferentes tamanhos sem perder qualidade. A descrição baseada em texto desses arquivos os torna independentes da resolução. É um dos formatos mais usados para construir um site e imprimir gráficos para alcançar escalabilidade. O formato só pode ser usado para gráficos bidimensionais. Os arquivos SVG podem ser visualizados/abertos em quase todos os navegadores modernos, incluindo Chrome, Internet Explorer, Firefox e Safari.

## Breve história ##

As especificações SVG estão disponíveis como padrão aberto pelo World Wide Web Consortium (W3C) desde 1999. Antes disso, especificações de formato de arquivo semelhantes em seis formatos diferentes foram submetidas ao W3C até 1998. Uma atualização foi aplicada às especificações em 2011 e foi versionado 1.1 . Em 2016, o SVG 2 foi publicado como uma versão mais recente, incluindo recursos adicionais aos do SVG 1.1.

## Especificações de formato de arquivo ##

O SVG Document Object Model (DOM) estabelece as bases para todas as especificações e interfaces que correspondem às seções específicas das especificações. Os visualizadores de SVG devem implementar as interfaces SVG DOM conforme definido nas especificações do W3C. Seu DOM expõe várias interfaces para diferentes tipos de dados e elementos.

### Formas SVG ###

O SVG possui alguns elementos de forma predefinidos que podem ser usados pelos desenvolvedores:

* Retângulo<rect>
* Círculo<circle>
* Elipse<ellipse>
* Linha<line>
* Polilinha<polyline>
* Polígono<polygon>
* Caminho<path>

Com base nessas formas e especificações, as áreas funcionais do SVG são as seguintes.

**Caminhos** - Os caminhos são usados para representar contornos de formas simples e compostas. Codificações são usadas para definir a natureza da operação. Por exemplo, M é usado para Move To, L é usado para Line To, Z é usado para fechar um caminho e assim por diante.

**Formas básicas** - Caminhos de linha reta e caminhos compostos de uma série de segmentos de linha reta conectados (polilinhas), bem como polígonos fechados, círculos e elipses podem ser desenhados. Retângulos e retângulos de cantos arredondados também são elementos padrão.

**Texto** - A representação de texto é expressa como dados de caracteres XML, onde muitos efeitos visuais podem ser aplicados ao texto. As especificações permitem lidar com texto bidirecional, texto vertical e caracteres ao longo de um caminho curvo.

**Pintura** - As formas podem ser preenchidas e/ou contornadas com uma cor, um gradiente ou um padrão, permitindo a capacidade de torná-la opaca ou ter qualquer grau de transparência. Recursos de final de linha, como pontas de seta ou símbolos que aparecem nos vértices de um polígono, são representados por marcadores.

**Cor** - As especificações SVG permitem aplicar cores a todos os elementos SVG visíveis, diretamente ou por meio de preenchimento, traçado e outras propriedades. Diferentes códigos de cores podem ser usados para especificar como preto ou azul, representação hexadecimal, decimal ou como porcentagens do formato RGB.

**Gradientes e padrões** - As formas em um arquivo SVG podem ser preenchidas ou contornadas com cores sólidas, gradientes ou padrões repetidos.

**Efeitos de filtro** - Na verdade, é uma série de operações gráficas que são aplicadas a um determinado gráfico vetorial de origem para produzir um resultado modificado.

**Interatividade** - Os usuários podem interagir com arquivos SVG alterando o foco, clicando no mouse, rolando ou ampliando a imagem. A Interatividade permite que as imagens SVG interajam com os usuários de diversas maneiras, conforme mencionado anteriormente.

**Links** - É possível que imagens SVG tenham hiperlinks para outros documentos. Isto é conseguido através do XML Linking Language ou XLink. Isso permite a criação de estados de visualização específicos que são usados para aumentar/diminuir o zoom de uma área específica ou para limitar a visualização a um elemento específico.

**Scripting** - Semelhante ao HTML, todos os aspectos de um documento SVG são acessíveis para manipulação usando scripts. Os objetos SVG DOM fornecem a orientação para conseguir isso usando o elemento e atributo SVG. Os scripts são incluídos em elementos de tag `script` e podem ser executados em resposta a eventos de ponteiro, teclado ou documento, conforme necessário.

**Animação** - Os elementos DOM<animate> ,<animateMotion> e<animateColor> permite incluir animação para conteúdo SVG. Claro, isso não é possível sem o uso de scripts e temporizadores embutidos. Essas animações podem ser contínuas e podem ser colocadas em loop, bem como repetidas, ao mesmo tempo em que respondem aos eventos do usuário.

**Fontes** - O texto em SVG pode fazer referência a arquivos de fontes externas, como fontes do sistema. Na ausência de tais fontes, o texto em SVG não será renderizado na saída. Isso pode ser superado incorporando os glifos necessários em um arquivo como uma fonte que é renderizada usando o<text> elemento.

## Exemplos ##
As linhas a seguir mostram como um Círculo é representado usando o script SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

As linhas de código a seguir mostram como usar o<text> bloco para renderizar texto para SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referências ##

* [Especificações SVG W3C](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

