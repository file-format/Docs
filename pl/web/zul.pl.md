{
  "date" : "2021-05-24",
  "keywords" :["zul", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "otwórz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - plik interfejsu użytkownika ZK",
  "description":"Poznaj format pliku ZUL i interfejsy API, które mogą tworzyć i otwierać pliki ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Czym jest plik ZUL?

Plik z rozszerzeniem .zul to plik internetowy utworzony za pomocą języka znaczników interfejsu użytkownika (ZUML) i zawiera definicje elementów interfejsu użytkownika. Klasy Ajax i Java obsługują ZUML oparty na [XML](/pl/web/xml/) do tworzenia plików po stronie serwera. Format pliku ZUL został opracowany przez ZK, platformę interfejsu użytkownika, która umożliwia tworzenie aplikacji internetowych i mobilnych bez znajomości JavaScript lub AJAX.

## Format pliku ZUL

Pliki ZUL są oparte na XML i składają się z różnych elementów do budowy interfejsu użytkownika. Program ładujący ZK używa każdego elementu XML do utworzenia komponentu. Ogólne przetwarzanie elementów strony, takich jak tytuł strony, opis itp., jest opisane w każdej instrukcji przetwarzania XML ZUML.

### ZUL Przykład

W poniższym przykładzie kodu ZUML pierwsza linia określa tytuł strony, druga tworzy główny komponent z tytułem i obramowaniem, a trzecia tworzy przycisk z etykietą i detektor zdarzeń.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Schemat ZUL można pobrać ze strony http://www.zkoss.org/2005/zul/zul.xsd.
## Bibliografia

* [ZUL - By ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Schemat ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

