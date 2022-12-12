{
  "date" : "2019-10-11",
  "keywords" :["asax","plik asax", "format pliku asax", "typ pliku asax", "plik", "typ", "co to jest plik asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - plik aplikacji serwera ASP.NET",
  "description" :"Dowiedz się, co to jest plik ASAX i interfejsy API, które mogą tworzyć i otwierać pliki ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Czym jest plik ASAX?

Plik z rozszerzeniem .asax to plik używany przez aplikacje ASP.NET, który znajduje się po stronie serwera. Zawiera kod służący do reagowania na zdarzenia na poziomie aplikacji i sesji zgłaszane przez ASP.NET lub moduły HTTP. Obejmuje to również obsługę niektórych zdarzeń podczas uruchamiania lub zamykania aplikacji. Pliki ASAX są opcjonalne i tylko jeden plik ASAX jest dodawany do aplikacji internetowych w celu obsługi zdarzeń i błędów na poziomie aplikacji na poziomie globalnym. W przeciwieństwie do stron ASPX, pliki ASAX nie zawierają żadnego kodu realizującego funkcjonalność aplikacji.

## Format pliku ASAX

Pliki ASAX są zapisywane w formacie zwykłego pliku tekstowego i są czytelne dla człowieka. Najczęściej używanym plikiem ASAX jest Global.asax, który znajduje się w katalogu głównym aplikacji ASP.NET. Serwery WWW są skonfigurowane tak, aby odrzucały wszelkie połączenia przychodzące do tego pliku, aby uniemożliwić użytkownikom pobieranie lub wyświetlanie kodu tego pliku.

### Global.ASAX — przykład formatu pliku ASAX

Pojedynczy plik ASAX składa się z wielu sekcji napisanych w celu obsługi zdarzeń na poziomie aplikacji. Oto one.

* **Dyrektywy aplikacji** — dyrektywy aplikacji to znaczniki używane do definiowania opcjonalnych ustawień specyficznych dla aplikacji, które mają być używane przez parser ASP.NET podczas przetwarzania pliku Global.asax. Dyrektywy te znajdują się na początku pliku Global.asax i są zdefiniowane w następujący sposób.

```
<%@ dyrektywa atrybut=wartość [atrybut=wartość … ]%>
```
* **Bloki deklaracji kodu** — bloki deklaracji kodu są używane do definiowania sekcji kodu serwera, które są osadzone w plikach aplikacji ASP.NET w obrębie \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Bloki renderowania kodu** — definiują wbudowany kod lub wyrażenia, które są wykonywane podczas renderowania strony. Dwa style bloków renderowania kodu obejmują kod wbudowany i wyrażenia wbudowane. Pierwsza służy do definiowania samodzielnych linii lub bloków kodu, podczas gdy lateral służy jako skrót do wywołania metody Write.

## Bibliografia

* [Omówienie programów obsługi HTTP i modułów HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax Składnia](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

