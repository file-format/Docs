{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Script Shell - Cum să îl rulați pe Ubuntu și Linux",
  "description":"Aflați despre ce este Shell Script și cum să-l rulați pe Ubuntu și Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-ro",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Ce este Shell Script?

Scriptul Shell implică scrierea unei serii de comenzi într-un fișier text simplu, adesea denumit **Script Shell**. Aceste scripturi sunt executate de un shell, care este un interpret de linie de comandă. Cele mai comune cochilii includ

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Peşte.

Scripturile Shell pot varia de la simple versiuni simple la programe complexe și sunt utilizate pentru a efectua o mare varietate de sarcini, cum ar fi manipularea fișierelor, administrarea sistemului și automatizarea sarcinilor repetitive.

## Beneficiile Shell Scripting:

1.  **Automatizare:** Scripturile Shell permit utilizatorilor să automatizeze sarcini repetitive, economisind timp și reducând șansa de eroare umană.
    
2.  **Personalizare:** Utilizatorii pot crea scripturi adaptate nevoilor lor specifice, oferind un grad ridicat de personalizare.
    
3.  **Procesare în lot:** Scripturile Shell sunt excelente pentru gestionarea sarcinilor de procesare în lot, în care mai multe comenzi trebuie executate în secvență.
    
4.  **Administrarea sistemului:** Scripturile Shell sunt utilizate în mod obișnuit pentru sarcinile de administrare a sistemului, cum ar fi copii de siguranță, rotația jurnalelor și instalarea software-ului.

## Scrierea unui script Shell simplu:

Să creăm un script shell de bază care imprimă un mesaj de salut. Deschideți un editor de text și creați un fișier numit `greeting.sh`. Adăugați următoarele rânduri:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Salvați fișierul și faceți-l executabil rulând următoarea comandă în terminal:

```
chmod +x greeting.sh
```

Acum, puteți executa scriptul:

```
./greeting.sh
```

Ieșirea ar trebui să fie:

```
Hello, welcome to the world of shell scripting!
```

## Rularea scripturilor Shell pe Ubuntu și Linux:

Acum, vom discuta despre **cum să rulați un fișier .sh în Ubuntu și Linux**.

1.  **Faceți scriptul executabil:** Înainte de a rula un script shell, asigurați-vă că este executabil. Utilizați comanda `chmod` așa cum este arătat mai devreme.
    
2.  **Navigați la directorul de scripturi:** deschideți un terminal și utilizați comanda `cd` pentru a naviga la directorul care conține scriptul dvs. shell.
    
3.  **Run the Script:** Executați scriptul tastând `./scriptname.sh` în terminal, înlocuind scriptname” cu numele real al scriptului dumneavoastră.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Folosind comanda Bash:** Dacă scriptul începe cu `#!/bin/bash` (cunoscut sub numele de **shebang**), îl puteți rula și folosind comanda `bash`.

```
bash greeting.sh
```

## Ce înseamnă $@ în Scriptul Shell?

În scriptul shell, `$@` reprezintă toate argumentele liniei de comandă transmise scriptului. Este adesea folosit pentru a face referire la lista de argumente ca entități separate. Când este folosit între ghilimele duble, cum ar fi `$@`, păstrează argumentele individuale, luând în considerare spațiile și caracterele speciale.

Iată o scurtă explicație:

- `$@`: Reprezintă toți parametrii poziționali (argumentele) transmise scriptului sau funcției. Fiecare argument este tratat ca un cuvânt separat.
    
- `$@`: Când sunt duble ghilimele, păstrează separarea argumentelor, permițând spații sau caractere speciale în cadrul argumentelor individuale.
    

Iată un exemplu simplu de ilustrat:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Când rulați acest script cu argumente, de exemplu:

```
bash example.sh arg1 "argument 2" arg3
```

Ar scoate:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

După cum puteți vedea, `$@` reprezintă toate argumentele, iar `$@` păstrează argumentele individuale, chiar dacă acestea conțin spații.

