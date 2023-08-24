{
  "date" : "2021-03-30",
  "keywords" :["PMLZ", "ZIP Palm Markup Language", "rozszerzenie", "Plik", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format pliku PMLZ, Palm Markup Language i interfejsy API, które mogą tworzyć i otwierać pliki PMLZ.",
  "title" :"PMLZ - spakowany plik języka znaczników dłoni",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Czym jest plik PMLZ?

Palm Inc wprowadził typ pliku eBook; znany jako format pliku PMLZ, który jest skompresowaną wersją formatu pliku [PML](/pl/ebook/pml/), dlatego pliki z rozszerzeniem .pmlz są znane jako **Zipped Palm Markup Language File**. Plik PMLZ to tylko kontener zip pliku, który kompiluje pliki [PDB](/pl/programming/pdb/) w celu utworzenia dokumentów dla **eReadera** (znanego jako urządzenie do czytania e-booków, takie jak tablet). Plik PML zawiera układ pliku PDB (zawierającego różne pliki danych) do wyświetlenia na urządzeniu Palm. Natomiast plik PDB jest plikiem bazy danych, który jest używany przez różne aplikacje, w tym Quicken, Pegasus, Microsoft Visual Studio i Palm Pilot. Krótko mówiąc, PMLZ to skompresowany kontener plików PML i PDB.


## Znajomość języka Palm Markup Language
Poniższa tabela przedstawia polecenia PML:

|Polecenie|Opis|
---|---|
| \ p | Nowa strona |
| \ x | Nowy rozdział; powoduje również nowy podział strony. Załącz tytuł rozdziału (i wszelkie kody stylów) za pomocą \x i \x |
| \Xn | Nowy rozdział, wcięcie n poziomów (n od 0 do 4 włącznie) w oknie dialogowym Rozdział; nie powoduje podziału strony. Dołącz tytuł rozdziału (i wszelkie kody stylów) za pomocą \Xn i \Xn |
| \Cn="Tytuł rozdziału" | Wstaw „Tytuł rozdziału” do listy rozdziałów z poziomem n (np. \Xn). Tekst nie jest wyświetlany na stronie i nie wymusza podziału strony. Czasami może to być przydatne, na przykład do wstawienia znacznika rozdziału na początku wprowadzenia do rozdziału. |
| \ c | Wyśrodkuj ten blok tekstu; zamknij za pomocą \c na początku linii |
| \ r | Wyrównaj do prawej blok tekstu; zamknij za pomocą \r na początku linii |
| \i| Blok kursywą; zamknij za pomocą \i |
| \ u | Podkreśl blok; zamknij za pomocą \u |
| \ o | blok overstrike; zamknij za pomocą \o |
| \ v | Niewidoczny tekst; zamknij za pomocą \v (można użyć do komentarzy) |
| \ t | Blok wcięcia. Zacznij od początku linii, zamknij \t na końcu linii |
| \T="50%" | Wcina określoną wartość procentową szerokości ekranu, w tym przypadku 50%. Jeśli bieżąca pozycja rysunku jest już poza określoną lokalizacją na ekranie, ten znacznik jest ignorowany. |
| \w="50%" | Osadź poziomą linię o określonej procentowej szerokości ekranu, w tym przypadku 50%. Ten tag powoduje podział linii przed i po nim. Reguła jest wyśrodkowana. Znak procentu jest obowiązkowy. |
| \ n | Przełącz na „normalną” czcionkę określoną przez użytkownika |
| \s | Przełącz na standardową czcionkę; zamknij za pomocą \s, aby powrócić do normalnej czcionki |
| \ b | Przełącz na pogrubioną czcionkę; zamknij za pomocą \b, aby powrócić do normalnej czcionki (przestarzałe; zamiast tego użyj \B) |
| \ l | Przełącz na dużą czcionkę; zamknij za pomocą \l, aby powrócić do normalnej czcionki |
| \B | Zaznacz tekst jako pogrubiony. W przeciwieństwie do tagu \b, \B nie zmienia czcionki, więc możesz mieć duży, pogrubiony tekst. Nie można mieszać \b i \B w tym samym pliku PML. |
| \ Sp | Oznacz tekst jako indeks górny. Nie należy mieszać z innymi stylami, takimi jak pogrubienie, kursywa itp. Tekst indeksu górnego należy dołączyć za pomocą \Sp. |
| \Sb | Oznacz tekst jako indeks dolny. Nie należy mieszać z innymi stylami, takimi jak pogrubienie, kursywa itp. Dołącz tekst indeksu dolnego za pomocą \Sb. |
| \ k | Umieść załączony tekst małymi literami; zamknij za pomocą \k. Wszystkie znaki zawarte w znacznikach \k (w tym te z akcentami) są zamieniane na wielkie i są renderowane w mniejszym rozmiarze punktowym niż zwykłe wielkie litery. |
| \\ | Reprezentuje pojedynczy ukośnik odwrotny |
| \aXXX | Wstaw znak inny niż ASCII, którego kodem Windows-1252 jest dziesiętny XXX. Szczegółowe informacje można znaleźć w tabeli znaków PML. |
| \UXXXX | Wstaw znak inny niż ASCII, którego kod Unicode to szesnastkowy XXXX. Szczegółowe informacje można znaleźć w rozszerzonej tabeli znaków PML. |
| \m="nazwaobrazu.png" | Wstaw nazwany obraz. Zobacz sekcję dotyczącą obrazów poniżej. |
| \q="#linkanchor"Jakiś tekst\q | Odwołaj się do zakotwiczenia łącza, które znajduje się w innym miejscu w dokumencie. Ciąg po specyfikacji zakotwiczenia i przed końcowym \q jest podkreślony lub w inny sposób pokazany jako łącze podczas przeglądania dokumentu. |
| \Q="powiązanie kotwicy" | Określ zakotwiczenie łącza w dokumencie. |
| \- | Wstaw miękki łącznik. Miękki łącznik pojawia się tylko wtedy, gdy konieczne jest przełamanie wyrazu w linii. |
| \Fn="przypis1"1\Fn | Połącz „1” z przypisem, którego nazwa to przypis 1, oznaczony na końcu dokumentu PML. Zobacz sekcję dotyczącą przypisów i pasków bocznych poniżej. |
| \Sd="pasek boczny1"Pasek boczny\Sd | Połącz tekst „Pasek boczny” z paskiem bocznym o nazwie sidebar1, oznaczonym na końcu dokumentu PML. Zobacz sekcję dotyczącą przypisów i pasków bocznych poniżej. |
| \ja | Oznacz jako element indeksu referencyjnego. Załącz element indeksu (i wszelkie kody stylów) za pomocą \I i \I.|


## Bibliografia

* [Palm Markup Language – MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [Czytnik elektroniczny — przez MobileRead](https://en.wikipedia.org/wiki/E-reader)

