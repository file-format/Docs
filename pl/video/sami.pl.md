{
"data": "2023-05-16",
  "keywords": [
"sami plik",
"co to jest plik sami",
"przykład pliku sami",
"plik",
"sami rozszerzenie pliku",
"rozszerzenie"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format pliku SAMI - plik wymiany napisów i metadanych",
  "description":"Dowiedz się o formacie SAMI i interfejsach API, które umożliwiają tworzenie i otwieranie plików SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
}
},
"lastmod": "16.05.2023"
}

## Czym jest plik SAMI?

Plik z rozszerzeniem ".sami" zazwyczaj odnosi się do pliku wymiany napisów i metadanych (SAMI). SAMI to format napisów używany do wyświetlania napisów w filmach. Został pierwotnie opracowany przez firmę Microsoft dla ich programu Windows Media Player.

Pliki SAMI zawierają informacje o czasie i treść tekstową napisów lub napisów kodowanych, umożliwiając ich synchronizację z odtwarzaniem wideo. Format obsługuje podstawowe opcje formatowania, takie jak styl czcionki, kolor i położenie napisów na ekranie.

Pliki SAMI to zwykle zwykłe pliki tekstowe, które można otwierać i edytować za pomocą edytora tekstu. Zawartość pliku SAMI zazwyczaj zawiera sekcję nagłówka zawierającą informacje o pliku, po której następują poszczególne wpisy napisów z odpowiednim czasem i tekstem.

Oto przykład tego, jak może wyglądać plik SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Pliki SAMI są powszechnie używane w połączeniu z odtwarzaczami wideo lub odtwarzaczami multimedialnymi obsługującymi wyświetlanie napisów, takimi jak Windows Media Player lub VLC Media Player. Odtwarzacz odczytuje plik SAMI i synchronizuje napisy z treścią wideo, umożliwiając widzom czytanie napisów podczas oglądania wideo.

## Obsługiwane tagi HTML

Pliki SAMI (Subtitles And Metadata Interchange) obsługują ograniczony zestaw znaczników przypominających HTML do formatowania i stylizacji napisów. Oto niektóre z powszechnie używanych tagów obsługiwanych przez SAMI:

- ``<SAMI> :`` Element główny hermetyzujący cały plik SAMI.
- ``<HEAD> :`` Zawiera informacje o nagłówku pliku SAMI.
<html>- ``<TITLE> :`` Określa tytuł pliku SAMI. </html>
- ``<BODY> :`` Zawiera wpisy napisów i informacje o ich czasie.
- ``<SYNC> :`` Reprezentuje punkt synchronizacji wpisu napisów. Określa moment, w którym napisy powinny być wyświetlane.
- ``<P> :`` Zawiera rzeczywistą treść napisów. Zwykle jest używany w obrębie a<SYNC> blok.
<html>- `` <FONT>:`` Określa właściwości czcionki dla załączonego tekstu. Atrybuty takie jak Kolor, Twarz, Rozmiar i Styl mogą służyć do modyfikowania wyglądu czcionki.</font>
- ``<BR> :`` Wstawia podział wiersza w napisach.
<html>- `` <B>:`` Wyświetla pogrubiony tekst.</b>
<html>- `` <I>:`` Wyświetla załączony tekst kursywą.</i>
<html>- `` <U>:`` Wyświetla podkreślony tekst.</u>
- ``<C> :`` Określa położenie lub wyrównanie tekstu napisów na ekranie. Obsługuje atrybuty takie jak Środek, Środek, Lewo, Prawo, Góra, Dół i ich kombinacje.
- ``<LANG> :`` Określa kod języka napisów. Pomaga w identyfikacji języka napisów.

Oto niektóre z podstawowych tagów obsługiwanych przez pliki SAMI. Należy pamiętać, że SAMI nie obsługuje pełnego zakresu znaczników i atrybutów HTML. Obsługiwane tagi skupiają się przede wszystkim na stylizacji i pozycjonowaniu napisów, a nie na zapewnianiu rozbudowanej struktury dokumentu lub interaktywności.

## Bibliografia
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

