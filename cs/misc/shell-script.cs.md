{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell skript - Jak jej spustit na Ubuntu a Linuxu",
  "description":"Přečtěte si o tom, co je Shell Script a jak jej spustit na Ubuntu a Linuxu",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-cs",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Co je Shell Script?

Skriptování shellu zahrnuje zapsání řady příkazů do prostého textového souboru, často označovaného jako **Shell Script**. Tyto skripty jsou spouštěny shellem, což je interpret příkazového řádku. Mezi nejčastější skořápky patří

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Ryba.

Skripty shellu se mohou pohybovat od jednoduchých jednoduchých řádků až po složité programy a používají se k provádění široké škály úkolů, jako je manipulace se soubory, správa systému a automatizace opakujících se úkolů.

## Výhody skriptování Shell:

1.  **Automatizace:** Skripty prostředí umožňují uživatelům automatizovat opakující se úkoly, což šetří čas a snižuje možnost lidské chyby.
    
2.  **Přizpůsobení:** Uživatelé mohou vytvářet skripty šité na míru jejich specifickým potřebám, což poskytuje vysoký stupeň přizpůsobení.
    
3.  **Batch Processing:** Shell skripty jsou vynikající pro zpracování úloh dávkového zpracování, kde je potřeba provádět více příkazů za sebou.
    
4.  **Správa systému:** Skripty prostředí se běžně používají pro úlohy správy systému, jako je zálohování, rotace protokolů a instalace softwaru.

## Psaní jednoduchého shell skriptu:

Vytvořme základní shell skript, který vytiskne uvítací zprávu. Otevřete textový editor a vytvořte soubor s názvem `greeting.sh`. Přidejte následující řádky:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Uložte soubor a udělejte jej spustitelný spuštěním následujícího příkazu v terminálu:

```
chmod +x greeting.sh
```

Nyní můžete skript spustit:

```
./greeting.sh
```

Výstup by měl být:

```
Hello, welcome to the world of shell scripting!
```

## Spouštění skriptů Shell na Ubuntu a Linuxu:

Nyní probereme **jak spustit soubor .sh v Ubuntu a Linuxu**.

1.  **Udělejte ze skriptu spustitelný:** Před spuštěním shellového skriptu se ujistěte, že je spustitelný. Použijte příkaz `chmod`, jak bylo uvedeno výše.
    
2.  **Přejděte do adresáře skriptů:** Otevřete terminál a pomocí příkazu `cd` přejděte do adresáře obsahujícího váš skript shellu.
    
3.  **Spusťte skript:** Skript spusťte zadáním `./scriptname.sh` do terminálu a nahraďte scriptname skutečným názvem vašeho skriptu.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Pomocí příkazu Bash:** Pokud váš skript začíná `#!/bin/bash` (známý jako **shebang**), můžete jej spustit také pomocí příkazu `bash`.

```
bash greeting.sh
```

## Co znamená $@ v Shell Script?

Ve skriptu shellu `$@` představuje všechny argumenty příkazového řádku předané skriptu. Často se používá k odkazování na seznam argumentů jako na samostatné entity. Při použití v dvojitých uvozovkách, jako je `$@`, zachovává jednotlivé argumenty, počítá s mezerami a speciálními znaky.

Zde je stručné vysvětlení:

- `$@`: Představuje všechny poziční parametry (argumenty) předané skriptu nebo funkci. Každý argument je považován za samostatné slovo.
    
- `$@`: Při dvojitých uvozovkách zachovává oddělení argumentů a umožňuje mezery nebo speciální znaky v jednotlivých argumentech.
    

Zde je jednoduchý příklad pro ilustraci:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Když spustíte tento skript s argumenty, například:

```
bash example.sh arg1 "argument 2" arg3
```

Vyšlo by to:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Jak vidíte, `$@` představuje všechny argumenty a `$@` zachovává jednotlivé argumenty, i když obsahují mezery.

