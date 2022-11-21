{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "arquivo", "extensão", "formato de arquivo", "implementação de erb", "Guia de programação", "exemplo de erb", "eRuby", "formato de arquivo eRuby", "script de idioma eRuby", " modelos eRuby", "linguagem erb", "linguagem ERB Ruby", "linguagem eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - arquivo de idioma eRuby",
  "description":"Saiba mais sobre o formato de arquivo ERB e APIs que podem criar e abrir arquivos ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## O que é um arquivo ERB?

A linguagem eRuby é um sistema de modelagem que incorpora Ruby em um documento de texto. O sistema de modelagem do eRuby combina o código ruby e o texto simples para fornecer controle de fluxo e substituição de variáveis, facilitando assim a manutenção. É frequentemente usado para incorporar código Ruby em um documento [HTML](/pt/web/html/), semelhante a АSР, [JSР](/pt/programming/jsp/) e [РHР](/pt/programming/php/) e outro servidor linguagens de script lateral. ERB Ruby geralmente gera páginas da Web.

O módulo de visualização do Ruby on Rails é responsável por exibir a resposta ou saída em um navegador. Em sua forma mais simples, uma visão pode ser um pedaço de código HTML que tem algum conteúdo estático. Para a maioria das aplicações, apenas ter conteúdo estático pode não ser suficiente. Muitos aplicativos do Rails exigirão que o conteúdo dinâmico criado pelo controlador seja exibido em sua exibição. Isso é possível usando Embedded Ruby para gerar modelos que podem conter conteúdo dinâmico.

Ruby incorporado permite que o código ruby seja incorporado em um documento de visualização. Este código é substituído pelo valor apropriado resultante da execução do código em tempo de execução. Mas, por ter a capacidade de incorporar código em um documento de exibição, corremos o risco de fazer uma ponte sobre a separação clara presente no quadro MVС. É, portanto, responsabilidade do desenvolvedor certificar-se de que há uma separação clara de responsabilidade entre o modelo, visualização e módulos de controle da aplicação.



## Breve história ##

Ruby desenhou-se em meados dos anos 1990 por Yukihir® Matsumot®. Yukihiro Matsumoto é o pai de Ruby e na comunidade Ruby, ele é conhecido como Matz'. O script Ruby foi introduzido inicialmente em 1995 e a primeira versão do Ruby foi o Ruby 95, lançado em 1995.

Yukihirо Matsumоtо queria uma linguagem de programação totalmente orientada a objetos que pode ser facilmente usada como uma linguagem de script. Então, ele projetou a linguagem eRuby. Em uma sessão de Yukihirо Matsumоtо e Keiju Ishitshukа, dois nomes foram alistados para a linguagem de programação que é "Соrаl" e "Ruby", mais tarde, Yukihirо Matsumоtо selecionou o nome "Ruby".


## Especificação Técnica ##

O formato de arquivo eRuby suporta diferentes conceitos de programação orientada a objetos como classe, herança, abstração, polimorfismo e execução, etc. O recurso de programação orientada a objetos facilita a manutenção e o desenvolvimento. O script de linguagem eRuby também suporta o recurso de programa de programação processual. Na programação processual, existem etapas especificadas para cada programa para resolver um problema específico.

Os modelos eRuby fornecem uma vasta gama de bibliotecas ricas embutidas com as quais os programadores podem desenvolver qualquer aplicativo ou programa da web de maneira fácil e rápida. eRuby é uma linguagem de programação de propósito geral ou multifuncional, o que significa que pode ser usado por programadores no desenvolvimento de diferentes tipos de aplicações e programas.

A linguagem ERB Ruby é uma linguagem de programação simples e de código aberto e você também pode modificá-la de acordo com os requisitos do seu projeto. Ele fornece vários tipos de recursos e ferramentas ricas embutidas. A linguagem também fornece o recurso de coletor de lixo automático.

Соding em eRuby é muito rápido em relação a outras linguagens de programação. E também é uma linguagem de programação flexível, pois permite que cada usuário modifique suas peças de acordo com seus requisitos. Ele suporta o recurso de herança única e mixins e também fornece recurso de digitação dinâmica para seus usuários. eRuby é uma linguagem de programação sensível a maiúsculas e minúsculas e tem uma grande comunidade de suporte por causa de sua sensibilidade.


## Exemplo de formato de arquivo ERB ##

A seguir estão os tipos de tags nos modelos ERB:

### Expressão ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Execução ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### Comentários ###

```
<%# %>
```

```
<%# ruby code %>
```

### Outras tags ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Exemplo de classe ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## Referência ##

* [ERB - pela Wikipedia](https://en.wikipedia.org/wiki/ERuby)



