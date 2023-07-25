{
  "date" : "2019-10-11",
  "keywords" :["asmx","plik asmx", "format pliku asmx", "typ pliku asmx", "plik", "typ", "co to jest plik asmx"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - plik usługi internetowej ASP.NET",
  "description" :"Dowiedz się, co to jest plik ASMX i interfejsy API, które mogą tworzyć i otwierać pliki ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Czym jest plik ASMX?

Plik z rozszerzeniami .asmx to plik usługi sieci Web ASP.NET, który zapewnia komunikację między dwoma obiektami przez Internet przy użyciu protokołu SOAP (Simple Object Access Protocol). Jest wdrażany jako usługa na serwerze sieci Web z systemem Windows w celu przetwarzania przychodzących żądań i zwracania odpowiedzi. W przeciwieństwie do plików [ASPX](/pl/web/aspx/), które zawierają kod do wizualnego wyświetlania stron internetowych ASP.NET, pliki ASMX działają na serwerze w tle i wykonują różne zadania, takie jak łączenie się z bazą danych, pobieranie danych i zwracanie ich w format, w jakim żądanie zostało złożone. Są one używane w szczególności w usługach sieciowych XML.

## Format pliku ASMX

Pliki ASMX są w formacie zwykłego tekstu i można je otwierać lub edytować w aplikacjach, takich jak Microsoft Visual Studio lub edytory tekstu. Jest to zastrzeżony format plików firmy Microsoft i ma dobrze zdefiniowaną składnię do tworzenia usług internetowych. Odpowiedź z pliku ASMX w postaci SOAP XML zawiera następujące elementy.

* `Envelop` — element główny, który identyfikuje dokument XML jako komunikat SOAP.
* `Header` — opcjonalny element zawierający informacje specyficzne dla aplikacji, takie jak dane uwierzytelniające. Jeśli obecny jest element Header, musi to być pierwszy element podrzędny elementu Envelope.
* `Body` - Zawiera wiadomość SOAP przeznaczoną dla odbiorcy.
* `Fault` — opcjonalny element używany do wskazywania komunikatów o błędach. Jeśli element Fault jest obecny, musi być elementem podrzędnym elementu Body.

Pliki ASMX można pisać w językach .NET, takich jak [C#](/pl/programming/cs/), [Visual Basic](/pl/programming/vb/) lub JScript.

## Czym różni się ASMX od ASPX i ASCX?

Pliki ASMX różnią się od plików ASPX i ASCX.

* Pliki ASPX, Active Server Pages to pliki programistyczne generowane przy użyciu platformy Microsoft ASP.NET działającej na serwerach WWW. Są one renderowane w przeglądarce internetowej klienta, gdy użytkownik żąda dostępu do takiej strony.
* ASCX, Active Server User Control, definiuje kontrolki użytkownika, które są używane do definiowania kontrolek wielokrotnego użytku na stronach internetowych ASP.NET lub w całej witrynie.

## Bibliografia

* [Korzystanie z usługi ASMX](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Kontrola użytkownika ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

