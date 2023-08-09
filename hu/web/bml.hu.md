{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML fájlformátum - Bean Markup Language File",
  "description":"További információ a BML-fájlformátumról és az API-król, amelyek BML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Mi az a BML fájl?

A .bml kiterjesztésű fájl egy Bean Markup Language fájl, amely Java-osztályokat tárol a Java-alkalmazások támogatásához. Ez lehetővé teszi a hozzáférést a Java objektumokhoz és metódusokhoz, és nincs szükség új funkciók létrehozására Java osztályok használatával. Meghatározza, hogy az összetevők hogyan kapcsolódnak egymáshoz a hasznos feladatok elvégzéséhez. A BML-t az IBM alphaWorks fejlesztette ki a struktúrák és az összetevők kapcsolatainak leírására. A BML-fájlok bármely szövegszerkesztővel megnyithatók és megtekinthetők, például webböngészővel, Microsoft Notepaddal és Notepad++-val.

## BML fájlformátum

Az IBM alphaworks webhely a BML két megvalósítását kínálja. Az első megvalósítás egy értelmező, amely "lejátszik" egy BML-szkriptet a kívánt komponens-hierarchia létrehozásához. A második megvalósítás egy olyan fordító, amely bármilyen BML-szkriptet tükröződésmentes Java kódra fordít. Ez abban az értelemben előnyös, hogy lehetővé teszi az alkalmazás komponensek közötti struktúrájának rögzítését egy erre a célra kialakított nyelv segítségével, azzal a képességgel, hogy azt „normál” Java kódba fordítsa.

## BML címkék

Az alábbiakban néhány, a BML nyelvben használt címkét magyarázunk:

### Az<bean> címke:

Az<bean> elemet új babok létrehozására vagy a babok név szerinti megkeresésére használják. Az<bean> a címke formátuma:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
A címkében lévő „id” a JavaBean objektum-nyilvántartásához van társítva.

### Az<string> címke

A karakterlánc-címke kétféleképpen használható:

1. Nem üres karakterlánc létrehozása:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Üres karakterlánc létrehozása:

```
<string/>
```
## Hivatkozások

* [Objektumorientált üzenetkezelés XML-lel](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [The Physical Markup Language](http://web.mit.edu/mecheng/pml/standards.htm)


