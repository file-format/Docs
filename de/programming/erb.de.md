{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "Datei", "Erweiterung", "Dateiformat", "erb-Implementierung", "Programmierhandbuch", "erb-Beispiel", "eRuby", "eRuby-Dateiformat", "eRuby-Sprachskript", " eRuby-Vorlagen", "erb-Sprache", "ERB-Ruby-Sprache", "eRuby-Sprache" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - eRuby-Sprachdatei",
  "description":"Erfahren Sie mehr über das ERB-Dateiformat und APIs, die ERB-Dateien erstellen und öffnen können.",
  "linktitle" :"ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Was ist eine ERB-Datei?

Die eRuby-Sprache ist ein Vorlagensystem, das Ruby in ein Textdokument einbettet. Das Templating-System von eRuby kombiniert den Ruby-Code und den einfachen Text, um eine Flusskontrolle und einen variablen Ersatz bereitzustellen, wodurch es einfach zu warten ist. Es wird oft verwendet, um Ruby-Code in ein [HTML](/de/web/html/)-Dokument einzubetten, ähnlich wie ASSR, [JSR](/de/programming/jsp/) und [CHSR](/de/programming/php/) und andere Server -seitige Skriptsprachen. ERB Ruby generiert normalerweise Webseiten.

Das Ansichtsmodul von Ruby on Rails ist dafür verantwortlich, die Antwort oder Ausgabe auf einem Browser anzuzeigen. In seiner einfachsten Form kann eine Ansicht ein Stück HTML-Code sein, der einen statischen Inhalt hat. Für die meisten Anwendungen reicht es möglicherweise nicht aus, nur statische Inhalte zu haben. Viele Rails-Anwendungen erfordern dynamische Inhalte, die vom Controller erstellt wurden, um in ihrer Ansicht angezeigt zu werden. Dies wird durch die Verwendung von Embedded Ruby zum Generieren von Vorlagen ermöglicht, die dynamische Inhalte enthalten können.

Eingebettetes Ruby ermöglicht das Einbetten von Ruby-Code in ein Ansichtsdokument. Dieser Code wird durch den richtigen Wert ersetzt, der sich aus der Ausführung des Codes zur Laufzeit ergibt. Durch die Möglichkeit, Code in ein Ansichtsdokument einzubetten, riskieren wir jedoch, die im MVС-Rahmen vorhandene klare Trennung zu überbrücken. Es liegt daher in der Verantwortung des Entwicklers sicherzustellen, dass es eine klare Trennung der Verantwortlichkeiten zwischen den Modell-, Ansichts- und Steuerungsmodulen der Anwendung gibt.



## Kurze Geschichte ##

Ruby wurde Mitte der 1990er Jahre von Yukihir® Mаtsumоt® entworfen. Yukihirо Matsumоtо ist der Vater von Ruby und in der Ruby-Gemeinschaft ist er als Matz bekannt. Das Ruby-Skript wurde ursprünglich 1995 eingeführt und die erste Version von Ruby war Ruby 95, die 1995 veröffentlicht wurde.

Yukihirо Matsumоtо wollte eine vollständig objektorientierte Programmiersprache, die einfach als Skriptsprache verwendet werden kann. Also entwarf er die eRuby-Sprache. In einer gemeinsamen Sitzung von Yukihirо Mаtsumоtо und Keiju Ishitshukа wurden zwei Namen für die Programmiersprache eingetragen, nämlich "Сorаl" und "Ruby", später wählte Yukihirо Mаtsumоto den Namen "Ruby".


## Technische Spezifikation ##

Das eRuby-Dateiformat unterstützt verschiedene Konzepte objektorientierter Programmieransätze wie Klasse, Vererbung, Abstraktion, Polymerisierung und Kapselung usw. Die Eigenschaft des objektorientierten Programmieransatzes macht Wartung und Entwicklung einfach. Das eRuby-Sprachskript unterstützt auch die Funktion des prozeduralen Programmieransatzes. Bei der prozeduralen Programmierung gibt es für jedes Programm festgelegte Schritte, um ein bestimmtes Problem zu lösen.

eRuby-Vorlagen bieten eine große Auswahl an umfangreichen integrierten Bibliotheken, mit denen Programmierer jede beliebige Webanwendung oder jedes beliebige Programm einfach und schnell entwickeln können. eRuby ist eine allgemeine oder Mehrzweck-Programmiersprache, was bedeutet, dass sie von Programmierern bei der Entwicklung verschiedener Arten von Anwendungen und Programmen verwendet werden kann.

Die ERB Ruby-Sprache ist eine einfache und offene Programmiersprache und Sie können sie auch entsprechend Ihren Projektanforderungen modifizieren. Es bietet verschiedene Arten von reichhaltigen integrierten Funktionen und Tools. Die Sprache bietet auch die Funktion eines automatischen Müllsammlers.

Die Programmierung in eRuby ist im Vergleich zu anderen Programmiersprachen sehr schnell. Und es ist auch eine flexible Programmiersprache, da es jedem Benutzer erlaubt, seine Teile entsprechend seinen Anforderungen zu modifizieren. Es unterstützt die Einzelvererbung und Mixins-Funktion und bietet seinen Benutzern auch eine dynamische Typisierungsfunktion. eRuby ist eine fallsensitive Programmiersprache und hat aufgrund ihrer Sensibilität eine große unterstützende Community.


## Beispiel für ein ERB-Dateiformat ##

Im Folgenden sind die Arten von Tags in ERB-Vorlagen aufgeführt:

### Ausdruck ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Ausführung ###

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

### Kommentare ###

```
<%# %>
```

```
<%# ruby code %>
```

### Andere Tags ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Klassenbeispiel ###

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

## Bezug ##

* [ERB - von Wikipedia](https://en.wikipedia.org/wiki/ERuby)



