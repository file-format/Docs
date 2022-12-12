{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "plik", "rozszerzenie", "format pliku", "implementacja erb", "Przewodnik programowania", "przykład erb", "eRuby", "format pliku eRuby", "skrypt języka eRuby", " szablony eRuby", "język erb", "język ERB Ruby", "język eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - plik językowy eRuby",
  "description":"Dowiedz się o formacie pliku ERB i interfejsach API, które mogą tworzyć i otwierać pliki ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Czym jest plik ERB?

Język eRuby to system szablonów, który osadza język Ruby w dokumencie tekstowym. System szablonów eRuby łączy kod ruby i zwykły tekst, aby zapewnić kontrolę przepływu i zmienne zastępowanie, ułatwiając w ten sposób konserwację. Jest często używany do osadzania kodu Ruby w dokumencie [HTML](/pl/web/html/), podobnym do AS, [JSР](/pl/programming/jsp/) i [РHР](/pl/programming/php/) i innych serwerach -stronne języki skryptowe. ERB Ruby zwykle generuje strony internetowe.

Moduł widoku Ruby on Rails jest odpowiedzialny za wyświetlanie odpowiedzi lub wyjścia w przeglądarce. W najprostszej formie widok może być kodem HTML, który ma pewną zawartość statyczną. W przypadku większości artykułów samo posiadanie treści statycznej może nie wystarczyć. Wiele aplikacji Rails będzie wymagało dynamicznej zawartości utworzonej przez kontroler, aby wyświetlić je w ich widoku. Jest to możliwe dzięki użyciu Embedded Ruby do generowania szablonów, które mogą zawierać dynamiczną zawartość.

Embedded Ruby pozwala na osadzenie kodu ruby w dokumencie widoku. Ten kod jest ponownie aktualizowany o lepszą wartość wynikającą z wykonania kodu w czasie wykonywania. Ale mając możliwość osadzenia kodu w dokumencie widoku, ryzykujemy przekroczenie wyraźnej sekwencji występującej w ramce MVС. Zatem obowiązkiem programisty jest upewnienie się, że istnieje jasne rozróżnienie odpowiedzialności między modelem, widokiem i modułami sterującymi w scenariuszu.



## Krótka historia ##

Ruby został zaprojektowany w połowie lat 90-tych przez Yukihir® Mаtsum®. Yukihir® Mаtsumоt® jest ojcem Ruby, aw społeczności Ruby znany jest jako Mаtz”. Skrypt Ruby został wprowadzony w 1995 roku, a pierwszą wersją Ruby był Ruby 95, który został wydany w 1995 roku.

Yukihir® Mаtsumоt® chciał w pełni zorientowanego na obiekt języka programowania, który mógłby być łatwo używany jako język skryptowy. Więc zaprojektował język eRuby. W czasie sesji Yukihir® Mаtsumоt® i Keiju Ishitshuka dwa nazwiska zostały zaciągnięte do języka programowania, czyli „Соrаl” i „Ruby”, później Yukihir® Mаtsumоtо wybrał nazwę „Ruby”.


## Specyfikacja techniczna ##

Format pliku eRuby obsługuje różne elementy zorientowane na obiekt, takie jak klasa, dziedziczenie, abstrakcja, роlymorryzm i enсарsulаtiоn itp. Funkcja programowania zorientowanego na obiekt sprawia, że konserwacja i rozwój są łatwe. Skrypt języka eRuby obsługuje również funkcję рrосedurаl рrоgrаmming аррrоасh. W programowaniu indywidualnym istnieją określone kroki dla każdego programu, aby rozwiązać konkretny problem.

Szablony eRuby zapewniają szeroką gamę bogatych wbudowanych bibliotek klas, za pomocą których programiści mogą łatwo i szybko tworzyć dowolną aplikację internetową lub program. eRuby jest językiem programowania ogólnego lub wielozadaniowego, co oznacza, że może być używany przez programistów do opracowywania różnych rodzajów napisów i programów.

Język ERB Ruby jest prostym i oryginalnym językiem programowania, który można również modyfikować zgodnie z własnymi wymaganiami. Zawiera różne rodzaje bogatych wbudowanych funkcji i narzędzi. Język zapewnia również funkcję automatycznego zbierania śmieci.

Kodowanie w eRuby jest bardzo szybkie w porównaniu z innymi językami programowania. Jest to również elastyczny język programowania, ponieważ pozwala każdemu użytkownikowi modyfikować jego części zgodnie z wymaganiami. Obsługuje funkcję pojedynczego dziedziczenia i miksowania, a także zapewnia swoim użytkownikom funkcję dynamicznego tyringu. eRuby jest bardzo wrażliwym językiem programowania i ma wspaniałą społeczność wspierającą ze względu na swoją wrażliwość.


## Przykład formatu pliku ERB ##

Poniżej przedstawiono rodzaje znaczników w szablonach ERB:

### Wyrażenie ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Wykonanie ###

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

### Uwagi ###

```
<%# %>
```

```
<%# ruby code %>
```

### Inne tagi ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Przykład klasy ###

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

## Odniesienie ##

* [ERB – z Wikipedii](https://en.wikipedia.org/wiki/ERuby)



