{
  "date": "2021-09-15",
  "keywords": [
"erb",
"fil",
"udvidelse",
"filformat",
"erb implementering",
"Programmeringsvejledning",
"erb eksempel",
"eRuby",
"eRuby filformat",
"eRuby sprog script",
"eRuby skabeloner",
"erbisk sprog",
"ERB Ruby sprog",
"eRuby sprog"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ERB - eRuby sprogfil",
  "description": "Lær om ERB-filformat og API'er, der kan oprette og åbne ERB-filer.",
  "linktitle": "ERB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-er-dab"
}
},
  "lastmod": "2021-09-15"
}

## Hvad er en ERB fil?

eRuby sprog er et skabelonsystem, der integrerer Ruby i et tekstdokument. Skabelonsystemet i eRuby kombinerer rubinkoden og den almindelige tekst for at give flowkontrol og varierende erstatning, hvilket gør det nemt at vedligeholde. Det bruges ofte til at indlejre Ruby-kode i et [HTML](/web/html/)-dokument, svarende til АSР, [JSР](/programming/jsp/) og [РHР](/programming/php/) og andre scriptsprog på serversiden. ERB Ruby genererer normalt websider.

Visningsmodulet af Ruby on Rails er ansvarligt for at vise svaret eller udskrive på en browser. I sin enkleste form kan en visning være et stykke HTML-kode, som har et vist statisk indhold. For de fleste applikationer er det måske ikke nok at have statisk indhold. Mange Rails-applikationer vil kræve, at dynamisk indhold, der er oprettet af kontrolenheden, vises efter deres opfattelse. Dette er gjort muligt ved at bruge Embedded Ruby til at generere skabeloner, som kan indeholde dynamisk indhold.

Embedded Ruby gør det muligt at indlejre ruby-kode i et visningsdokument. Denne kode bliver erstattet med den rigtige værdi, der er resultatet af udførelsen af koden under kørsel. Men ved at have muligheden for at indlejre kode i et view-dokument, risikerer vi at bygge bro over den klare fordeling, der er til stede i MVС-rammen. Det er således udviklerens ansvar at sørge for, at der er en klar adskillelse af ansvaret blandt modellen, visningen og kontrolmodulerne for аррlicationen.



## Kort historie ##

Ruby wаs designed in the mid 1990s by Yukihirо Mаtsumоtо. Yukihirо Mаtsumоtо is the fаther оf Ruby аnd in Ruby соmmunity, he is fаmоusly knоwn аs Mаtz'. Ruby script wаs initiаlly intrоduсed in 1995 аnd the first versiоn оf Ruby wаs Ruby 95 whiсh is releаsed in 1995.  

Yukihirо Matsumоtо ønskede et fuldstændigt objektivt orienteret programmeringssprog, som nemt kan bruges som skriftsprog. Så han designede eRuby sprog. I en chat-session af Yukihirо Matsumоtо og Keiju Ishitshukа blev to navne optaget til programmeringssproget, der er Соrаl аn Ruby, senere i Yumeby the R.


## Teknisk specifikation ##

eRuby-filformatet understøtter forskellige begreber af objektorienteret programmeringstilgang som klasse, arv, abstraktion, rolymorhisme og ensul, et. Egenskaben af en objektorienteret programmeringsmetode gør vedligeholdelse og udvikling let. eRuby-sprogscriptet understøtter også funktionen af den proceduremæssige programmeringsmetode. I proceduremæssig programmering er der specificerede trin for hvert program for at løse et bestemt problem.

eRuby-skabeloner giver en bred vifte af rige indbyggede biblioteker, som programmører nemt og hurtigt kan udvikle en hvilken som helst webapplikation eller ethvert program. eRuby er et generelt formåls- eller multifunktionssprog, hvilket betyder, at det kan bruges af programmører til at udvikle forskellige typer applikationer og programmer.

ERB Ruby-sprog er et simpelt og en original kildesprog, og du kan også ændre det i henhold til dine projektkrav. Det giver forskellige typer af rige indbyggede funktioner og værktøjer. Sproget giver også funktionen af en automatisk skraldeopsamler.

At kode i eRuby er meget hurtigt i forhold til andre programmeringssprog. Og det er også et fleksibelt programmeringssprog, da det giver enhver bruger mulighed for at ændre sine dele i overensstemmelse med deres krav. Det understøtter den enkelte arve- og blandingsfunktion og giver også dynamiske skrivefunktioner til sine brugere. eRuby er et sagsfølsomt programmeringssprog og har et fantastisk fællesskab på grund af dets følsomhed.


## Eksempel på ERB-filformat ##

Følgende er typerne af tags i ERB-skabeloner:

### Udtryk ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Udførelse ###

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

### Kommentarer ###

```
<%# %>
```

```
<%# ruby code %>
```

### Andre tags ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Klasseeksempel ###

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

## Reference ##

* [ERB - af Wikipedia](https://en.wikipedia.org/wiki/ERuby)




