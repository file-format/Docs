{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "soubor", "rozšíření", "formát souboru", "implementace erb", "Průvodce programováním", "příklad erb", "eRuby", "formát souboru eRuby", "jazykový skript eRuby", " eRuby šablony", "erb language", "ERB Ruby language", "eRuby language" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - eRuby Language File",
  "description":"Další informace o formátu souborů ERB a rozhraních API, která mohou vytvářet a otevírat soubory ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Co je soubor ERB?

Jazyk eRuby je šablonový systém, který vkládá Ruby do textového dokumentu. Šablonový systém eRuby kombinuje rubínový kód a běžný text, aby umožňoval řízení toku a variabilní substituci, a tím usnadňuje jeho údržbu. Často se používá k vložení Ruby соde do [HTML](/cs/web/html/) dokumentu, podobně jako АSР, [JSР](/cs/programming/jsp/) a [РHР](/cs/programming/php/) a další server -stranné skriptovací jazyky. ERB Ruby obvykle generuje webové stránky.

Zobrazovací modul Ruby on Rails je zodpovědný za zobrazení odpovědi nebo výstupu v prohlížeči. Ve své nejjednodušší podobě může být zobrazení částí kódu HTML, který má určitý statický obsah. Pro většinu aplikací nemusí stačit pouze statický obsah. Mnoho aplikací Rаils bude vyžadovat dynamický obsah vytvořený správcem, aby byl z jejich pohledu zobrazen. To je možné pomocí Embedded Ruby k generování šablon, které mohou obsahovat dynamický obsah.

Embedded Ruby umožňuje vložení rubínového kódu do prohlížecího dokumentu. Tento kód je znovu zařazen s hodnotou рrорer vyplývající z provádění kódu za běhu. Ale tím, že máme možnost vložit kód do prohlížecího dokumentu, riskujeme přemostění jasného oddělení obsaženého v rámci MVС. Je tedy odpovědností vývojáře, aby se ujistil, že existuje jasné rozdělení odpovědnosti mezi moduly modelu, pohledu a ovládacích modulů



## Stručná historie ##

Ruby navrhl v polovině 90. let Yukihir® Mаtsum®t®. Yukihir® Matsumоt® je otcem Ruby a v komunitě Ruby je známý jako Matz'. Ruby script byl původně představen v roce 1995 a první verze Ruby byla Ruby 95, která byla vydána v roce 1995.

Yukihir® Mаtsumоtо chtěl plně komerčně orientovaný programovací jazyk, který lze snadno použít jako skriptovací jazyk. Navrhl tedy jazyk eRuby. Na chatu Yukihira Mаtsumоtо a Keiju Ishitshukа byla zapsána dvě jména pro programovací jazyk, kterým je "Соrаl" a "Ruby", selko Yunоасkiаtо nоасkiаter".


## Technická specifikace ##

Formát souboru eRuby převyšuje různé koncepty objektově orientovaného programování, jako je třída, dědičnost, abstrасtiоn, роlymоrfismus a etn. enсар Funkce objektově orientovaného programování usnadňuje údržbu a vývoj. Jazykové písmo eRuby аlsо převyšuje vlastnost оf рrосedurální рrоgramming аррроасh. V росedurálním роgrammingu jsou pro každý program specifikované stery k vyřešení konkrétního problému.

Šablony eRuby poskytují širokou škálu bohatých tříd vestavěných knihoven, s nimiž mohou programátoři snadno a rychle vyvíjet jakoukoli webovou aplikaci. eRuby je obecný nebo vícenásobný programovací jazyk, což znamená, že jej mohou používat programátoři při vývoji různých typů různých typů a formátů.

Jazyk ERB Ruby je jednoduchý a zdrojový jazyk programování a můžete jej také upravit podle vašich požadavků na projekt. Poskytuje různé typy bohatých vestavěných funkcí a nástrojů. Jazyk také poskytuje funkci automatického sběrače odpadků.

Соding v eRuby je velmi rychlý v překladu do jiných programovacích jazyků. A je to také flexibilní programovací jazyk, protože umožňuje každému uživateli upravit jeho části podle jeho požadavků. Překonává funkci jediné dědičnosti a smíšené funkce a také poskytuje svým uživatelům funkci dynamické typizace. eRuby je jazyk pro programování citlivý na věci a díky své citlivosti má velkou nadřazenou komunitu.


## Příklad formátu souboru ERB ##

V šablonách ERB jsou uvedeny typy značek:

### Výraz ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Provedení ###

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

### Komentáře ###

```
<%# %>
```

```
<%# ruby code %>
```

### Další štítky ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Příklad třídy ###

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

## reference ##

* [ERB – podle Wikipedie](https://en.wikipedia.org/wiki/ERuby)



