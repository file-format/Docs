{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","co je soubor jar","jak otevřít soubor jar", "přípona", "soubor", "soubor jar","formát souboru jar", "přípona .jar"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java Archive File Format",
  "description":"Další informace o formátu souboru JAR a rozhraních API, která mohou vytvořit a otevřít soubor JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor JAR?

Soubor s příponou .jar je soubor Java Archive, který obsahuje mnoho různých souborů souvisejících s aplikací jako jeden soubor. Tento formát souboru byl vytvořen za účelem snížení rychlosti načítání staženého Java Applet v prohlížeči prostřednictvím HTTP transakce, a to tím, že se vyhýbá vytváření vícenásobných HTTP připojení. Jeden soubor JAR může obsahovat soubory třídy Java ([.class](/cs/programming/class/)), [images](/cs/image/) a [sounds](/cs/audio/). Jednotlivé položky v souboru JAR mohou být digitálně podepsány vývojářem aplikace za účelem ověření jejich původu. Soubory JAR se pravidelně používají k vytváření funkčních rozhraní API, která obsahují konkrétní funkce související s tímto rozhraním API.

## Formát souboru JAR

Soubory JAR jsou založeny na oblíbeném [formátu souboru ZIP](/cs/compression/zip/), který archivuje jednotlivé soubory obsahu do jednoho souboru. Formát souboru JAR podporuje komprese, což má za následek menší velikost souboru pro stahování, a tím dále zkracuje dobu stahování. [Specifikace souboru JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce společnosti Oracle poskytuje úplné podrobnosti o interních specifikacích souborů JAR.

### Soubor manifestu

Když je vytvořen soubor JAR, automaticky se v něm vytvoří soubor manifestu, který obsahuje informace o metadatech o obsahu souboru JAR. Tento soubor zobrazuje obsah, který je zabalen v souboru JAR. Typický soubor Manifest vypadá následovně, který ukazuje složky a třídy obsažené v souboru JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifest specifikace

Specifikace manifestu jsou definovány společností Oracle následovně.

`manifest-file`: nový řádek hlavní sekce \*individuální sekce

`hlavní sekce`: informace o verzi nový řádek \*hlavní-atribut

`version-info`: Manifest-Version: číslo verze

`číslo-verze` : digit+{.digit+}*

`main-attribute`: (jakýkoli legitimní hlavní atribut) nový řádek

`individuální-sekce`: Název : hodnota nový řádek \*perentry-atribut

`perentry-attribute`: (jakýkoli legitimní atribut perentry) nový řádek

"nový řádek": CR LF | LF | ČR (nenásleduje LF)

`digit`: {0-9}

### Spustitelný soubor JAR

Soubory JAR mohou také obsahovat aplikaci, kterou lze spustit pomocí Java Virtual Machine (JVM), podobně jako jakákoli jiná aplikace v operačním systému Microsoft Windows. V tomto případě potřebuje JVM vědět o vstupním bodu aplikace, kterým je jakákoli třída s veřejnou statickou metodou void main. Soubor manifestu identifikuje takovou třídu hlavičkou „Main-Class“ v následujícím formátu:

```
Main-Class: com.example.MyClassName
```



## Reference

* [Přehled souboru JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Formát souboru JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

