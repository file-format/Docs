{
  "date" : "2020-03-02",
  "keywords" :["SVG", "plik", "format pliku", "Język opisu strony", "Skalarny"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku SVG i interfejsy API, które mogą tworzyć i otwierać pliki SVG.",
  "title" :"Co to jest plik SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Co to jest plik SVG? ##

Plik SVG to plik skalarnej grafiki wektorowej, który używa formatu tekstowego opartego na XML do opisywania wyglądu obrazu. Słowo Scalable odnosi się do faktu, że SVG można skalować do różnych rozmiarów bez utraty jakości. Opis tekstowy takich plików uniezależnia je od rozdzielczości. Jest to jeden z najczęściej używanych formatów do budowy strony internetowej i drukowania grafiki w celu uzyskania skalowalności. Format ten może być jednak używany tylko w przypadku grafiki dwuwymiarowej. Pliki SVG można przeglądać/otwierać w prawie wszystkich nowoczesnych przeglądarkach, w tym Chrome, Internet Explorer, Firefox i Safari.

## Krótka historia ##

Specyfikacje SVG są dostępne jako otwarty standard przez World Wide Web Consortium (W3C) od 1999 roku. Wcześniej podobne specyfikacje formatu plików w sześciu różnych formatach były przesyłane do W3C do 1998 roku. Aktualizacja specyfikacji została zastosowana w 2011 roku i była w wersji 1.1 . W 2016 roku SVG 2 został opublikowany jako nowsza wersja zawierająca funkcje dodatkowe do tych w SVG 1.1.

## Specyfikacje formatu plików ##

Obiektowy model dokumentu SVG (DOM) kładzie podwaliny pod wszystkie specyfikacje i interfejsy, które odpowiadają poszczególnym sekcjom specyfikacji. Przeglądarki SVG muszą zaimplementować interfejsy SVG DOM zgodnie z definicją w specyfikacjach W3C. Jego DOM udostępnia kilka interfejsów dla różnych typów danych i elementów.

### Kształty SVG ###

SVG ma kilka predefiniowanych elementów kształtu, które mogą być używane przez programistów:

* Prostokąt<rect>
* Koło<circle>
* Elipsa<ellipse>
* Linia<line>
* Polilinia<polyline>
* Wielokąt<polygon>
* Ścieżka<path>

W oparciu o te kształty i specyfikacje, obszary funkcjonalne SVG są następujące.

**Ścieżki** — ścieżki są używane do reprezentowania prostych i złożonych konturów kształtów. Kody służą do określenia charakteru operacji. Na przykład M służy do Przenieś do, L służy do Linia do, Z służy do zamknięcia ścieżki i tak dalej.

**Kształty podstawowe** — Można rysować ścieżki proste i ścieżki złożone z serii połączonych segmentów linii prostych (polilinii), a także zamknięte wielokąty, okręgi i elipsy. Prostokąty i prostokąty z zaokrąglonymi rogami są również standardowymi elementami.

**Tekst** — reprezentacja tekstu jest wyrażona jako dane znakowe XML, w których można zastosować wiele efektów wizualnych do tekstu. Specyfikacje umożliwiają obsługę tekstu dwukierunkowego, tekstu pionowego i znaków wzdłuż zakrzywionej ścieżki.

**Malowanie** — kształty można wypełniać i/lub obrysowywać kolorem, gradientem lub wzorem, co pozwala na uzyskanie nieprzezroczystości lub dowolnego stopnia przezroczystości. Elementy końca linii, takie jak groty strzałek lub symbole pojawiające się na wierzchołkach wielokąta, są reprezentowane przez Znaczniki.

**Kolor** — specyfikacje SVG umożliwiają stosowanie kolorów do wszystkich widocznych elementów SVG bezpośrednio lub za pomocą wypełnienia, obrysu i innych właściwości. Do określenia można użyć różnych kodów kolorów, takich jak czarny lub niebieski, reprezentacja szesnastkowa, dziesiętna lub procentowa w postaci RGB.

**Gradienty i wzory** — kształty w pliku SVG można wypełnić lub obrysować jednolitymi kolorami, gradientami lub powtarzającymi się wzorami.

**Efekty filtrów** - W rzeczywistości jest to seria operacji graficznych, które są stosowane do danej źródłowej grafiki wektorowej w celu uzyskania zmodyfikowanego wyniku.

**Interaktywność** — użytkownicy mogą wchodzić w interakcje z plikami SVG, zmieniając ostrość, klikając myszką, przewijając lub powiększając obraz. Interaktywność umożliwia obrazom SVG interakcję z użytkownikami na wiele różnych sposobów, jak wspomniano powyżej.

**Łączenie** — obrazy SVG mogą zawierać hiperłącza do innych dokumentów. Osiąga się to za pomocą XML Linking Language lub XLink. Pozwala to na tworzenie określonych stanów widoku, które służą do powiększania/pomniejszania określonego obszaru lub ograniczania widoku do określonego elementu.

**Skrypty** — podobnie jak w przypadku HTML, wszystkimi aspektami dokumentu SVG można manipulować za pomocą skryptów. Obiekty SVG DOM zawierają wskazówki, jak to osiągnąć za pomocą elementu i atrybutu SVG. Skrypty są zawarte w elementach znaczników `script` i mogą być uruchamiane w odpowiedzi na zdarzenia związane ze wskaźnikiem, klawiaturą lub dokumentem.

**Animacja** — elementy DOM<animate> ,<animateMotion> oraz<animateColor> pozwala dołączyć animację do treści SVG. Oczywiście nie jest to możliwe bez użycia skryptów i wbudowanych timerów. Te animacje mogą być ciągłe i można je zapętlać lub powtarzać, jednocześnie reagując na zdarzenia użytkownika.

**Czcionki** — tekst w formacie SVG może odwoływać się do zewnętrznych plików czcionek, takich jak czcionki systemowe. W przypadku braku takich czcionek tekst w SVG nie będzie renderowany na wyjściu. Można temu zaradzić, włączając wymagane glify do takiego pliku jako czcionkę, która jest następnie renderowana przy użyciu<text> element.

## Przykłady ##
Poniższe wiersze pokazują, w jaki sposób koło jest reprezentowane za pomocą skryptu SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Poniższe wiersze kodu pokazują, jak używać<text> blok do renderowania tekstu do SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Bibliografia ##

* [Specyfikacje W3C SVG](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

