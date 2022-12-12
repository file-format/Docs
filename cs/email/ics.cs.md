{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar File Format",
  "description":"Další informace o formátu souboru ICS a rozhraních API, která mohou vytvářet a otevírat soubory ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor ICS?

Internet Calendaring and Scheduling Core Object Specification (iCalendar) je internetový standard (RFC 2445) pro výměnu a nasazení kalendářových událostí a plánování. Formát iCalendar je interoperabilní, čímž zajišťuje výměnu informací kalendáře mezi uživateli s různými e-mailovými aplikacemi. iCalendar formátuje vstupní data jako Multipurpose Internet Mail Extensions (MIME) a usnadňuje výměnu objektů prostřednictvím různých přenosových protokolů. Těmito přenosovými protokoly mohou být SMTP, HTTP, asynchronní komunikace point-to-point a přenos po síti na základě fyzických médií.

iCalendar umožňuje uživatelům sdílet události, úkoly závislé na datu/čase a informace o volném čase prostřednictvím e-mailů ostatním uživatelům, kteří mohou odpovědět. Soubory iCalendar se ukládají pomocí přípon „.ics“, „.iCalendar“ nebo „.ifb“ s typem MIME „text/calendar“. iCalendar je udržován tak, aby byl soběstačný bez jakékoli závislosti na transportním protokolu. Webové servery (s protokolem HTTP) mohou přenášet informace iCalendar a webové stránky mohou obsahovat data iCalendar ve vložené podobě pomocí iCalendar.

## Stručná historie formátu souborů ICS

V roce 1998 Internet Engineering Task Force (IETF) definoval iCalendar jako standard (RFC 2445). Standard zdokumentovali Frank Dawson (Lotus Notes Corporation) a Derik Stenerson (Microsoft). V roce 2009 byl standard znovu zdokonalen Bernardem Desruisseauxem (Oracle) jako RFC 5545. Tentokrát byly přidány některé nové funkce a některé zastaralé funkce byly zastaralé. V roce 2016 byl vydán RFC 7986 a rozšířen na původní iCalendar RFC. RFC 7986 přidal nové vlastnosti do hlavního objektu VCALENDAR a byly také zavedeny nové podpůrné funkce pro konferenční systémy.

## Formát souboru ICS ##

Typ MIME používaný daty iCalendar je „text/calendar“. Výchozí znaková sada pro iCalendar je UTF-8, ale poskytnutím parametrů v MIME lze použít jinou znakovou sadu. Soubor iCalendar obsahuje sekce, mezi těmito sekcemi je „VCALENDAR“ globální sekce, která zapouzdřuje všechny ostatní sekce. Sekce VEVENT definuje události, VTODO uvádí seznam všech úkolů, VJOURNAL obsahuje položky deníku a VTIMEZONE specifikuje informace o časové zóně. více sekcí podobné kategorie je povoleno. U mnoha událostí může být v souboru iCalendar přítomno více sekcí VEVENT.

### Obsahové řádky ###

Objekty iCalendar jsou uspořádány do samostatných řádků textu „řádků obsahu“. V tomto formátu souboru ukončuje sekvence CRLF řádek, zatímco délka řádku je omezena na 75 oktetů bez zalomení řádku. Dlouhá datová položka může být rozdělena do mnoha řádků.

### Oddělovače seznamů a polí ###

Vlastnosti a parametry určují seznam hodnot, které jsou odděleny znakem ČÁRKA. Pro hodnoty parametrů založené na URI se používají řetězce v uvozovkách. Seznam parametrů lze sestavit podle hodnoty vlastnosti. Každý parametr vlastnosti v tomto seznamu musí být oddělen středníkem.

V seznamu hodnot STŘEDNÍK izoluje parametry vlastností a čárka samostatné hodnoty vlastností. Příklad je uveden níže:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Více hodnot

Některé vlastnosti mohou mít více hodnot. Jednoduché vygenerování nového řádku obsahu s názvem vlastnosti je základním pravidlem pro vlastnosti s více hodnotami. Pro jednu hodnotu s více jazykovými variacemi však nesmíte používat vlastnosti s více hodnotami.

### Binární obsah

V rámci objektu iCalendar může hodnota vlastnosti odkazovat na data binárního obsahu umístěná v externí entitě MIME pomocí URI. Inline binární obsah lze použít ve speciálních situacích s parametrem "ENCODING", kde aplikace potřebuje vyjádřit objekt iCalendar jako jedinou entitu. Následující příklad vysvětluje vlastnost "ATTACH" s odkazem na URI:

PŘÍLOHA: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Sada znaků

Ačkoli výchozí schéma znakové sady pro iCalendar je UTF-8, není specifikován žádný parametr vlastnosti, který by definoval znakovou sadu hodnoty vlastnosti. v MIME přenosech parametr "charset" MUSÍ být použit pro existující znakovou sadu.

## Reference

* [Specifikace základního objektu internetového kalendáře a plánování](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

