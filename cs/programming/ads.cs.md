
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor ADS - Formát souboru specifikace Ada",
  "description":"Zjistěte, co je formát souboru ADS s příklady a rozhraními API, která mohou vytvářet a otevírat soubory ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Co je soubor ADS?

Soubor ADS je soubor specifikace pro projekt programování Ada. Je to obdoba třídy pro Javu nebo dvojice záhlaví a implementace v případě C++. Veřejné a soukromé specifikace balíčku Ada jsou uloženy v souboru .ads. Soubor .adb naproti tomu obsahuje implementaci neboli těla Ada. Stejně jako [C++](/cs/programming/cpp/) nabízí Ada oddělení mezi specifikacemi a implementacemi nezávisle na OOP.

Soubory ADS lze otevřít v libovolném textovém editoru, jako je Microsoft Notepad, Notepad++ a Atom.

## Formát souboru ADS

Soubory ADS jsou ve formátu jednoduchého textového souboru a lze je otevřít/upravit pomocí libovolného textového editoru. Balíčky Ada lze organizovat do hierarchií. Podřízenou jednotku lze deklarovat následujícím způsobem:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Reference

* [Balíčky Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

