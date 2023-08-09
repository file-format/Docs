{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů PYC a rozhraních API, která mohou vytvářet a otevírat soubory PYC.",
  "title" :"PYC File Format - Python Compiled File",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Co je soubor PYC?

Soubor PYC je zkompilovaný výstupní soubor generovaný ze zdrojového kódu napsaného v programovacím jazyce Python. Když je soubor PY spuštěn pomocí interpretu Python, je převeden na bajtový kód pro spuštění. Současně je zkompilovaný bajtový kód také uložen jako soubor .pyc, aby mohl být později znovu použit z mezipaměti, pokud je to možné.

## Struktura formátu souboru PYC

Soubory PYC jsou v bajtovém kódu a specifikace jejich formátu souborů nejsou veřejně dostupné. Průzkum některých zdrojů však ukazuje, že [struktura souboru PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) se skládá z:

* `Čtyřbajtové magické číslo`r – Jednoduše dva bajty, které se mění s každou změnou zařazovacího kódu, a pak dva bajty 0d0a.
* `Čtyřbajtové časové razítko modifikace` - Unixové časové razítko modifikace zdrojového souboru, který vygeneroval .pyc, takže jej lze znovu zkompilovat, pokud se zdroj změní.
* `Objekt seřazeného kódu` - výstup marshal.dump objektu kódu, který je výsledkem kompilace zdrojového souboru.

## Reference

* [Struktura souborů .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

