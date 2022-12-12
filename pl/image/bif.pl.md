{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik BIF - Ventana Cały format obrazu slajdu",
  "description":"Poznaj format pliku BIF i interfejsy API, które mogą tworzyć i otwierać pliki BIF.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Czym jest plik BIF?

Plik BIF to plik obrazu rastrowego zawierający obraz próbki slajdu. Składa się z wielu obrazów TIFF, które są łączone przez aplikacje do przeglądania slajdów w jeden złożony obraz. Pliki BIF są tworzone przez cyfrowy skaner slajdów firmy Ventana Medical i są w pełni zgodne z wariantem BigTIFF definicji [TIFF](/pl/image/tiff/) v 6.0.

## Format pliku BIF

Plik BIF jest zapisywany jako binarny plik obrazu i składa się z aż 200 000 x 200 000 pikseli. Może to prowadzić do dużych rozmiarów plików, przekraczając limit rozmiaru 4 GB narzucony przez 32-bitowe wskaźniki plików zdefiniowane przez standard TIF. Jednak w przypadku 64-bitowych wskaźników plików ta bariera rozmiaru pliku jest pokonywana przez wariant BigTIFF standardu TIFF.

### Kto używa pliku BIF?

Pliki BIF są używane przez cyfrowe skanery slajdów do skanowania i tworzenia cyfrowych kopii próbek slajdów. Jeśli jesteś patologiem, możesz otwierać te pliki BIF w aplikacjach do przeglądania slajdów. Dzięki dużemu poziomowi szczegółowości i wysokiej rozdzielczości danych można powiększać i pomniejszać obraz slajdu, aby wyświetlać sekcje preparatu z większą lub mniejszą liczbą szczegółów. Plik metadanych [XML](/pl/web/xml/) obecny w tych plikach określa sposób łączenia obrazów oraz obraz, który powinien być używany jako miniatura pliku.

## Jak Otworzyć Plik BIF?

Pliki BIF można otwierać za pomocą:

* OpenSlide (wieloplatformowy)
* ImageJ (wieloplatformowy)
* Przeglądarka NetScope (Windows)

## Bibliografia ##

* [Biały dokument Roche Digital Pathology BIF](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

