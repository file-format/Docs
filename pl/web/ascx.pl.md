{
  "date" : "2019-10-11",
  "keywords" :[ "ascx","plik ascx", "format pliku ascx", "typ pliku ascx", "plik", "typ", "co to jest plik ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku ASCX",
  "description" :"Dowiedz się, czym jest plik ASCX i interfejsy API, które mogą tworzyć i otwierać pliki ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik ASCX?

Plik z rozszerzeniem .ascx to formant użytkownika używany jako składnik wielokrotnego użytku na stronach internetowych. Odwołuje się do niego w dowolnej witrynie ASP, przeciągając go z pola kontrolnego na stronę. Kontrolki użytkowników ASCX są dodawane do projektu jako centralne źródło, co powoduje, że każda zmiana w kontrolce użytkownika jest odzwierciedlana w całej witrynie. W przeciwieństwie do plików ASMX, które definiują mechanizm komunikacji w ramach 2 obiektów przez Internet, pliki ASCX są kontrolkami użytkownika do osadzania na stronach lub w witrynie.

## Format pliku ASCX

Pliki ASCX są zapisywane w formacie zwykłego tekstu i mogą używać kodu za funkcjami, takimi jak strony internetowe, które kończą się na .ascx.cs. Kod znaczników kontrolek użytkownika zaczyna się od dyrektywy @Control, jak pokazano w poniższym przykładzie.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Ta kontrola użytkownika sieci Web może być ponownie używana na wielu stronach, takich jak stopka strony, nagłówek lub jakiś rodzaj nawigacji w witrynie. Kontrolki użytkownika sieci Web mają właściwości, metody i zdarzenia, jak każdy inny kontroler, co czyni je użytecznymi w ustawianiu ich zachowania wizualnego.

### Przykład rejestrowania kontrolek użytkownika w pliku web.config

Aby używać jednego elementu sterującego użytkownika na wielu stronach, element sterujący sieci Web można zarejestrować w pliku web.config. Pozwala to na korzystanie z kontroli nad całym serwisem zamiast rejestrowania się na każdej stronie z osobna. Poniższy przykładowy kod definiuje sposób rejestrowania kontrolki internetowej w web.config, która ma być wyświetlana jako stopka w całej witrynie internetowej.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Bibliografia

* [ASCX vs ASMX](https://forums.asp.net/t/1838934.aspx?How+to+work+with+ascx+files+)
* [Kontrola użytkownika ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

