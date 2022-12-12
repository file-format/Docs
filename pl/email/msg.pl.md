{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSG - format wiadomości e-mail programu Microsoft Outlook",
  "description":"Poznaj format pliku MSG i interfejsy API, które mogą tworzyć i otwierać pliki MSG.",
  "linktitle" : "MSG",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik MSG?

MSG to format pliku używany przez [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) i Exchange do przechowywania wiadomości e-mail , kontakt, spotkanie lub inne zadania. Takie wiadomości mogą zawierać jedno lub więcej pól e-mail, z nadawcą, odbiorcą, tematem, datą i treścią wiadomości lub informacjami kontaktowymi, szczegółami spotkania i jedną lub kilkoma specyfikacjami zadań. Właściwości, które składają się na obiekt Message, w tym również są częścią pliku MSG. Plik MSG ma nagłówki, główną treść wiadomości i hiperłącza jako zwykły tekst ASCII. Pliki MSG są również odpowiednie z programami, które wymagają interfejsu programistycznego Microsoft Messaging Applications Programming Interface (MAPI).

## Struktura plików MSG

Format CFB_3 jest podstawą pliku MSG. Paradygmat opiera się na koncepcjach magazynów i strumieni, dość zbliżonych do katalogów i plików. Dlatego główną różnicą w tym pierwszym jest cała hierarchia spakowana w odrębny plik, zwany plikiem złożonym. Obiekty stanowią pliki komunikatów i składają się z pojedynczej właściwości lub jej kolekcji. Ta zdolność ułatwia aplikacjom przechowywanie skomplikowanych, ustrukturyzowanych danych w jednym pliku. Ten format określa również wiele magazynów, z których każdy reprezentuje obiekt Message jako główny składnik. Te magazyny zawierają pewną liczbę strumieni reprezentujących właściwość tego komponentu. Możliwe jest również zagnieżdżanie magazynu.

## Właściwości mapy

Na najwyższym poziomie pliku .msg magazyny zawierają strumienie, w których są przechowywane właściwości. Właściwości można podzielić w następujący sposób:

* Stałe właściwości długości
* Właściwości zmiennej długości
* Właściwości o wielu wartościach

Niezależnie od kategorii właściwość jest albo oznaczona, albo nazwana. Jednak odpowiednie informacje o mapowaniu są wymagane dla nazwanych właściwości określonych przez ich magazyn mapowania.

## Magazyny

Magazyny stanowią kluczowe komponenty obiektu Message. Format pliku MSG określa następujące magazyny:

## Struktura najwyższego poziomu

Obiekt komunikatu reprezentuje cały najwyższy poziom formatu pliku MSG. W zależności od typu, właściwości, liczby odbiorców i obiektów załączników, obiekt wiadomości może mieć różne przechowywanie strumieni w odpowiednim pliku .MSG.

### Relacje z innymi strukturami

Format pliku Msg ma następujące relacje z innymi strukturami:

* Podstawą formatu .msg jest plik złożony w formacie binarnym.
* W tym formacie używane są właściwości używane przez Message and Attachment Object Protocol.

## Scenariusze unikania formatów MSG

Obiekt komunikatu może być współużytkowany przez klientów lub magazyny komunikatów korzystające z systemu plików .msg. Istnieje kilka okoliczności, w których przechowywanie obiektu Message w formacie pliku .msg nie byłoby właściwe. Na przykład:

* W przypadku utrzymywania dużego niezależnego archiwum lepiej jest użyć w pełni funkcjonalnego formatu, w którym widoki mogą być renderowane z większą precyzją.
* Jeśli odbiorca jest nieznany, możliwe, że format nie jest obsługiwany przez odbiornik i może zostać dostarczona wiadomość prywatna lub nieistotna.

## Przykład pliku MSG

Aby zobaczyć, jak wygląda plik MSG, możesz pobrać [przykładowy plik MSG](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) i otworzyć na swoim komputera, aby wyświetlić jego zawartość.

## Bibliografia

* [[MS-OXMSG]: Format pliku Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

