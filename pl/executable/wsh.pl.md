{
  "date" : "2021-08-27",
  "keywords" :[ "plik wsh", "format pliku wsh", "co to jest plik wsh", "plik", "przykład wsh", "rozszerzenie pliku wsh", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku WSH i interfejsy API, które mogą tworzyć i otwierać pliki WSH.",
  "title" :"WSH - plik skryptu systemu Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## Czym jest plik WSZ?
Plik z rozszerzeniem .wsh zawiera właściwości i parametry dla określonego skryptu języka programowania, takiego jak VB lub VBS itp. Rzeczywistą potrzebą WSH jest wykorzystanie ich do dostosowania wykonywania niektórych skryptów. Do uruchomienia wymagany jest język WScript lub CScript, który jest zawarty w systemie operacyjnym Windows. Pliki WSH były początkowo dostarczane w systemie Windows 95 na dyskach instalacyjnych jako opcjonalne konfigurowalne i możliwe do zainstalowania w Panelu sterowania, a następnie jako domyślny składnik systemu Windows 98.

## Format pliku WSH
WSH (Windows Script Host) może być używany do różnych celów, w tym do administracji, skryptów logowania i ogólnej automatyzacji. WSH ustanawia środowisko do uruchamiania skryptów. wywołuje odpowiedni silnik skryptowy i przydziela zestaw usług i obiektów, z którymi skrypt ma pracować. Skrypty te można uruchamiać w trybie GUI, z obiektu COM lub w trybie wiersza poleceń, zapewniając użytkownikowi elastyczność zarówno w przypadku skryptów interaktywnych, jak i nieinteraktywnych.

### Przykłady
Oto bardzo prosty przykład, który pokazuje skrypt VBScript, który używa głównego obiektu WSH COM „WScript” do wyświetlenia komunikatu z przyciskiem „OK”. Kiedy ten skrypt zostanie uruchomiony, zostanie wywołany silnik CScript lub WScript i zostanie ustanowione środowisko wykonawcze.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Bibliografia

* [Host skryptów systemu Windows – według Wikipedii](https://en.wikipedia.org/wiki/Windows_Script_Host)



