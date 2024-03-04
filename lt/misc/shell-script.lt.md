{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell scenarijus – kaip jį paleisti Ubuntu ir Linux",
  "description":"Sužinokite, kas yra „Shell Script“ ir kaip jį paleisti „Ubuntu“ ir „Linux“.",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-lt",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Kas yra „Shell Script“?

Shell scenarijus apima komandų serijos rašymą paprasto teksto faile, dažnai vadinamu **Shell Script**. Šiuos scenarijus vykdo apvalkalas, kuris yra komandų eilutės vertėjas. Dažniausiai pasitaikantys apvalkalai apima

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Žuvis.

Apvalkalo scenarijai gali skirtis nuo paprastų vienarūšių iki sudėtingų programų, be to, jie naudojami įvairioms užduotims atlikti, pavyzdžiui, failų tvarkymui, sistemos administravimui ir pasikartojančių užduočių automatizavimui.

## „Shell“ scenarijų pranašumai:

1.  **Automatizavimas:** Shell scenarijai leidžia vartotojams automatizuoti pasikartojančias užduotis, taupant laiką ir sumažinant žmogiškųjų klaidų tikimybę.
    
2.  **Tinkinimas:** naudotojai gali kurti scenarijus, pritaikytus jų konkretiems poreikiams, užtikrindami aukštą tinkinimo laipsnį.
    
3.  **Paketinis apdorojimas:** Shell scenarijai puikiai tinka paketinio apdorojimo užduotims, kai reikia paeiliui vykdyti kelias komandas.
    
4.  **Sistemos administravimas:** Shell scenarijai dažniausiai naudojami sistemos administravimo užduotims, pvz., atsarginėms kopijoms kurti, žurnalo rotacijai ir programinės įrangos diegimui.

## Paprasto apvalkalo scenarijaus rašymas:

Sukurkime pagrindinį apvalkalo scenarijų, kuris spausdina sveikinimo pranešimą. Atidarykite teksto rengyklę ir sukurkite failą pavadinimu greeting.sh. Pridėkite šias eilutes:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Išsaugokite failą ir padarykite jį vykdomąjį paleisdami šią komandą terminale:

```
chmod +x greeting.sh
```

Dabar galite vykdyti scenarijų:

```
./greeting.sh
```

Išvestis turėtų būti:

```
Hello, welcome to the world of shell scripting!
```

## „Shell“ scenarijų paleidimas „Ubuntu“ ir „Linux“:

Dabar aptarsime **kaip paleisti .sh failą Ubuntu ir Linux**.

1.  **Padarykite scenarijų vykdomąjį:** prieš paleisdami apvalkalo scenarijų įsitikinkite, kad jis yra vykdomas. Naudokite komandą chmod, kaip parodyta anksčiau.
    
2.  **Eikite į scenarijaus katalogą:** atidarykite terminalą ir naudokite komandą cd, kad pereitumėte į katalogą, kuriame yra jūsų apvalkalo scenarijus.
    
3.  **Paleiskite scenarijų:** Vykdykite scenarijų terminale įvesdami `./scriptname.sh`, pakeisdami scenarijaus pavadinimą tikruoju scenarijaus pavadinimu.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Naudojant komandą Bash:** jei jūsų scenarijus prasideda #!/bin/bash (žinoma kaip **shebang**), taip pat galite jį paleisti naudodami komandą bash.

```
bash greeting.sh
```

## Ką „Shell Script“ reiškia $@?

Apvalkalo scenarijuje $@ reiškia visus komandinės eilutės argumentus, perduodamus scenarijui. Jis dažnai naudojamas norint nurodyti argumentų sąrašą kaip atskirus objektus. Kai naudojamas dvigubose kabutėse, pvz., $@, jis išsaugo atskirus argumentus, atsižvelgia į tarpus ir specialiuosius simbolius.

Štai trumpas paaiškinimas:

- `$@`: nurodo visus padėties parametrus (argumentus), perduodamus scenarijui arba funkcijai. Kiekvienas argumentas traktuojamas kaip atskiras žodis.
    
- `$@`: kai kabutės yra dvi, išsaugomas argumentų atskyrimas, atskiruose argumentuose leidžiama naudoti tarpus arba specialiuosius simbolius.
    

Štai paprastas pavyzdys iliustruoti:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Kai paleidžiate šį scenarijų su argumentais, pavyzdžiui:

```
bash example.sh arg1 "argument 2" arg3
```

Išvestų:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Kaip matote, $@ reiškia visus argumentus, o $@ išsaugo atskirus argumentus, net jei juose yra tarpų.

