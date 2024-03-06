{
  "date": "2023-05-29",
  "keywords": [
"rb fails",
"kas ir rb fails",
"kā palaist ruby skriptu rb failā",
"ko satur rb fails",
"kāds ir rb faila formāts",
"failu",
"rb faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "RB faila formāts — rubīna avota koda fails",
  "description": "Uzziniet par RB formātu un API, kas var izveidot un atvērt RB failus.",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb-lv",
      "parent": "programming"
}
},
  "lastmod": "2023-05-29"
}

## Kas ir RB fails?

Faila paplašinājums .rb parasti ir saistīts ar Ruby programmēšanas valodas failiem. Rubīns ir dinamiska, uz objektu orientēta programmēšanas valoda, kas pazīstama ar savu vienkāršību un lasāmību.

.rb fails satur Ruby pirmkodu, ko var izpildīt Ruby tulks vai Ruby izstrādes vide. Šie faili bieži satur klašu, metožu, mainīgo un citu Ruby koda konstrukciju definīcijas.

## Kā palaist Ruby skriptu RB failā?

Lai palaistu Ruby skriptu, kas saglabāts failā .rb, jūsu sistēmā būs jāinstalē Ruby tulks. Šeit ir pamata piemērs Ruby skriptam, kas saglabāts failā ar nosaukumu example.rb.

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

Lai palaistu šo skriptu, varat atvērt komandrindu vai termināli, pāriet uz direktoriju, kurā atrodas fails example.rb, un pēc tam izmantot Ruby interpreter:

```
ruby example.rb
```

Izpildot iepriekš minēto komandu, tiks palaists skripts, un konsolē tiks parādīta izvade:

```
The square of 5 is: 25
```

Šis ir vienkāršs piemērs, taču .rb faili var saturēt sarežģītāku kodu, tostarp klases, moduļus un vadības struktūras, kas ļauj jums izveidot pilnvērtīgas Ruby lietojumprogrammas.

## Ko satur RB fails?

Konkrētais .rb faila saturs var atšķirties atkarībā no tā mērķa un programmētāja, kurš to uzrakstījis. Tomēr kopumā .rb fails satur Ruby pirmkodu, kas sastāv no instrukciju sērijas, kuras Ruby tulks var saprast un izpildīt.

Šeit ir daži izplatīti elementi, ko varat atrast Ruby failā:

- **Komentāri:** Ruby atbalsta gan vienas rindiņas, gan vairāku rindiņu komentārus. Komentāri tiek izmantoti, lai pievienotu paskaidrojošas piezīmes vai atspējotu konkrētu koda rindu izpildi. Tie ir apzīmēti ar # rakstzīmi.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

- **Mainīgo deklarācijas:** Ruby ir dinamiski drukāta valoda, tāpēc mainīgajiem nav nepieciešamas precīzas tipa deklarācijas. Varat piešķirt vērtības mainīgajiem, izmantojot piešķiršanas operatoru (=).

- **Metodes:** Ruby izmanto atslēgvārdu def, lai definētu metodes, kas ir atkārtoti lietojami koda bloki, kas veic konkrētus uzdevumus.

- **Klases un objekti:** Rubīns ir uz objektu orientēta valoda, un klases tiek izmantotas, lai definētu objektu projektus. Objekti ir klašu gadījumi, un tiem var būt atribūti (instanču mainīgie) un uzvedība (instanču metodes).

- **Vadības struktūras:** Ruby nodrošina dažādas vadības struktūras, piemēram, nosacījumu priekšrakstus (ja, else, elsif, ja vien), cilpas (while, till, for, every) un citas, lai kontrolētu izpildes plūsmu programmā.

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## Kāds ir RB faila formāts?

.rb faila formāts ir vienkāršs teksts, kas parasti tiek kodēts, izmantojot UTF-8 vai ASCII kodējumu. Tas seko noteiktai sintaksei un struktūrai, ko nosaka Ruby programmēšanas valoda.

## Kāds ir RB faila MIME tips?

- Application/x-ruby.

## Atsauces
* [Ruby (programmēšanas valoda)](https://en.wikipedia.org/wiki/Ruby_(programming_language))


