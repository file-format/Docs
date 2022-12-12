{
  "date" : "2021-07-13",
  "keywords" :["CFM", "rozszerzenie", "plik", "format", "system", "Cold Fusion Markup Language", "język", "strony internetowe CFM", "silnik CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - znaczniki zimnej fuzji",
  "description":"Poznaj format pliku CFM i interfejsy API, które mogą tworzyć i otwierać pliki CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Czym jest plik CFM? ##

Strony internetowe i pliki używane w **Cold Fusion Markup Language** zawierają rozszerzenia CFM i nazywane są stronami internetowymi CFM. Ten język skryptowy do tworzenia stron internetowych działa w Google App Engine, .NET Framework i JVM. Może zawierać język programowania lub kod języka. Gdy użytkownik uzyskuje dostęp do którejkolwiek z jego stron, serwer sieciowy ColdFusion wykonuje tę czynność. CFScript (który jest zbliżony do JavaScript) lub znaczniki mogą być używane do pisania CFML. CFML może być używany do generowania innych języków oprócz [HTML](/pl/web/html/), takich jak [CSS](/pl/web/css/), [JavaScript](/pl/web/js/), [XML](/pl/web/ xml/) i nie tylko.

Użycie tego języka i obsługiwanych przez niego tagów dotyczy głównie tworzenia dynamicznych aplikacji internetowych. Pliki można uruchamiać bezpośrednio w przeglądarce online, jeśli podczas korzystania z platformy rozwoju aplikacji w trybie offline wystąpi jakikolwiek błąd.
 

CFML działa w taki sposób, że określone rozszerzenia plików serwera (.cfc, .cfm) są przekazywane do przetwarzania w silniku CFML. Jeśli silniki są oparte na Javie, jest to realizowane za pomocą serwletów Javy. Silnik CFML przetwarza tylko funkcje i znaczniki oraz zwraca funkcje i tekst poza znacznikami CFML do serwera WWW bez żadnych zmian.


## Krótka historia ##

W 1995 roku została po raz pierwszy stworzona przez korporację o nazwie Allaire. W 2005 roku przejął ją Adobe i do dziś świadczy usługi w zakresie rozwoju ColdFusion. Przez lata był rozwijany i ulepszany przez wiele osób i firm. W 2012 roku została uruchomiona fundacja o nazwie OpenCFML. Później, w 2015 roku były Railo świadczył swoje usługi w celu poprawy wydajności CFM i zmniejszył zasoby, aby uzyskać lepszą funkcjonalność. Jego najnowsza aktualizacja została uruchomiona w 2020 roku i ma być kontynuowana do 2028 roku.

## Format pliku CFM ##

Kod plików CFM i stron internetowych zawiera głównie znaczniki takie jak HTML, ale z niewielką różnicą. Pliki te są odpowiedzialne za wykonywanie różnych operacji, które umożliwiają uruchamianie skryptów ColdFusion.
* Dostęp do tych plików można uzyskać i uruchomić bezpośrednio w systemie Windows i macOS za pomocą przeglądarki dowolnego systemu operacyjnego.
* Adobe ColdFusion zapewnia platformę do tworzenia stron internetowych i dynamicznych aplikacji na PC.
* Dowolny edytor tekstu, taki jak Notatnik lub inny edytor tekstu w systemie operacyjnym, może być używany do otwierania tych plików, ponieważ pliki te są oparte na tekście.
* Kiedy dowolny plik CFM jest otwierany w edytorze tekstu, wyświetla kod składający się ze znaczników i skryptów, których nikt nie zrozumiałby, gdyby nie był programistą stron internetowych.

## Przykład użycia CFM ##

Poniżej przedstawiono prosty przykład użycia pliku CFM.

### Dokument CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Bibliografia ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

