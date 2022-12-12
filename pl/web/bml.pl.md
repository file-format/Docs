{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku BML - plik języka znaczników fasoli",
  "description":"Poznaj format pliku BML i interfejsy API, które mogą tworzyć i otwierać pliki BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Czym jest plik BML?

Plik z rozszerzeniem .bml to plik Bean Markup Language, który przechowuje klasy Java do obsługi aplikacji Java. Umożliwia to dostęp do obiektów i metod Java i nie wymaga tworzenia nowych funkcji przy użyciu klas Java. Określa, w jaki sposób komponenty są ze sobą połączone w celu wykonywania użytecznych zadań. BML został opracowany przez IBM alphaWorks w celu opisania relacji między strukturami i komponentami. Pliki BML można otwierać i przeglądać za pomocą dowolnego edytora tekstu, takiego jak przeglądarki internetowe, Microsoft Notepad i Notepad ++.

## Format pliku BML

Witryna IBM alphaworks udostępnia dwie implementacje BML. Pierwsza implementacja to interpreter, który „odtwarza” skrypt BML w celu wygenerowania pożądanej hierarchii komponentów bean. Druga implementacja to kompilator, który kompiluje dowolny skrypt BML do wolnego od refleksji kodu Java. Jest to korzystne w tym sensie, że umożliwia przechwycenie międzykomponentowej struktury aplikacji przy użyciu języka zaprojektowanego do tego konkretnego celu z dodatkową możliwością kompilacji go do „zwykłego” kodu Java.

## Tagi BML

Poniżej znajduje się wyjaśnienie niektórych znaczników używanych w języku BML:

###<bean> etykietka:

The<bean> element służy do tworzenia nowych komponentów bean lub do wyszukiwania komponentów bean według nazwy. The<bean> tag ma format:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
„id” w znaczniku jest powiązane z rejestrem obiektów dla komponentu JavaBean.

###<string> etykietka

Istnieją dwa sposoby użycia tagu string:

1. Aby utworzyć niepusty ciąg znaków:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Aby utworzyć pusty ciąg:

```
<string/>
```
## Bibliografia

* [Przesyłanie wiadomości zorientowane obiektowo za pomocą XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Fizyczny język znaczników] (http://web.mit.edu/mecheng/pml/standards.htm)
* [Język znaczników Bean](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

