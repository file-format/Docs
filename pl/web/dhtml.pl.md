{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml","plik dhtml", "format pliku dhtml", "typ pliku dhtml", "plik", "typ", "co to jest plik dhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - Dynamiczny Format Pliku HTML",
  "description":"Poznaj format pliku DHTML i interfejsy API, które mogą tworzyć i otwierać pliki DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik DHTML?

Plik z rozszerzeniem .dhtml to dynamiczny plik [HTML](/pl/web/html/), który służy do tworzenia dynamicznej zawartości strony internetowej. Element webowy utworzony w DHTML jest sterowany zdarzeniami i nie wymaga przeładowania strony. W większości przypadków plik DHTML jest używany do tworzenia dynamicznej zawartości strony internetowej, takiej jak rozwijane menu, pływające warstwy, przyciski przewijania i inne dynamiczne treści. Z dynamicznymi elementami html spotykasz się prawie codziennie w swoim życiu, gdy najedziesz myszką na element menu i otworzy się dalsze opcje podmenu. DHTML korzysta z technologii internetowych, takich jak [HTML](/pl/web/html/), [Javascript](/pl/web/js/), HTML DOM, HTML Events i [CSS](/pl/web/css/), aby osiągnąć zachowanie elementów.

## Format pliku DHTML

Pliki DHTML to zwykłe pliki tekstowe zawierające kod DHTML do implementacji dynamicznego zachowania elementów internetowych.


### DOM DHTML

Obiektowy model dokumentu DHTML (DOM) jest oparty na DOM HTML, który jest strukturą drzewa z elementami, atrybutami i tekstem, jak pokazano na poniższym obrazku.

{{< figure src="../dhtml.png" alt="DOM HTML" >}}

Węzeł `Document` może być użyty do wywołania kilku funkcji w celu zaimplementowania różnych funkcjonalności. Poniższy przykład po prostu wykorzystuje metodę document.write() języka JavaScript w kodzie DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Ten kod zapisuje tekst „Hello World” do wyświetlenia w przeglądarce.

### Zdarzenia DHTML

|Nr S.|Zdarzenie|Wystąpienie|
---|---|---|
|1|onabort|Występuje, gdy użytkownik przerywa ładowanie strony lub pliku multimedialnego.|
|2|onblur|Występuje, gdy użytkownik opuszcza obiekt HTML.|
|3|onchange|Występuje, gdy użytkownik zmienia lub aktualizuje wartość obiektu.|
|4|onclick|Występuje lub uruchamia się, gdy dowolny użytkownik kliknie element HTML.|
|5|ondblclick|Występuje, gdy użytkownik kliknie element HTML dwa razy razem.|
|6|onfocus|Występuje, gdy użytkownik skupia się na elemencie HTML. Ta procedura obsługi zdarzeń działa odwrotnie do onblur.|
|7|onkeydown|Uruchamia się, gdy użytkownik naciska klawisz na urządzeniu z klawiaturą. Ten program obsługi zdarzeń działa dla wszystkich kluczy.|
|8|onkeypress|Uruchamia się, gdy użytkownik naciska klawisz na klawiaturze. Ten program obsługi zdarzeń nie jest wyzwalany dla wszystkich kluczy.|
|9|onkeyup|Występuje, gdy użytkownik zwolni klawisz z klawiatury po naciśnięciu obiektu lub elementu.|
|10|onload|Występuje, gdy obiekt jest całkowicie załadowany.|
|11|onmousedown|Występuje, gdy użytkownik naciska przycisk myszy nad elementem HTML.|
|12|onmousemove|Występuje, gdy użytkownik przesuwa kursor na obiekt HTML.|
|13|onmouseover|Występuje, gdy użytkownik przesuwa kursor nad obiektem HTML.|
|14|onmouseout|Występuje lub uruchamia się, gdy wskaźnik myszy zostanie przesunięty poza element HTML.|
|15|onmouseup|Występuje lub wyzwala się, gdy przycisk myszy zostanie zwolniony nad elementem HTML.|
|16|onreset|Używany przez użytkownika do resetowania formularza.|
|17|onselect|Występuje po wybraniu treści lub tekstu na stronie internetowej.|
|18|onsubmit|Uruchamia się, gdy użytkownik kliknie przycisk po przesłaniu formularza.|
|19|onunload|Uruchamia się, gdy użytkownik zamyka stronę internetową.|

## Bibliografia

* [Dynamiczny HTML – Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

