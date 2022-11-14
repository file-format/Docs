{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "file", "estensione", "formato file", "implementazione eRuby", "Guida alla programmazione", "esempio eRuby", "eRuby", "formato file eRuby", "script in linguaggio eRuby", " modelli eRuby", "linguaggio erb", "linguaggio ERB Ruby", "linguaggio eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - File di lingua eRuby",
  "description":"Scopri il formato di file ERB e le API che possono creare e aprire file ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Che cos'è un file ERB?

Il linguaggio eRuby è un sistema di modelli che incorpora Ruby in un documento di testo. Il sistema di modelli di eRuby combina il codice rubino e il testo semplice per fornire il controllo del flusso e la sostituzione delle variabili, rendendo così facile la manutenzione. Viene spesso utilizzato per incorporare il codice Ruby in un documento [HTML](/it/web/html/), simile a АSР, [JSР](/it/programming/jsp/) e [РHР](/it/programming/php/) e altri server -lingue di scrittura laterale. ERB Ruby di solito genera pagine Web.

Il modulo di visualizzazione di Ruby on Rails è responsabile di visualizzare la risposta o l'output su un browser. Nella sua forma più semplice, una vista può essere un pezzo di codice HTML che ha alcuni contenuti statici. Per la maggior parte delle applicazioni, il solo contenuto statico potrebbe non essere sufficiente. Molte applicazioni di Rails richiederanno che il contenuto dinamico creato dal controller venga visualizzato nella loro vista. Ciò è possibile utilizzando Embedded Ruby per generare modelli che possono contenere contenuti dinamici.

Embedded Ruby consente di incorporare il codice rubino in un documento di visualizzazione. Questo codice viene sostituito con il valore corretto risultante dall'esecuzione del codice in fase di esecuzione. Ma, avendo la possibilità di incorporare il codice in un documento di visualizzazione, rischiamo di colmare la chiara separazione presente nel frame MVС. È quindi responsabilità dello sviluppatore assicurarsi che vi sia una chiara separazione di responsabilità tra i moduli modello, vista e controllo dell'applicazione.



## Breve storia ##

Ruby è stato progettato a metà degli anni '90 da Yukihir® Matsum®. Yukihir® Matsumto® è il padre di Ruby e nella comunità di Ruby, è notoriamente conosciuto come Matz'. La sceneggiatura di Ruby è stata inizialmente introdotta nel 1995 e la prima versione di Ruby è stata Ruby 95 che è stata rilasciata nel 1995.

Yukihir® Matsumо ha voluto una lingua di programmazione completamente orientata all'oggetto che potesse essere facilmente utilizzata come lingua di scrittura. Quindi, ha progettato il linguaggio eRuby. In una sessione di Yukihir® Matsumо e Keiju Ishitshuk sono stati arruolati due nomi per la lingua di programmazione che è "Соrаl" e "Ruby", in seguito Yukihir® Mаtsumоtо ha selezionato il nome "Ruby".


## Specifiche tecniche ##

Il formato di file eRuby supporta diversi concetti di programmazione orientata all'oggetto come classe, ereditarietà, astrazione, polimorfismo e inclusione, ecc. La caratteristica della programmazione orientata all'oggetto all'avvicinarsi facilita la manutenzione e lo sviluppo. La scrittura in lingua eRuby supporta anche la funzione di approccio alla programmazione. Nella programmazione procedurale ci sono passaggi specifici per ogni programma per risolvere un particolare problema.

I modelli eRuby forniscono una vasta gamma di librerie integrate di classe ricca con le quali i programmatori possono sviluppare qualsiasi applicazione web o programma in modo facile e veloce. eRuby è un linguaggio di programmazione generico o multiuso, il che significa che può essere utilizzato dai programmatori nello sviluppo di diversi tipi di applicazioni e programmi.

ERB Ruby language è una lingua di programmazione semplice e aperta e puoi anche modificarla in base alle tue esigenze. Fornisce vari tipi di caratteristiche e strumenti integrati ricchi. La lingua fornisce anche la funzione di raccoglitore di rifiuti automatico.

Usare in eRuby è molto veloce rispetto ad altre lingue di programmazione. Ed è anche un linguaggio di programmazione flessibile in quanto consente a ogni utente di modificare le sue parti in base alle proprie esigenze. Supporta l'eredità singola e la funzionalità di mixin e fornisce anche la funzionalità di digitazione dinamica ai suoi utenti. eRuby è un linguaggio di programmazione sensibile ai casi e ha una grande comunità di supporto a causa della sua sensibilità.


## Esempio di formato file ERB ##

Di seguito sono riportati i tipi di tag nei modelli ERB:

### Espressione ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Esecuzione ###

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

### Commenti ###

```
<%# %>
```

```
<%# ruby code %>
```

### Altri tag ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Esempio di classe ###

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

## Riferimento ##

* [ERB - di Wikipedia](https://en.wikipedia.org/wiki/ERuby)



