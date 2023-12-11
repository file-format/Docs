{
"data": "2023-05-29",
  "keywords": [
"fișier rb",
"Ce este un fișier rb",
"cum se rulează scriptul ruby în fișierul rb",
"ce conține fișierul rb",
"care este formatul fișierului rb",
"fişier",
"extensie fișier rb",
"extensie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "fals",
"toc": true,
"title": "Format fișier RB - Fișier cod sursă Ruby",
  "description":"Aflați despre formatul RB și despre API-urile care pot crea și deschide fișiere RB.",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "identifier": "programming-rb",
      "parent": "programming"
}
},
"lastmod": "2023-05-29"
}

## Ce este un fișier RB?

O extensie de fișier ".rb" este de obicei asociată fișierelor în limbajul de programare Ruby. Ruby este un limbaj de programare dinamic, orientat pe obiecte, cunoscut pentru simplitatea și lizibilitatea sa.

Un fișier ".rb" conține cod sursă Ruby, care poate fi executat de un interpret Ruby sau de un mediu de dezvoltare Ruby. Aceste fișiere conțin adesea definiții ale claselor, metodelor, variabilelor și altor constructe de cod Ruby.

## Cum se rulează scriptul Ruby în fișierul RB?

Pentru a rula un script Ruby salvat în fișierul ".rb", veți avea nevoie de un interpret Ruby instalat pe sistemul dumneavoastră. Iată un exemplu de bază de script Ruby salvat în fișierul numit "example.rb":

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

Pentru a rula acest script, puteți deschide linia de comandă sau terminalul, navigați la directorul în care se află fișierul "example.rb" și apoi utilizați interpretul Ruby:

```
ruby example.rb
```

Executarea comenzii de mai sus va rula scriptul și rezultatul va fi afișat în consolă:

```
The square of 5 is: 25
```

Acesta este un exemplu simplu, dar fișierele ".rb" pot conține cod mai complex, inclusiv clase, module și structuri de control, permițându-vă să construiți aplicații Ruby cu drepturi depline.

## Ce conține fișierul RB?

Conținutul specific al fișierului ".rb" poate varia în funcție de scopul acestuia și de programatorul care l-a scris. Cu toate acestea, în general, fișierul ".rb" conține cod sursă Ruby, care constă dintr-o serie de instrucțiuni pe care interpretul Ruby le poate înțelege și executa.

Iată câteva elemente comune pe care le puteți găsi în fișierul Ruby:

- **Comentarii:** Ruby acceptă atât comentarii cu o singură linie, cât și comentarii pe mai multe rânduri. Comentariile sunt folosite pentru a adăuga note explicative sau pentru a dezactiva anumite linii de cod din execuție. Sunt notate cu caracterul #.

```
# This is a single-line comment

=begin
This is a
multi-line comment
=end
```

- **Declarații de variabile:** Ruby este un limbaj tatat dinamic, astfel încât variabilele nu au nevoie de declarații de tip explicite. Puteți atribui valori variabilelor folosind operatorul de atribuire (=).

- **Metode:** Ruby folosește cuvântul cheie `def` pentru a defini metode, care sunt blocuri de cod reutilizabile care efectuează sarcini specifice.

- **Clasuri și obiecte:** Ruby este un limbaj orientat pe obiecte, iar clasele sunt folosite pentru a defini modelele obiectelor. Obiectele sunt instanțe de clase și pot avea atribute (variabile de instanță) și comportamente (metode de instanță).

- **Structuri de control:** Ruby oferă diverse structuri de control, cum ar fi instrucțiuni condiționale (if, else, elsif, unless), bucle (while, until, for, each) și multe altele, pentru a controla fluxul de execuție în program.

```
if age >= 18
  puts "You are an adult."
else
  puts "You are a minor."
end

# Output: You are an adult.
```

## Care este formatul fișierului RB?

Formatul fișierului ".rb" este text simplu, de obicei codificat utilizând codificarea UTF-8 sau ASCII. Urmează o sintaxă și o structură specifice definite de limbajul de programare Ruby.

## Care este tipul MIME al fișierului RB?

- `application/x-ruby`

## Referințe
* [Ruby (limbaj de programare)](https://en.wikipedia.org/wiki/Ruby_(limbaj_de_programare))

