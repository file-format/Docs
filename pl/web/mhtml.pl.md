{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","plik mhtml", "format pliku mhtml", "typ pliku mhtml", "plik", "typ", "co to jest plik mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - Plik MIME HTML",
  "description":"Poznaj format pliku MHTML i interfejsy API, które mogą tworzyć i otwierać pliki MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik MHTML?

Pliki z rozszerzeniem MHTML reprezentują format archiwum strony internetowej, który może być tworzony przez wiele różnych aplikacji. Format ten nazywany jest formatem archiwum, ponieważ zapisuje internetowy kod **[HTML](/pl/web/html/)** i powiązane zasoby w jednym pliku. Zasoby te obejmują wszystko, co jest powiązane ze stroną internetową, takie jak obrazy, aplety, animacje, pliki audio i tak dalej. Pliki MHTML można otwierać w różnych aplikacjach, takich jak Internet Explorer i Microsoft Word. Microsoft Windows używa formatu pliku MHTML do rejestrowania scenariuszy problemów zaobserwowanych podczas korzystania z dowolnej aplikacji w systemie Windows, która powoduje problemy. Format pliku MHTML koduje zawartość strony podobnie do specyfikacji zdefiniowanych w komunikacie/rfc822, który jest specyfikacją związaną z wiadomościami e-mail w postaci zwykłego tekstu. Rzeczywiste specyfikacje formatu są wyszczególnione w [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Format pliku MHTML

MHTML jest również znany jako MIME Encapsulation of Aggregate HTML Documents ze względu na możliwość kodowania stron internetowych HTML wraz z zasobami w jednym archiwum internetowym. Zgodnie ze specyfikacją RFC 2557 dokument zbiorczy to wiadomość zakodowana w formacie MIME, która zawiera główny zasób (obiekt) oraz inne zasoby powiązane z nim za pomocą identyfikatorów URI. Takimi innymi zasobami mogą być reprezentacje wbudowanych obrazów, arkuszy stylów, apletów itp. Ponadto mogą to być źródła innych dokumentów multimedialnych. Pełne specyfikacje dokumentów dla formatu pliku MHTML są wyszczególnione w [RFC 2557](https://tools.ietf.org/html/rfc2557) i należy się do nich odnieść w przypadku wszelkiego rodzaju tworzenia aplikacji do odczytu/zapisu tego formatu pliku. Norma określa, że części ciała, do których mają się odnosić, można zidentyfikować za pomocą identyfikatora treści lub lokalizacji zawartości.

### Nagłówki treści MIME

Nagłówek treści MIME, Content-Location, jest zdefiniowany w celu rozpoznawania odniesień URI do zasobów w innych częściach ciała. Ten nagłówek może wystąpić w dowolnej wiadomości lub nagłówku treści.

### Nagłówek lokalizacji zawartości

Lokalizacja zawartości to reprezentacja URI, która oznacza zawartość części ciała, w której się znajduje. Jego wartością może być bezwzględny lub względny identyfikator URI. Można go użyć do oznaczenia zasobu, którego nie mogą odzyskać niektórzy lub wszyscy odbiorcy wiadomości. Pojedyncza wiadomość może mieć tylko jeden nagłówek Content-Location. Przykład struktury wieloczęściowej/powiązanej zawierającej części ciała z etykietami Content-Location i Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI agregatów MHTML

Identyfikator URI agregatu MHTML jest inny niż identyfikator URI głównego elementu. Pole nagłówka Content-Location powinno dotyczyć całego agregatu, jeśli jest użyte w nagłówku wieloczęściowego/powiązanego nagłówka. Podobnie zestaw pobranych zasobów może różnić się od zestawu zasobów pobranych przy użyciu lokalizacji zawartości jego części, gdy do pobrania tego agregatu używany jest identyfikator URI odnoszący się do agregatu MHTML. Na przykład pobranie agregatu MHTML może zwrócić starą wersję, podczas gdy pobranie głównego identyfikatora URI i powiązanych z nim obiektów w wierszu może zwrócić nowszą wersję.

## Bibliografia

* [Enkapsulacja MIME dokumentów zbiorczych — RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Format pliku MHTML – według Wikipedii](https://en.wikipedia.org/wiki/MHTML)

