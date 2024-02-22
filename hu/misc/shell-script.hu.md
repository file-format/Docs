{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell script – Hogyan futtassuk Ubuntu és Linux rendszeren",
  "description":"Ismerje meg, mi az a Shell Script, és hogyan futtassa Ubuntu és Linux rendszeren",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-hu",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Mi az a Shell Script?

A shell-szkriptek egy sor parancsot írnak egy egyszerű szöveges fájlba, amelyet gyakran **Shell Scriptnek** neveznek. Ezeket a szkripteket egy shell hajtja végre, amely egy parancssori értelmező. A leggyakoribb kagylók közé tartozik

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Hal.

A shell szkriptek az egyszerű egysoros programoktól az összetett programokig terjedhetnek, és sokféle feladat elvégzésére szolgálnak, például fájlkezelésre, rendszeradminisztrációra és az ismétlődő feladatok automatizálására.

## A Shell Scripting előnyei:

1.  **Automatizálás:** A shell-szkriptek lehetővé teszik a felhasználók számára, hogy automatizálják az ismétlődő feladatokat, így időt takarítanak meg és csökkentik az emberi hibák esélyét.
    
2.  **Testreszabás:** A felhasználók egyedi igényeikre szabott szkripteket hozhatnak létre, amelyek nagyfokú testreszabást biztosítanak.
    
3.  **Kötegelt feldolgozás:** A shell-szkriptek kiválóan alkalmasak kötegelt feldolgozási feladatok kezelésére, ahol több parancsot kell egymás után végrehajtani.
    
4.  **Rendszeradminisztráció:** A shell-parancsfájlokat általában rendszeradminisztrációs feladatokhoz használják, például biztonsági mentésekhez, naplóforgatáshoz és szoftvertelepítéshez.

## Egyszerű shell-szkript írása:

Hozzunk létre egy alapvető shell-szkriptet, amely üdvözlő üzenetet nyomtat. Nyisson meg egy szövegszerkesztőt, és hozzon létre egy greeting.sh nevű fájlt. Adja hozzá a következő sorokat:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Mentse el a fájlt, és tegye végrehajthatóvá a következő parancs futtatásával a terminálban:

```
chmod +x greeting.sh
```

Most már végrehajthatja a szkriptet:

```
./greeting.sh
```

A kimenetnek a következőnek kell lennie:

```
Hello, welcome to the world of shell scripting!
```

## Shell-szkriptek futtatása Ubuntu és Linux rendszeren:

Most megvitatjuk, **hogyan lehet .sh fájlt futtatni Ubuntuban és Linuxban**.

1.  **Tegye végrehajthatóvá a szkriptet:** Mielőtt egy shell-szkriptet futtatna, győződjön meg arról, hogy az végrehajtható. Használja a chmod parancsot a korábban bemutatott módon.
    
2.  **Navigáljon a Script Directoryhoz:** Nyisson meg egy terminált, és a `cd' paranccsal navigáljon a shell-szkriptet tartalmazó könyvtárhoz.
    
3.  **Futtassa a szkriptet:** Futtassa le a szkriptet a `./scriptname.sh` beírásával a terminálba, a scriptname szó helyére a szkript tényleges nevével.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **A Bash parancs használata:** Ha a szkript `#!/bin/bash` karakterrel kezdődik (**shebang** néven ismert), akkor a `bash` paranccsal is futtathatja.

```
bash greeting.sh
```

## Mit jelent a $@ a Shell Scriptben?

A shell scriptben a `$@` a szkriptnek átadott összes parancssori argumentumot jelöli. Gyakran használják az argumentumok listájára, mint különálló entitásokra. Ha kettős idézőjelben használjuk, mint például a `$@`, megőrzi az egyéni argumentumokat, figyelembe véve a szóközöket és a speciális karaktereket.

Íme egy rövid magyarázat:

- `$@`: A szkriptnek vagy függvénynek átadott összes pozícióparamétert (argumentumot) jelöli. Minden argumentumot külön szóként kezelünk.
    
- `$@`: Dupla idézőjel esetén megőrzi az argumentumok elválasztását, lehetővé téve szóközök vagy speciális karakterek használatát az egyes argumentumokban.
    

Íme egy egyszerű példa a szemléltetésre:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Amikor ezt a szkriptet argumentumokkal futtatja, például:

```
bash example.sh arg1 "argument 2" arg3
```

Kiadná:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Amint láthatja, a `$@` az összes argumentumot jelöli, a `$@` pedig megőrzi az egyes argumentumokat, még akkor is, ha szóközt tartalmaznak.

