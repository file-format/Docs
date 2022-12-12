{
  "date" : "2021-08-11",
  "keywords" :[ "plik wim", "format pliku wim", "co to jest plik wim", "plik", "przykład wim", "rozszerzenie pliku wim", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Poznaj format pliku WIM i interfejsy API, które mogą tworzyć i otwierać pliki WIM.",
  "title" :"WIM - plik formatu Windows Imaging",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Czym jest plik WIM?
Pliki z rozszerzeniem .wim po raz pierwszy pojawiły się w systemie Windows Vista. WIM należy do formatu obrazowania opartego na plikach, który był zwykle wprowadzany w systemie Microsoft Windows Vista. Umożliwia wdrożenie pojedynczego obrazu dysku na różnych platformach komputerowych. Pliki WIM służą do zarządzania plikami, takimi jak aktualizacje, sterowniki i komponenty, bez ponownego uruchamiania obrazu systemu operacyjnego. Plik AQ WIM zawiera zestaw plików i powiązanych metadanych, które są bardzo podobne do innych formatów plików dyskowych.

## formaty plików WIM
Format pliku WIM nie przypomina formatów opartych na sektorach, takich jak VHD lub IS, w rzeczywistości jest oparty na plikach, co oznacza, że podstawową jednostką informacji w WIM jest plik. Podstawową zaletą oparcia na plikach jest to, że przechowywanie pojedynczej instancji pliku jest wielokrotnie odwoływane w drzewie systemu plików i niezależność sprzętowa. Zmniejsza obciążenie związane z otwieraniem i zamykaniem różnych plików indywidualnie, ponieważ pliki są przechowywane w jednym WIM plik. Pliki WIM mogą przechowywać wiele obrazów dysków, do których odwołuje się ich unikalna nazwa lub indeks numeryczny.
### Obsługa algorytmów kompresji
WIM obsługuje następujące rodziny algorytmów kompresji w malejącej prędkości i rosnącym współczynniku:
-XPRESS
-LZX
- LZMS
Solidna kompresja.
Pierwsze trzy rodziny są oparte na LZ77, podczas gdy solidna kompresja została wprowadzona wraz z LZMS w WIMGAPI Windows 8 i DISM Windows 8.1.
### Narzędzia do formatu plików WIM
Następujące narzędzia zazwyczaj obsługują format pliku WIM:

- **ImageX**: Narzędzie wiersza polecenia służące do edytowania, tworzenia i wdrażania obrazów dysków Windows w formacie Windows Imaging. Wraz z odpowiednim WIMGAPI jest dystrybuowany jako część bezpłatnego zestawu zautomatyzowanej instalacji systemu Windows. Począwszy od systemu Windows Vista, Instalator systemu Windows używa interfejsu API WAIK do instalowania systemu Windows.
- **DISM**: narzędzie wprowadzone w systemach Windows 7 i Windows Server 2008 R2, które może wykonywać zadania związane z usługami na obrazie instalacyjnym systemu Windows, niezależnie od tego, czy jest to obraz online, czy obraz offline w folderze lub pliku WIM. to narzędzie było zdolne do montowania i odmontowywania obrazów, dodawania sterownika urządzenia do obrazu offline i wysyłania zapytań do zainstalowanych sterowników urządzeń w obrazie offline.
 




## Bibliografia


* [Format Windows Imaging – Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


