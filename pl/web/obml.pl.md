{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku OBML - zapisany plik strony internetowej Opera Mini",
  "description" :"Dowiedz się, czym jest plik OBML i interfejsy API, które mogą tworzyć i otwierać plik OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Czym jest plik OBML?

Plik OBML (Opera Binary Markup Language) to wersja offline strony internetowej zapisana przez przeglądarkę mobilną Opera Mini. Jest to samodzielna, kompaktowa wersja plików [HTML](/pl/web/html/), która zawiera wszystkie elementy strony do wyświetlania na określonych urządzeniach w trybie offline. Format pliku OBML został zaktualizowany do kilku wersji, przy czym OBML15 i OBML16 są powszechnie używane. Ważną kwestią, o której należy pamiętać, jest to, że każda wersja Opery Mini jest kompatybilna tylko z jednym formatem OBML. W związku z tym uaktualnienie Opery Mini sprawi, że wcześniej zapisane strony będą nadal czytelne. Pliki OBML można konwertować do formatu HTML i [PDF](/pl/pdf/).

## Format pliku OBML

Format pliku OBML jest zapisywany w zastrzeżonym formacie Opery, a jego specyfikacje formatu plików nie są publicznie dostępne. Jednak [format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) został poddany inżynierii wstecznej w celu zdekodowania jego struktury w następujący sposób.

### Typy danych OBML

Zgodnie z wynikami inżynierii wstecznej OBML używa następujących typów pierwotnych:

* `bajt` – liczba całkowita bez znaku (1 bajt)
* `short` – liczba całkowita ze znakiem (2 bajty, big-endian)
* `medium` – liczba całkowita ze znakiem (3 bajty, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – bajt zawierający znak ASCII
* `string` – blob zawierający tekst zakodowany w UTF-8

### Nagłówek OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Bibliografia

* [format OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

