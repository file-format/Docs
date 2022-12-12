{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Make File - Xcode Makefile Script File",
  "description":"Další informace o formátu XCode MakeFile a rozhraních API, která mohou vytvářet a otevírat soubory MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Co je soubor MAKE?

Soubor MAKE je soubor skriptu XCode, který organizuje kompilaci kódu. Používá se ke kompilaci a propojení programů z více souborů zdrojového kódu. Tato nápověda vám pomůže rozhodnout, které části velké aplikace je nutné překompilovat, když je třeba aplikaci aktualizovat. Aby soubory používaly řadu instrukcí ke spuštění v závislosti na tom, jaké soubory se změnily.

## Příklad formátu souboru MAKE

Následující obsah se provádí pomocí nástroje Make a výstupy jsou následující.

```
hello:
	echo "hello world"
```
**Vytvořit výstup**

```
$ make
echo "hello world"
hello world
```

## Reference
* [XCode and Make – Apple Forums](https://developer.apple.com/forums/thread/657458)
* [Průvodce objektem C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

