{
  "date": "2023-05-29",
  "keywords": [
"rb failą",
"kas yra rb failas",
"kaip paleisti ruby scenarijų rb faile",
"kas yra rb faile",
"koks yra rb failo formatas",
"failą",
"rb failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "RB failo formatas – „Ruby“ šaltinio kodo failas",
  "description": "Sužinokite apie RB formatą ir API, kurios gali kurti ir atidaryti RB failus.",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb-lt",
      "parent": "programming"
}
},
  "lastmod": "2023-05-29"
}

## Kas yra RB failas?

.rb failo plėtinys paprastai siejamas su Ruby programavimo kalbos failais. Ruby yra dinamiška, į objektą orientuota programavimo kalba, žinoma dėl savo paprastumo ir skaitomumo.

.rb faile yra Ruby šaltinio kodas, kurį gali vykdyti Ruby vertėjas arba Ruby kūrimo aplinka. Šiuose failuose dažnai yra klasių, metodų, kintamųjų ir kitų Ruby kodo konstrukcijų apibrėžimų.

## Kaip paleisti Ruby scenarijų RB faile?

Norėdami paleisti .rb faile išsaugotą Ruby scenarijų, jūsų sistemoje reikės įdiegti Ruby interpretatorių. Štai pagrindinis Ruby scenarijaus, išsaugoto faile pavadinimu example.rb, pavyzdys:

```
# example.rb

# Define a method to calculate the square of a number
def square(number)
  number * number
end

# Call the square method with an argument
result = square(5)

# Print the result
puts "The square of 5 is: #{result}"
```

Norėdami paleisti šį scenarijų, galite atidaryti komandų eilutę arba terminalą, pereiti į katalogą, kuriame yra failas example.rb, ir naudoti Ruby interpretatorių:

```
ruby example.rb
```

Vykdant aukščiau esančią komandą bus paleistas scenarijus, o išvestis bus rodoma konsolėje:

```
The square of 5 is: 25
```

Tai paprastas pavyzdys, tačiau .rb failuose gali būti sudėtingesnis kodas, įskaitant klases, modulius ir valdymo struktūras, leidžiančias kurti visavertes Ruby programas.

## Kas yra RB faile?

Konkretus .rb failo turinys gali skirtis priklausomai nuo jo paskirties ir jį parašiusio programuotojo. Tačiau apskritai .rb faile yra Ruby šaltinio kodas, kurį sudaro instrukcijų serijos, kurias Ruby interpretatorius gali suprasti ir vykdyti.

Štai keletas bendrų elementų, kuriuos galite rasti Ruby faile:

– **Komentarai:** Ruby palaiko ir vienos, ir kelių eilučių komentarus. Komentarai naudojami norint pridėti aiškinamąsias pastabas arba išjungti konkrečias kodo eilutes. Jie žymimi # simboliu.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

– **Kintamųjų deklaracijos:** Ruby yra dinamiškai įvedama kalba, todėl kintamiesiems nereikia aiškių tipo deklaracijų. Vertes kintamiesiems galite priskirti naudodami priskyrimo operatorių (=).

– **Metodai:** Ruby naudoja raktinį žodį def, kad apibrėžtų metodus, kurie yra daugkartinio naudojimo kodo blokai, atliekantys konkrečias užduotis.

- **Klasės ir objektai:** Ruby yra į objektus orientuota kalba, o klasės naudojamos objektų brėžiniams apibrėžti. Objektai yra klasių egzemplioriai ir gali turėti atributus (pavyzdžių kintamuosius) ir elgseną (pavyzdžių metodai).

- **Valdymo struktūros:** Ruby teikia įvairias valdymo struktūras, pvz., sąlyginius sakinius (jei, else, elsif, nebent), kilpas (while, till, for, kiekvienas) ir daugiau, kad būtų galima valdyti programos vykdymo srautą.

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## Koks yra RB failo formatas?

.rb failo formatas yra paprastas tekstas, paprastai užkoduotas naudojant UTF-8 arba ASCII kodavimą. Ji atitinka specifinę sintaksę ir struktūrą, apibrėžtą Ruby programavimo kalbos.

## Koks yra RB failo MIME tipas?

- Application/x-ruby.

## Nuorodos
* [Ruby (programavimo kalba)](https://en.wikipedia.org/wiki/Ruby_(programming_language))


