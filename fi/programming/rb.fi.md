{
  "date": "2023-05-29",
  "keywords": [
"rb-tiedosto",
"mikä on rb-tiedosto",
"kuinka suorittaa ruby-skripti rb-tiedostossa",
"mitä rb-tiedosto sisältää",
"mikä on rb-tiedoston muoto",
"tiedosto",
"rb tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "RB-tiedostomuoto - Ruby-lähdekooditiedosto",
  "description": "Opi RB-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata RB-tiedostoja.",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb-fi",
      "parent": "programming"
}
},
  "lastmod": "2023-05-29"
}

## Mikä on RB-tiedosto?

.rb-tiedostopääte liittyy yleensä Ruby-ohjelmointikielitiedostoihin. Ruby on dynaaminen, olio-ohjelmointikieli, joka tunnetaan yksinkertaisuudestaan ja luettavuudestaan.

.rb-tiedosto sisältää Ruby-lähdekoodin, jonka voi suorittaa Ruby-tulkki tai Ruby-kehitysympäristö. Nämä tiedostot sisältävät usein määritelmiä luokista, menetelmistä, muuttujista ja muista Ruby-koodirakenteista.

## Kuinka suorittaa Ruby-skripti RB-tiedostossa?

Jotta voit suorittaa .rb-tiedostoon tallennetun Ruby-komentosarjan, järjestelmääsi on asennettu Ruby-tulkki. Tässä on perusesimerkki Ruby-skriptistä, joka on tallennettu tiedostoon example.rb:

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

Voit suorittaa tämän skriptin avaamalla komentorivin tai terminaalin, siirtymällä hakemistoon, jossa example.rb-tiedosto sijaitsee, ja käyttämällä sitten Ruby-tulkkia:

```
ruby example.rb
```

Yllä olevan komennon suorittaminen suorittaa skriptin ja tulos näytetään konsolissa:

```
The square of 5 is: 25
```

Tämä on yksinkertainen esimerkki, mutta .rb-tiedostot voivat sisältää monimutkaisempaa koodia, mukaan lukien luokkia, moduuleja ja ohjausrakenteita, jolloin voit rakentaa täysimittaisia Ruby-sovelluksia.

## Mitä RB-tiedosto sisältää?

.rb-tiedoston sisältö voi vaihdella sen tarkoituksen ja sen kirjoittaneen ohjelmoijan mukaan. Yleensä .rb-tiedosto sisältää kuitenkin Ruby-lähdekoodin, joka koostuu käskysarjoista, joita Ruby-tulkki voi ymmärtää ja suorittaa.

Tässä on joitain yleisiä elementtejä, joita saatat löytää Ruby-tiedostosta:

- **Kommentit:** Ruby tukee sekä yksirivisiä että monirivisiä kommentteja. Kommentteja käytetään lisäämään selittäviä huomautuksia tai estämään tiettyjen koodirivien suorittaminen. Ne on merkitty #-merkillä.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

- **Muuttujamääritykset:** Ruby on dynaamisesti kirjoitettu kieli, joten muuttujat eivät tarvitse nimenomaisia tyyppimäärityksiä. Voit määrittää muuttujille arvoja määritysoperaattorilla (=).

- **Menetelmät:** Ruby käyttää def-avainsanaa menetelmien määrittämiseen, jotka ovat uudelleenkäytettäviä koodilohkoja, jotka suorittavat tiettyjä tehtäviä.

- **Luokat ja objektit:** Ruby on oliokieli, ja luokkia käytetään objektisuunnitelmien määrittämiseen. Objektit ovat luokkien ilmentymiä, ja niillä voi olla attribuutteja (instanssimuuttujia) ja käyttäytymistä (instanssimenetelmät).

- **Ohjausrakenteet:** Ruby tarjoaa erilaisia ohjausrakenteita, kuten ehdollisia lausekkeita (if, else, elsif, ellei), silmukoita (while, till, for, kukin) ja paljon muuta ohjaamaan ohjelman suorituskulkua.

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## Mikä on RB-tiedoston muoto?

.rb-tiedoston muoto on pelkkää tekstiä, joka on tyypillisesti koodattu UTF-8- tai ASCII-koodauksella. Se noudattaa Ruby-ohjelmointikielen määrittelemää tiettyä syntaksia ja rakennetta.

## Mikä on RB-tiedoston MIME-tyyppi?

- sovellus/x-ruby.

## Viitteet
* [Ruby (ohjelmointikieli)](https://en.wikipedia.org/wiki/Ruby_(ohjelmointikieli))


