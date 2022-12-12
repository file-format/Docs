{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - format pliku iCalendar",
  "description":"Poznaj format pliku ICS i interfejsy API, które mogą tworzyć i otwierać pliki ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik ICS?

Internet Calendaring and Scheduling Core Object Specification (iCalendar) to internetowy standard (RFC 2445) służący do wymiany i wdrażania wydarzeń w kalendarzu oraz planowania. Format iCalendar jest interoperacyjny, zapewniając w ten sposób wymianę informacji kalendarza między użytkownikami posiadającymi różne aplikacje pocztowe. iCalendar formatuje dane wejściowe jako Multipurpose Internet Mail Extensions (MIME) i ułatwia wymianę obiektów za pośrednictwem różnych protokołów transportowych. Tymi protokołami transportowymi mogą być SMTP, HTTP, komunikacja asynchroniczna typu punkt-punkt oraz transport sieciowy oparty na nośnikach fizycznych.

iCalendar umożliwia użytkownikom udostępnianie wydarzeń, zadań zależnych od daty/godziny oraz informacji wolny/zajęty za pośrednictwem wiadomości e-mail innym użytkownikom, którzy mogą odpowiedzieć. Pliki iCalendar przechowują przy użyciu sufiksów „.ics”, „.iCalendar” lub „.ifb” z typem MIME „text/calendar”. iCalendar jest samowystarczalny, bez zależności od protokołów transportowych. Serwery internetowe (z protokołem HTTP) mogą przesyłać informacje iCalendar, a strony internetowe mogą zawierać dane iCalendar w formie osadzonej za pomocą iCalendar.

## Krótka historia formatu pliku ICS

W 1998 roku Internet Engineering Task Force (IETF) zdefiniował iCalendar jako standard (RFC 2445). Standard został udokumentowany przez Franka Dawsona (Lotus Notes Corporation) i Derika Stenersona (Microsoft). W 2009 roku standard został ponownie udoskonalony przez Bernarda Desruisseaux (Oracle) jako RFC 5545. Tym razem dodano kilka nowych funkcji, a niektóre przestarzałe funkcje zostały wycofane. W 2016 roku RFC 7986 został wydany i rozszerzony do oryginalnego iCalendar RFC. RFC 7986 dodał nowe cechy do głównego obiektu VCALENDAR, a także wprowadzono nowe funkcje pomocnicze dla systemów konferencyjnych.

## Format pliku ICS ##

Typ MIME używany przez dane iCalendar to „text/calendar”. Domyślny zestaw znaków dla iCalendar to UTF-8, jednak podając parametry w MIME, można użyć innego zestawu znaków. Plik iCalendar zawiera sekcje, wśród których „VCALENDAR” to sekcja globalna obejmująca wszystkie inne sekcje. Sekcja VEVENT definiuje wydarzenia, VTODO zawiera listę wszystkich rzeczy do zrobienia, VJOURNAL zawiera wpisy do dziennika, a VTIMEZONE określa informacje o strefie czasowej. dozwolone jest wiele sekcji o podobnej kategorii. W przypadku wielu wydarzeń w pliku iCalendar może znajdować się wiele sekcji VEVENT.

### Wiersze treści ###

Obiekty iCalendar są ułożone w odrębne linie tekstu „linii treści”. W tym formacie pliku sekwencja CRLF kończy linię, podczas gdy długość linii jest ograniczona do 75 oktetów z wyłączeniem końca linii. Długi element danych może obejmować wiele wierszy.

### Separatory list i pól ###

Właściwości i parametry określają listę wartości oddzielonych znakiem PRZECINKA. Ciągi w cudzysłowie są używane dla wartości parametrów opartych na URI. Listę parametrów można zbudować według wartości właściwości. Każdy parametr właściwości na tej liście musi być oddzielony ŚREDNIKIEM.

Na liście wartości parametry właściwości izoluje ŚREDNIK, a wartości właściwości rozdziela PRZECINEK. Przykład podano poniżej:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Wiele wartości

Niektóre właściwości mogą mieć wiele wartości. Proste wygenerowanie nowej linii zawartości z nazwą właściwości jest podstawową zasadą dla właściwości wielowartościowych. Jednak w przypadku pojedynczej wartości z wieloma odmianami językowymi nie należy używać właściwości wielowartościowych.

### Zawartość binarna

W obiekcie iCalendar wartość właściwości może odwoływać się do danych zawartości binarnej umieszczonych w zewnętrznej jednostce MIME przy użyciu identyfikatora URI. Wbudowana zawartość binarna może być używana w szczególnych sytuacjach z parametrem „KODOWANIE”, gdzie aplikacja musi wyrazić obiekt iCalendar jako samodzielną całość. Poniższy przykład wyjaśnia właściwość „ADTACH” z odwołaniem do identyfikatora URI:

ZAŁĄCZ: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Zestaw znaków

Chociaż domyślnym schematem znaków dla iCalendar jest UTF-8, to jednak żaden parametr właściwości nie jest określony w celu zdefiniowania zestawu znaków dla wartości właściwości. w transferach MIME parametr "charset" MUSI być użyty dla istniejącego zestawu znaków.

## Bibliografia

* [Specyfikacja podstawowego obiektu kalendarza internetowego i planowania] (https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

