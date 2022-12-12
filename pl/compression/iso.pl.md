{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO — format pliku obrazu dysku",
  "description":"Co to jest plik ISO i interfejsy API, które mogą tworzyć i otwierać pliki ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Czym jest plik ISO?

Plik z rozszerzeniem .iso to nieskompresowany plik obrazu dysku archiwum, który reprezentuje zawartość całych danych na dysku optycznym, takim jak CD lub DVD. W oparciu o standard [ISO-9660](https://www.iso.org/standard/17505.html), format pliku obrazu ISO zawiera dane dysku wraz z przechowywanymi na nim informacjami o systemie plików. Zdolność plików ISO do przechowywania dokładnej repliki zawartości sprawia, że jest to idealny typ pliku do tworzenia kopii płyt CD/DVD i jest najczęściej używany do przechowywania danych startowych do instalacji. W większości przypadków pliki ISO są nagrywane na USB/CD/DVD jako zawartość startowa do uruchamiania komputera w celu instalacji. Pliki ISO mają typ MIME application/x-iso9660-image.

## Format pliku ISO

Format pliku ISO różni się od innych formatów plików kontenerów, chociaż archiwizuje określoną zawartość danych. Archiwum jest tworzone jako plik binarny z dokładną strukturą zawartości i informacjami o systemie plików. Format pliku ISO jest opisany w [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) w następujący sposób.

### Struktura najwyższego poziomu pliku ISO

Ogólna struktura pliku składa się z:

* „Obszar systemowy” — 32 768 bajtów i nie jest używany przez ISO_9660
* `Obszar danych` - składa się z zestawu deskryptorów woluminu i tabel ścieżek, katalogów i plików

### Zestaw deskryptorów woluminu

Obszar danych zaczyna się od zestawu deskryptorów woluminu, zestawu jednego lub więcej deskryptorów woluminu zakończonego terminatorem zestawu deskryptorów woluminu. Działają one łącznie jako nagłówek obszaru danych, opisujący jego zawartość (podobnie jak blok parametrów BIOS używany przez dyski sformatowane w systemach FAT, HPFS i NTFS).

Zestaw deskryptorów woluminu jest pokazany poniżej.

|Zestaw deskryptorów woluminu|
---|
|Deskryptor woluminu #1|
|...|
|Deskryptor woluminu #N|
|Terminator zestawu deskryptorów woluminu|

#### Deskryptor woluminu

Każdy deskryptor woluminu ma rozmiar 2048 bajtów i ma następującą strukturę:

|Część |Typ |Identyfikator |Wersja |Dane|
---|---|---|---|---|
|Rozmiar |1 bajt |5 bajtów (zawsze 'CD001') |1 bajt (zawsze 0x01) |2041 bajtów|

## Bibliografia

* [Obraz dysku optycznego – Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Podpisy plików] (https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 – Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

