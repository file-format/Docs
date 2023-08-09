{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java Manifest File Format",
  "description":"Další informace o formátu souboru MF a rozhraních API, která mohou vytvářet a otevírat soubory MF.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor MF?

Soubor s příponou .mf je soubor Java Manifest, který obsahuje informace o jednotlivých položkách souboru [JAR](/cs/programming/jar/). Samotný soubor MF je obsažen v souboru JAR a poskytuje všechna rozšíření a definice související s balíčkem. Soubory JAR lze vytvořit pro použití jako spustitelný soubor. V takovém případě soubor mainfest specifikuje hlavní třídu aplikace, která obsahuje příkaz **`public static void main`**. Soubory manifestu jsou pojmenovány jako MANIFEST.MF a lze je otevřít pomocí libovolného textového editoru v operačních systémech Windows, MacOS a Linux.

## Specifikace formátu manifestu

[Specifikace formátu souboru manifestu](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) jsou k dispozici společností Oracle ve své příručce pro formát souborů JAR. Soubor Manifest se skládá z hlavních sekcí, za kterými následuje seznam sekcí pro jednotlivé položky souboru JAR. Každá sekce má určitá pravidla a omezení.

### Hlavní sekce

Hlavní sekce:

* obsahuje informace o zabezpečení a konfiguraci souboru JAR
* obsahuje informace o aplikaci nebo rozšíření, které je soubor JAR součástí
* definuje hlavní atributy pro každou jednotlivou položku manifestu

**Poznámka**: Žádný atribut v této sekci nemůže být pojmenován jako „Jméno“.

### Jednotlivé sekce

Jednotlivá sekce definuje různé atributy pro balíčky nebo soubory souboru JAR. Každá sekce musí začínat atributem s názvem "Name", jehož hodnota musí být relativní cesta k souboru nebo absolutní URL odkazující na data mimo archiv.

### Manifest Specifikace

|Atributy|Popis|
---|---|
|manifest-soubor|hlavní-sekce nový řádek *individuální-sekce|
|hlavní sekce|informace o verzi nový řádek *hlavní-atribut|
|version-info|Manifest-Version : číslo-verze|
|číslo-verze|číslice+{.číslice+}*|
|hlavní-atribut|(jakýkoli legitimní hlavní atribut) nový řádek|
|individuální-sekce|Jméno : hodnota nový řádek *perentry-attribute|
|perentry-attribute|(jakýkoli legitimní atribut perentry) nový řádek|
|nový řádek|CR LF | LF | ČR (nenásleduje LF)|
|číslice|{0-9}|

## Reference

* [Oracle – formát souboru JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [Formát souboru JAR](https://en.wikipedia.org/wiki/JAR_(file_format))

