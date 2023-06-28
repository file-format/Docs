{
  "date" : "2021-02-10",
  "keywords" :[ "plik jpx", "format pliku jpx", "co to jest plik jpx", "plik", "przykład jpx", "rozszerzenie pliku jpx", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX — format pliku obrazu",
  "description":"Poznaj format pliku JPX i interfejsy API, które mogą tworzyć i otwierać pliki JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Czym jest plik JPX? ##

Plik z rozszerzeniem .jpx jest rozszerzeniem formatu plików JPEG 2000. Wykorzystuje przede wszystkim kompresję JPEG 2000, a także zapewnia zaawansowane funkcje, takie jak wiele warstw obrazu, różne przestrzenie kolorów, krycie i pofragmentowane strumienie kodu. JPX umożliwia również inne kompresje, takie jak JBIG, CCITT Group3, CCITT Group4 itp. Oprócz kompresji JPEG 2000. Format pliku JPX został zatwierdzony jako standard [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), ale nie spotkał się z ciepłym przyjęciem ze względu na szerokie wykorzystanie formatu [JPEG ](/pl/image/jpeg/) w formacie pliku. Aplikacje, które mogą otwierać pliki JPX, to Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 i CorelDraw Graphics Suite 2020.

## Krótka historia

W 2000 roku komitet Joint Photographic Experts Group zaprojektował JP2 w celu ulepszenia własnego standardu JPEG opartego na dyskretnej transformacji kosinusowej za pomocą tej nowej metody opartej na falkach. Komitet JPEG miał na celu udostępnienie swoich podstawowych metod bez opłat licencyjnych. W konkurencji o licencję JP2 wśród 20 firm wygrały one o włos. JPEG 2000 został ogłoszony jako standard ISO, chociaż większość przeglądarek internetowych nie jest gotowa do pomocy JPEG 2000 od 2017 r. W 2004 r. format ISO/IEC 15444-2 został publicznie zaakceptowany jako rozszerzenie formatu plików JP2.

## Format pliku JPX

Format pliku JPX został opracowany w celu spełnienia wymagań aplikacji, które potrzebowały struktur danych wykraczających poza funkcjonalność zdefiniowaną przez format pliku [JP2](/pl/image/jp2/). Plik JP2 z niekompatybilnymi rozszerzeniami może prowadzić do zamieszania na rynku, gdzie niektórzy czytelnicy mogą interpretować niektóre pliki JP2, ale nie inne. JPX jest odpowiedzią na unikanie takich problemów w aplikacjach.

### Identyfikacja pliku

Pliki JPX są przechowywane jako [JPF](/pl/image/jpf/), gdy są przechowywane w tradycyjnym komputerowym systemie plików. Dlatego termin JPX jest najrzadziej używany w porównaniu z JPF. Plik JPX zaczyna się od następujących bajtów:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organizacja plików

Podobnie jak JP2, plik JPX jest zbiorem pól o strukturze binarnej z polami ułożonymi w ciągłej kolejności. Pierwsze pole daje początek pliku z jego pierwszym bajtem, a ostatni bajt ostatniego pola reprezentuje ostatni bajt pliku.
Binarna struktura pudełka w pliku JPX jest identyczna z tą zdefiniowaną w formacie pliku [JP2](/pl/image/jp2/).

### Przechowywanie CodeStream w JPX

Format pliku JPX umożliwia podzielenie strumienia kodu obrazu na fragmenty. Umożliwia to modyfikację pojedynczego kafelka obrazu i zapisanie zmodyfikowanego kafelka na końcu pliku bez przepisywania całego pliku. Oryginalny format pliku [JP2](/pl/image/jp2/) ogranicza przechowywanie całego strumienia kodu w ciągłej części pliku, co może być problematyczne dla aplikacji do edycji obrazu, które mogą chcieć zmodyfikować pojedynczy kafelek obrazu i osiągnąć powyższa obsługa przez format pliku JPX. Fragmentacja strumienia kodu obrazu sprawia, że format pliku JPX jest lepszy od formatu pliku JP2. Ponadto format pliku JPX umożliwia łączenie wielu strumieni kodu i generowanie renderowanego wyniku. Strumienie kodu można łączyć jako kompozycję i animację.

## Bibliografia ##

* [Przegląd formatu JPEG 2000](https://jpeg.org/jpeg2000/)

