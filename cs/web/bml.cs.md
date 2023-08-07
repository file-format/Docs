{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru BML - Bean Markup Language File",
  "description":"Další informace o formátu souborů BML a rozhraních API, která mohou vytvářet a otevírat soubory BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Co je soubor BML?

Soubor s příponou .bml je soubor Bean Markup Language, který ukládá třídy Java pro podporu aplikací Java. To umožňuje přístup k objektům a metodám Java a není třeba vytvářet nové funkce pomocí tříd Java. Specifikuje, jak jsou komponenty vzájemně propojeny pro provádění užitečných úkolů. BML byl vyvinut společností IBM alphaWorks k popisu struktur a vztahů mezi komponentami. Soubory BML lze otevřít a prohlížet pomocí libovolného textového editoru, jako jsou webové prohlížeče, Microsoft Notepad a Notepad++.

## Formát souboru BML

Webová stránka IBM alphaworks poskytla dvě implementace BML. První implementace je interpret, který „přehraje“ BML skript pro generování požadované hierarchie fazolí. Druhou implementací je kompilátor, který zkompiluje libovolný BML skript do kódu Java bez reflexe. To je výhodné v tom smyslu, že umožňuje zachytit mezisložkovou strukturu aplikace pomocí jazyka, který je navržen pro tento konkrétní účel, s přidanou schopností zkompilovat ji do „běžného“ kódu Java.

## BML tagy

Následuje vysvětlení některých značek používaných v jazyce BML:

### The<bean> štítek:

The<bean> prvek se používá k vytvoření nových fazolí nebo k vyhledání fazolí podle názvu. The<bean> tag je ve formátu:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
"id" ve značce je spojeno s registrem objektů pro JavaBean.

### The<string> štítek

Tag string lze použít dvěma způsoby:

1. Chcete-li vytvořit neprázdný řetězec:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Chcete-li vytvořit prázdný řetězec:

```
<string/>
```
## Reference

* [Object-Oriented Messaging with XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)


