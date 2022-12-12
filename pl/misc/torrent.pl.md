{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku Torrent - Plik BitTorrent",
  "description":"Dowiedz się o plikach TORRENT i interfejsach API, które mogą tworzyć i otwierać pliki TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Co to jest plik TORRENT?

Plik TORRENT to plik tekstowy używany przez BitTorrent i inne programy P2P (peer-to-peer) do pobierania i wymiany treści. Zawartość do pobrania może obejmować dokumenty, filmy, gry, filmy i inne media dostępne w Internecie. Zawiera metadane dotyczące zawartości i lokalizacji pobieranych multimediów. Oprogramowanie takie jak BitTorrent wykorzystuje informacje z tego pliku, takie jak nazwa, rozmiar pliku i struktura folderów do pobierania danych. Pliki torrent można konwertować online na inne formaty plików, takie jak [PDF](/pl/pdf/).

## Co to jest torrentowanie? Format pliku TORRENT do wymiany danych

Torrenting to koncepcja wymiany (pobierania i wysyłania) plików danych za pomocą sieci BitTorrent. W przeciwieństwie do konwencjonalnych serwerów, na których dane są przesyłane, aby inni mogli uzyskać do nich dostęp i je pobrać, pliki torrent są pobierane i wysyłane za pośrednictwem sieci torrent. Gdy użytkownik otwiera plik .torrent w aplikacjach takich jak BitTorrent, oprogramowanie zaczyna pobierać zawartość pliku bitowo. Jeśli wielu użytkowników ma ten sam plik, BitTorrent rozdziela pobieranie między wszystkich użytkowników, aby przyspieszyć proces pobierania. Jednocześnie komputer użytkownika, który pobiera plik, staje się również źródłem pliku do wysłania go innym użytkownikom, którzy również pobierają ten sam plik.

### Struktura pliku TORRENT

Plik torrent to połączenie listy plików i metadanych dotyczących wszystkich fragmentów pliku, który ma zostać pobrany. Zawiera następujące informacje w postaci kluczy.

- `announce` — Adres URL modułu śledzącego, który jest ogłaszany innym rówieśnikom w celu poinformowania o dostępności pliku
- `info` — Odwzorowuje słownik, którego klucze są zależne od tego, czy udostępniany jest jeden lub więcej plików:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `długość` — rozmiar pliku w bajtach.
- `ścieżka` — lista ciągów znaków odpowiadających nazwom podkatalogów, z których ostatnia jest rzeczywistą nazwą pliku
- `długość` — rozmiar pliku w bajtach (tylko gdy udostępniany jest jeden plik)
- `nazwa` — nazwa pliku, w którym plik ma zostać zapisany
- `długość kawałka` — liczba bajtów na kawałek. Zwykle jest to 28 KiB = 256 KiB = 262 144 B.
- `pieces` — lista skrótów będąca konkatenacją skrótu SHA-1 każdego elementu.

## Czy torrentowanie jest bezpieczne i legalne?

Protokół torrentowania do wymiany danych między użytkownikami P2P jest bezpieczny, ponieważ służy tylko do udostępniania dowolnego typu plików. Zatem sam protokół nie jest niebezpieczny ani nielegalny. Treści udostępniane za pośrednictwem sieci mogą jednak zawierać pliki lub nośniki, które mogą naruszać status prawny udostępnianych dokumentów. W takim przypadku wymiana takich danych może spowodować podjęcie kroków prawnych przeciwko stronom zaangażowanym w publiczne udostępnianie takich plików.

## Bibliografia

* [Plik TORRENT - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

