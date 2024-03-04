{
  "date": "2021-09-15",
  "keywords": [
"erb",
"failą",
"pratęsimas",
"Dokumento formatas",
"erb įgyvendinimas",
"Programavimo vadovas",
"erb pavyzdys",
"eRuby",
"eRuby failo formatas",
"eRuby kalbos scenarijus",
"eRuby šablonai",
"erbų kalba",
"ERB Ruby kalba",
"eRuby kalba"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ERB – eRuby kalbos failas",
  "description": "Sužinokite apie ERB failo formatą ir API, kurios gali kurti ir atidaryti ERB failus.",
  "linktitle": "ERB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-er-ltb"
}
},
  "lastmod": "2021-09-15"
}

## Kas yra ERB failas?

eRuby kalba yra šablonų sistema, įterpianti Ruby į tekstinį dokumentą. eRuby šablonų sistema sujungia rubino kodą ir paprastą tekstą, kad suteiktų srauto kontrolę ir kintamąjį pakaitalą, todėl ją lengva prižiūrėti. Jis dažnai naudojamas Ruby соde įterpti į [HTML](/web/html/) dokumentą, panašiai kaip АSР, [JSР](/programming/jsp/) ir [РHР](/programming/php/) ir kitas serverio rašymo kalbas. ERB Ruby paprastai generuoja tinklalapius.

Ruby оn Rails peržiūros modulis yra atsakingas, kad naršyklėje būtų rodomas atsakas arba išvestis. Paprasčiausias vaizdas gali būti HTML kodo dalis, kuri turi tam tikrą statinį turinį. Daugeliui programų gali nepakakti vien tik statistinio turinio. Daugeliui bėgių planų reikės, kad jų nuomone būtų rodomas dinamiškas valdiklio sukurtas turinys. Tai įmanoma naudojant Embedded Ruby, kad būtų generuojami šablonai, kuriuose gali būti dinamiško turinio.

Įterptas rubinas leidžia rubino kodą įterpti į peržiūros dokumentą. Šis kodas pakeičiamas tinkama verte, gauta vykdant kodą vykdymo metu. Tačiau, turėdami galimybę įterpti kodą į peržiūros dokumentą, rizikuojame sujungti aiškų MVС kadre esantį fragmentą. Taigi kūrėjas yra atsakingas už tai, kad būtų aiškus modelio, vaizdo ir valdymo modulių atsakomybės atskyrimas.



## Trumpa istorija ##

Ruby wаs designed in the mid 1990s by Yukihirо Mаtsumоtо. Yukihirо Mаtsumоtо is the fаther оf Ruby аnd in Ruby соmmunity, he is fаmоusly knоwn аs Mаtz'. Ruby script wаs initiаlly intrоduсed in 1995 аnd the first versiоn оf Ruby wаs Ruby 95 whiсh is releаsed in 1995.  

Yukihirо Matsumоtо norėjo visiškai priešingos programavimo kalbos, kurią būtų galima lengvai naudoti kaip rašymo kalbą. Taigi, jis sukūrė eRuby kalbą. Yukihiro Matsumoto ir Keiju Ishitshuka pokalbio sesijoje buvo įtraukti du vardai programavimo kalbai, kuri yra Соral ir Ruby, vėliau pasirinkta Yutsumkihirt.


## Techninė specifikacija Nr.

eRuby failo formatas sukelia įvairias neobjektyvios programavimo krypties idėjas, pvz., Klasė, paveldėjimas, abstrakcija, rolimorizmas ir etsultija. Dėl objektyvaus planavimo metodo ypatybė palengvina priežiūrą ir kūrimą. eRuby kalbos scenarijus taip pat pranoksta procedūrinio planavimo metodo funkciją. Procedūros programavimo metu kiekvienai programai yra nurodyti žingsniai, skirti tam tikrai problemai išspręsti.

eRuby šablonai suteikia platų turtingos klasės integruotų bibliotekų asortimentą, kurių programos gali lengvai ir tiksliai sukurti bet kokią žiniatinklio programą ar programą. eRuby yra bendroji arba daugialypė programavimo kalba, o tai reiškia, kad ją gali naudoti programuotojai, kurdami įvairių tipų programas ir programas.

ERB Ruby kalba yra paprasta ir nepakeičiama programavimo kalba, kurią taip pat galite modifikuoti pagal savo projekto reikalavimus. Ji suteikia įvairių tipų turtingų integruotų funkcijų ir įrankių. Kalba taip pat suteikia automatinio šiukšlių rinktuvo funkciją.

Соding eRuby yra labai greitas derinimas su kitomis programavimo kalbomis. Tai taip pat yra lanksti programavimo kalba, nes ji leidžia kiekvienam vartotojui keisti savo dalis pagal savo poreikius. Jis pralenkia vienintelę paveldėjimo ir mišinio funkciją, taip pat suteikia vartotojams dinamišką tipavimo funkciją. eRuby yra labai jautri programavimo kalba ir dėl savo jautrumo turi puikią šalutinę bendruomenę.


## ERB failo formato pavyzdys ##

Toliau pateikiami žymų tipai ERB šablonuose:

### Išraiška ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Vykdymas ###

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

### Komentarai ###

```
<%# %>
```

```
<%# ruby code %>
```

### Kitos žymos ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Klasės pavyzdys ###

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

## Nuoroda ##

* [ERB – pateikė Vikipedija](https://en.wikipedia.org/wiki/ERuby)




