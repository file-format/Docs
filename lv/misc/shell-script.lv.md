{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell skripts — kā to palaist Ubuntu un Linux",
  "description":"Uzziniet, kas ir Shell Script un kā to palaist Ubuntu un Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-lv",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Kas ir Shell skripts?

Shell skriptēšana ietver komandu sērijas rakstīšanu vienkārša teksta failā, ko bieži dēvē par **Shell skriptu**. Šos skriptus izpilda apvalks, kas ir komandrindas tulks. Visizplatītākie apvalki ietver

1. Bašs (Bourne Again SHell)
2. Zsh (Z Shell)
3. Zivis.

Apvalka skripti var būt no vienkāršiem vienrindas skriptiem līdz sarežģītām programmām, un tos izmanto, lai veiktu ļoti dažādus uzdevumus, piemēram, failu manipulācijas, sistēmas administrēšana un atkārtotu uzdevumu automatizācija.

## Shell skriptēšanas priekšrocības:

1.  **Automatizācija:** Shell skripti ļauj lietotājiem automatizēt atkārtotus uzdevumus, ietaupot laiku un samazinot cilvēka kļūdu iespējamību.
    
2.  **Pielāgošana:** lietotāji var izveidot skriptus, kas pielāgoti viņu īpašajām vajadzībām, nodrošinot augstu pielāgošanas pakāpi.
    
3.  **Pakešapstrāde:** Shell skripti ir lieliski piemēroti pakešapstrādes uzdevumu apstrādei, kur ir jāizpilda vairākas komandas pēc kārtas.
    
4.  **Sistēmas administrēšana:** Shell skripti parasti tiek izmantoti sistēmas administrēšanas uzdevumiem, piemēram, dublēšanai, žurnālu rotācijai un programmatūras instalēšanai.

## Vienkārša čaulas skripta rakstīšana:

Izveidosim pamata čaulas skriptu, kas izdrukā sveiciena ziņojumu. Atveriet teksta redaktoru un izveidojiet failu ar nosaukumu greeting.sh. Pievienojiet šādas rindas:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Saglabājiet failu un padariet to izpildāmu, terminālī izpildot šādu komandu:

```
chmod +x greeting.sh
```

Tagad jūs varat izpildīt skriptu:

```
./greeting.sh
```

Izvadei jābūt šādai:

```
Hello, welcome to the world of shell scripting!
```

## Shell skriptu palaišana Ubuntu un Linux:

Tagad mēs apspriedīsim **kā palaist .sh failu Ubuntu un Linux**.

1.  **Padariet skriptu izpildāmu:** pirms čaulas skripta palaišanas pārliecinieties, vai tas ir izpildāms. Izmantojiet komandu chmod, kā parādīts iepriekš.
    
2.  **Pāriet uz skriptu direktoriju:** atveriet termināli un izmantojiet komandu cd, lai pārietu uz direktoriju, kurā ir jūsu čaulas skripts.
    
3.  **Palaidiet skriptu:** izpildiet skriptu, terminālī ierakstot `./scriptname.sh`, aizstājot skripta nosaukums ar īsto skripta nosaukumu.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Izmantojot komandu Bash:** ja jūsu skripts sākas ar #!/bin/bash (pazīstams kā **shebang**), varat to palaist arī, izmantojot komandu bash.

```
bash greeting.sh
```

## Ko Shell Script nozīmē $@?

Apvalka skriptā `$@` apzīmē visus skriptam nodotos komandrindas argumentus. To bieži izmanto, lai atsauktos uz argumentu sarakstu kā atsevišķu entītiju. Lietojot dubultpēdiņās, piemēram, $@, tiek saglabāti atsevišķi argumenti, ņemot vērā atstarpes un īpašās rakstzīmes.

Šeit ir īss skaidrojums:

- $@: atspoguļo visus pozicionālos parametrus (argumentus), kas nodoti skriptam vai funkcijai. Katrs arguments tiek uzskatīts par atsevišķu vārdu.
    
- `$@`: ja tiek izmantotas dubultpēdas, tiek saglabāta argumentu atdalīšana, pieļaujot atstarpes vai speciālās rakstzīmes atsevišķos argumentos.
    

Šeit ir vienkāršs piemērs ilustrācijai:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Palaižot šo skriptu ar argumentiem, piemēram:

```
bash example.sh arg1 "argument 2" arg3
```

Tas izvadītu:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Kā redzat, `$@` apzīmē visus argumentus, un `$@` saglabā atsevišķus argumentus, pat ja tajos ir atstarpes.

