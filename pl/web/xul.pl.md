{
  "date" : "2021-05-24",
  "keywords" :["xul", "Plik", "Rozszerzenie", "Format pliku", "Rozszerzenie pliku", "Język interfejsu użytkownika XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - plik języka interfejsu użytkownika XML",
  "description":"Poznaj format pliku XUL i interfejsy API, które mogą tworzyć i otwierać pliki XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Czym jest plik XUL?

Plik z rozszerzeniem .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) oznacza XML User Interface Language) to plik języka znaczników oparty na [XML](/pl/web/xml/) dla tworzenie interfejsów użytkownika. Został opracowany przez Mozillę dla programistów do tworzenia graficznych elementów interfejsu użytkownika podobnych do innych języków znaczników używanych do tworzenia stron internetowych. XUL był szeroko używany przez Mozillę w jej przeglądarce Firefox, gdzie wykorzystywał bazę kodu Mozilli. Renderowanie XUL odbywa się za pomocą
[Silnik Gecko](https://en.wikipedia.org/wiki/Gecko_(oprogramowanie)). Rozwidlenia Firefoksa, takie jak Pale Moon, Basilisk i Waterfox, zachowują obsługę dodatków XUL. Pliki XUL są identyfikowane za pomocą typu MIME: application/vnd.mozilla.xul+xml.

## Format pliku XUL

Pliki XUL są zapisywane zwykłym tekstem opartym na formacie pliku XML i są renderowane przy użyciu silnika Gecko. Trzy główne części struktury XUL to:

* `Zawartość` — obejmuje deklaracje okna i zawarte w nich elementy interfejsu użytkownika.
* `Skóra` — zawiera wszelkie arkusze stylów, obrazy i inne pliki związane z motywami. Wygląd okna jest opisany w arkuszach stylów.
* `Locale` - Tekst wyświetlany w oknie jest przechowywany oddzielnie, a użytkownicy mogą używać wielu zestawów plików językowych.

### Przykład XUL

Poniższy przykład tworzy trzy przyciski, które są ułożone jeden na drugim w kierunku pionowym.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Bibliografia

* [XUL – z Wikipedii](https://en.wikipedia.org/wiki/XUL)
* [Zarchiwizowana dokumentacja XUL – autorstwa Mozilli](https://wiki.mozilla.org/XUL:Home_Page)

