{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "format pliku", "typ pliku", "co to jest plik .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - Plik konfiguracyjny ASP",
  "description" :"Dowiedz się, co to jest plik ASA i interfejsy API, które mogą tworzyć i otwierać pliki ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Czym jest plik ASA?

Plik ASA to plik konfiguracyjny utworzony dla projektów [ASP](/pl/web/asp/)/ASP.NET. Zawiera deklaracje zmiennych, zawiera i funkcje, które mają być dostępne na poziomie globalnym w aplikacji. Wszystkie strony w projekcie mogą uzyskiwać dostęp do tych zmiennych i funkcji, unikając w ten sposób wymogu ich przepisywania. Jednym z takich przykładów jest strona Global.asa, która jest przechowywana w katalogu głównym, aby była dostępna dla innych stron serwisu WWW ASP. Pliki Global.asa są opcjonalne, ale jeśli są używane, każda aplikacja może mieć tylko jeden plik Global.asa.

## Format pliku ASA — więcej informacji

Pliki ASA to zwykłe pliki tekstowe z następującymi informacjami.

* Zdarzenia aplikacji
* Imprezy sesyjne
* \<object> deklaracje
* Deklaracje TypeLibrary
* dyrektywa #include

## Przykład pliku ASA

Plik Global.asa może wyglądać mniej więcej tak.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Bibliografia

* [Plik ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

