{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Wirtualny plik kontaktowy",
  "description":"Poznaj format pliku VCF i interfejsy API, które mogą tworzyć i otwierać pliki VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik VCF?

VCF (Virtual Card Format) lub vCard to cyfrowy format plików służący do przechowywania informacji kontaktowych. Format jest szeroko stosowany do wymiany danych w popularnych aplikacjach do wymiany informacji. Większość systemów operacyjnych, takich jak Windows i MacOS, jest dostarczana z domyślnymi aplikacjami do tworzenia i otwierania tych plików. Pojedynczy plik VCF może zawierać informacje kontaktowe dla jednego lub wielu kontaktów. Plik VCF zwykle zawiera informacje, takie jak imię i nazwisko kontaktu, adres, numer telefonu, adres e-mail, urodziny, zdjęcia i dźwięk, oprócz wielu innych pól. Dzięki obsłudze klientów i usług pocztowych nie dochodzi do utraty danych podczas przesyłania kontaktów za pomocą formatu vCard. Typ nośnika dla formatu pliku VCF to text/vcard.

## Format pliku VCF

Pliki VCF są z natury tekstowe i są czytelne dla człowieka. Można je otwierać w edytorach tekstu, takich jak Notatnik w systemie Microsoft Windows i TextEdit w systemie MacOS. Jeśli jednak w pliku znajduje się obraz, nie pojawi się on w edytorze tekstu.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) zapewnia obsługę otwieranie plików VCF, a także konwertowanie do wielu innych formatów, takich jak popularny format [MSG](/pl/email/msg/). Format pliku VCF ulepszony z czasem od wersji 2.1 do 4.0, dodając szczegółowe informacje do formatu pliku. Format służy również do eksportowania kontaktów z telefonu, a następnie importowania ich na inne urządzenie.

{{< figure src="../VCF.png" alt="Format pliku VCF" >}}

### VCF 2.1 Przykład

Poniżej znajduje się przykład wersji 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### Przykład VCF 3.0

Poniżej znajduje się przykład wersji 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### Przykład VCF 4.0

Poniżej znajduje się przykład wersji 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Bibliografia

* [VCF – z Wikipedii](https://en.wikipedia.org/wiki/VCard)

