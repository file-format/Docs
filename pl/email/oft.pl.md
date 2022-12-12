{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFT - plik szablonu wiadomości e-mail programu Microsoft Outlook",
  "description":"Poznaj format plików OFT i interfejsy API, które mogą tworzyć i otwierać pliki OFT.",
  "linktitle" : "OFT",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik OFT?

Pliki z rozszerzeniem .oft to pliki szablonów tworzone za pomocą programu Microsoft Outlook. Wstępnie sformatowany zestaw szablonów wiadomości jest następnie używany do wysyłania wiadomości e-mail ze wspólnymi informacjami w celu zaoszczędzenia czasu. Takie pliki można wygenerować, tworząc nową wiadomość e-mail, dodając niezbędne informacje, a następnie korzystając z listy rozwijanej Zapisz jako szablon pakietu Office (.oft) w programie Microsoft Outlook. Użytkownicy mogą otwierać pliki OFT, klikając je dwukrotnie, a otworzy się w powiązanej aplikacji w tym konkretnym systemie.

## Struktura plików OFT ##

Format pliku .OFT bazuje na formacie pliku [MSG](/pl/email/msg/). Jedyną różnicą jest to, że pliki OFT mają CLSID_TemplateMessage ({0006F046-0000-0000-C000-000000000046}) jako klasę przechowywania (WriteClassStg), podczas gdy pliki MSG używają CLSID_MailMessage ({00020D0B-0000-0000-C000-000000000046}).

Format CFB_3 jest podstawą pliku MSG. Paradygmat opiera się na koncepcjach magazynów i strumieni, dość zbliżonych do katalogów i plików. Dlatego główną różnicą w tym pierwszym jest cała hierarchia spakowana w odrębny plik, zwany plikiem złożonym. Obiekty stanowią pliki komunikatów i składają się z pojedynczej właściwości lub jej kolekcji. Ta zdolność ułatwia aplikacjom przechowywanie skomplikowanych, ustrukturyzowanych danych w jednym pliku. Ten format określa również wiele magazynów, z których każdy reprezentuje obiekt Message jako główny składnik. Te magazyny zawierają pewną liczbę strumieni reprezentujących właściwość tego komponentu. Możliwe jest również zagnieżdżanie magazynu.

### Właściwości OFT

Na najwyższym poziomie pliku .msg magazyny zawierają strumienie, w których są przechowywane właściwości. Właściwości można podzielić w następujący sposób:

* Stałe właściwości długości
* Właściwości zmiennej długości
* Właściwości o wielu wartościach

Niezależnie od kategorii właściwość jest albo oznaczona, albo nazwana. Jednak dla nazwanych właściwości wymagane są odpowiednie informacje o mapowaniu, zgodnie z ich pamięcią mapowania.

### Magazyny OFT

Magazyny stanowią kluczowe komponenty obiektu Message. Format pliku MSG określa następujące magazyny:

### Struktura najwyższego poziomu

Obiekt komunikatu reprezentuje cały najwyższy poziom formatu pliku Msg. W zależności od typu, właściwości, liczby odbiorców i obiektów załączników, obiekt wiadomości może mieć różne przechowywanie strumieni w odpowiednim pliku .MSG.

#### Relacje z innymi strukturami

Format pliku MSG/OFT ma następujące relacje z innymi strukturami:

* Podstawą formatu .msg jest plik złożony w formacie binarnym.
* W tym formacie używane są właściwości używane przez Message and Attachment Object Protocol.

## Bibliografia

* [[MS-OXMSG]: Format pliku Outlook MSG](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)

