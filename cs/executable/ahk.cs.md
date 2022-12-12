{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů AHK a rozhraních API, která mohou vytvářet a otevírat soubory AHK.",
  "title" :"Formát souboru AHK - soubor skriptu AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## Co je soubor AHK?

Soubor AHK je soubor skriptu generovaný softwarovou aplikací AutoHotkey, která se používá pro automatizaci úloh v systému Microsoft Windows. Obsahuje pokyny pro automatizaci úloh pomocí klávesových zkratek, které lze použít k provádění okamžitých akcí. Soubor je spuštěn AutoHotkey a všechny akce jsou prováděny postupně. Soubory AHK jsou dostatečně výkonné k provádění složitých úkolů pomocí klávesových zkratek definovaných pomocí klávesových zkratek. Soubory AHK lze otevřít pomocí textových editorů, jako je Microsoft Notepad a Notepad++.

## Formát souboru AHK

Soubory AHK se ukládají na disk jako soubory ve formátu prostého textu a obsahují řádky kódu, které lze spustit pomocí AutoHotkey. AutoHotkey je bezplatný skriptovací jazyk s otevřeným zdrojovým kódem a umožňuje uživatelům vytvářet jednoduché až složité skripty pro provádění akcí, jako jsou vyplňování formulářů, automatické klepání, spouštění maker atd. Soubor AHK může provést minimálně jednu akci a poté ukončit .

K dispozici jsou nástroje, které lze použít ke konverzi souborů AHK na soubory [Exe](/cs/executable/exe/).

### Příklad AHK

Následující příklad používá klávesu Win+Z ke spuštění programu Microsoft Poznámkový blok nebo jej přenese do popředí, pokud již běží.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Jak vytvořím soubor AHK?

K vytvoření souboru AHK lze použít následující kroky. Ty předpokládají, že AutoHotkey je již v počítači nainstalován.

* Klepněte pravým tlačítkem myši na plochu.
* Najděte v nabídce "Nové".
* Klikněte na "AutoHotkey Script" v nabídce "Nový".
* Dejte skriptu nový název.
* Najděte nově vytvořený soubor na ploše a klikněte na něj pravým tlačítkem.
* Klikněte na "Upravit skript".
* Mělo se objevit okno, pravděpodobně Poznámkový blok.
* Uložte soubor.

## Reference

* [AutoHotkey](https://www.autohotkey.com/)
* [Dávkový soubor – od Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

