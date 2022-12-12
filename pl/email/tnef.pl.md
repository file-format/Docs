{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TNEF",
  "description":"Poznaj format pliku TNEF i interfejsy API, które mogą tworzyć i otwierać pliki TNEF.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik TNEF?

Transport Neutral Encapsulation Format (TNEF) jest zastrzeżonym formatem firmy Microsoft, służącym do enkapsulacji załączników do wiadomości e-mail w oparciu o interfejs programowania aplikacji Messaging Application Programming Interface (**MAPI**). Microsoft Outlook i Microsoft Exchange Server w pełni obsługują TNEF, a później dekodują TNEF do MAPI i wyświetlają sformatowane wiadomości. Załącznik wiadomości e-mail z kodowaniem TNEF ma typ MIME MS-TNEF i jest przechowywany jako winmail/win.dat. Załącznik w pliku winmail .dat zawiera następujące informacje:


|Wiadomość|Obiekty OLE|Funkcje programu Outlook
---|---|---|
|<ul><li> Oryginalne załączniki wiadomości</li><li> Oryginalna wersja sformatowana</li><li> czcionki, rozmiary tekstu i kolory tekstu</li></ul> |<ul><li> osadzone zdjęcia</li><li> osadzone dokumenty pakietu Office</li></ul> |<ul><li> formularze niestandardowe</li><li> przyciski do głosowania</li><li> prośby o spotkanie</li></ul>


Inne usługi e-mail, które nie obsługują formatu TNEF, wyświetlają zwykły tekst wiadomości w formacie TNEF. Outlook osadza bogaty format wiadomości w plikach TNEF (OLE) lub w określonych funkcjach Outlooka (formularze, przyciski sondowania i wezwania konferencyjne). Sankcjonowanie jawnego kodowania TNEF w kliencie poczty e-mail programu Outlook nie jest możliwe, jednak wybranie formatu RTF do wysyłania wiadomości e-mail pośrednio ułatwia kodowanie TNEF.

## Format pliku TNEF

Algorytm danych TNEF ustanawia spłaszczoną strukturę na podstawie bogatych, hierarchicznych właściwości wiadomości. Te spłaszczone struktury są następnie używane do reprezentowania strumienia danych szeregowych złożonego z określonych właściwości.

W niektórych sytuacjach, gdy właściwości występują w grupach lub mają wiele wartości, strumień może zawierać liczniki i dopełnienia, aby wymusić określone wyrównania danych. Charakterystyczna sytuacja, w której użycie tego algorytmu jest korzystne, występuje w nieobsługiwanym środowisku przesyłania wiadomości. W takich środowiskach bogata właściwość komunikatu jest kodowana w strumieniu danych szeregowych przez program zapisujący TNEF. Ponadto właściwości, które nie należą do podstawowego pliku TNEF, mogą zostać zamknięte podczas transmisji. Te hermetyzowane właściwości są następnie udostępniane przez dekodowanie za pomocą formatu TNEF, aby zapewnić dostępność wszystkich właściwości oryginalnej wiadomości dla aplikacji klienckiej.

W formacie TNEF wszystkie numeryczne typy danych są typu little-endian, a ich rozmiar jest większy niż jeden bajt. Obsługa tych wartości liczbowych na platformach innych niż little-endian wymaga wykonania odpowiednich przekształceń w celu uzyskania poprawnych wartości. Wartości ciągu są reprezentowane w formacie Augmented Backus-Naur Form (ABNF) zgodnie ze specyfikacjami [RFC5234]. Gdy łańcuch kończy się znakiem null, jest on również uwzględniany; na przykład „pracownik@próbka.com” %x00.

{{< figure src="../TNEF.png" alt="Format pliku TNEF" >}}

## Atrybuty TNEF i reguły przetwarzania ##

Strumień danych w formacie TNEF zaczyna się od starszego numeru wersji, podpisu, pierwotnej wartości klucza i atrybutu reprezentującego stronę kodową. Ta strona kodowa jest generowana, gdy koder rejestruje atrybuty i właściwości ANSI. Następnie strumień stał się serią atrybutów, w których najpierw umieszczano atrybuty wiadomości, a następnie atrybuty załączników. Różne właściwości wiadomości i załączników są zawarte w atrybutach specjalnych, takich jak attMsgProps, attAttachment i attRecipTable. Atrybuty pojawiające się w strumieniu TNEF zawierają strukturę, właściwości komunikatu i konwersje niezbędne do połączenia ich z właściwościami komunikatu. Każdy atrybut składa się z identyfikatora, rozmiaru i danych atrybutu, sumy kontrolnej i poziomu zgodnie z jego zastosowaniem.

## Związek z protokołami i innymi algorytmami ##

Systemy, które mają słaby mechanizm wyświetlania bogatego formatu wiadomości, natywnie potrzebują algorytmu danych TNEF do transportu. Używając nośnika typu ms-TNEF, wyjście algorytmu składa się z pliku załącznika (winmail.dat) i części ciała MIME określonej w [RFC2045]. Treść wiadomości w postaci zwykłego tekstu jest przesyłana przy użyciu kodu UUENCODE zgodnie ze specyfikacją [MSDN-UAF] i ta treść wiadomości lub równoważna metoda jest dekodowana po stronie odbiorcy. Co więcej, TNEF może przesyłać dane wiadomości za pomocą różnych protokołów internetowych, takich jak SMTP, POP3, IMAP4, a także zintegrować MIME zgodnie ze standardem RFC2045.

## Oświadczenie o zastosowaniu ##

Poza prostą transmisją komunikatów, oryginalna aplikacja TNEF miała powstać w celu wykorzystania klas komunikatów i obsługi dodatkowych funkcji, które nie mają oryginalnego wsparcia w protokole transportowym. Ta aplikacja została dodatkowo udoskonalona pod kątem przesyłania bogatych właściwości komunikatów i nazwanych właściwości, z których obecnie korzystają współcześni klienci do przesyłania wiadomości. Aby zapewnić zgodność z oryginalną implementacją, zachowana jest oryginalna składnia atrybutu, a specjalny atrybut przechowuje oddzielnie właściwości nowego komunikatu.

## Bibliografia

* [Transport Neutral Encapsulation Format](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Adresy e-mail i książki adresowe w Exchange Server](https://docs.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: algorytm danych Transport Neutral Encapsulation Format (TNEF)](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

