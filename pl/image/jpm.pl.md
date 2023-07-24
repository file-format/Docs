{
  "date" : "2019-11-25",
  "keywords" :[ "plik jpm", "format pliku jpm", "co to jest plik jpm", "plik", "przykład jpm", "rozszerzenie pliku jpm", "rozszerzenie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM — złożony format pliku JPEG 2000",
  "description":"Poznaj format pliku JPM i interfejsy API, które mogą tworzyć i otwierać pliki JPM.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## Czym jest plik JMP?

JPM odnosi się do systemu kodowania obrazu JPEG 2000, część 6, który jest używany do obrazowania dokumentów. Opiera się na standardzie Mixed Raster Content Standard (ISO/IEC 16485) i zawiera warstwowe obrazy nieruchome, które korzystają z kodowania JPEG 2000 i innych. Oprócz własnych specyfikacji format pliku JPM dziedziczy funkcje swojego rodzica, tj. formatu pliku [jp2](/pl/image/jp2/).

## Format pliku JPM

Format pliku JPM jest zdefiniowany przez [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) — obraz JPEG 2000 system kodowania -- Część 6: Złożony format pliku obrazu. Obraz złożony może zawierać obrazy zeskanowane, obrazy syntetyczne lub oba, co wymaga połączenia metod kompresji ciągłej i dwupoziomowej. Format pliku JPM definiuje model kompozycji, który opisuje metodę łączenia wielu obrazów w celu wygenerowania złożonego obrazu przy użyciu wielowarstwowego modelu obrazowania Mixed Raster Content (MRC), zdefiniowanego w ITU-T T.44 | ISO/IEC 16485.

### Specyfikacje JPM
Standard formatu plików JPM określa, że jest to kontener binarny reprezentujący złożony obraz, za pomocą którego wiele obrazów można połączyć w jeden obraz. Ustawia mechanizm grupowania wielu obrazów w hierarchii obiektów układu, stron i kolekcji stron w celu przechowywania JPEG 2000 i innych skompresowanych formatów danych obrazu. Format zawiera mechanizm włączania metadanych (często określanych jako metadane strukturalne w projektach bibliotek cyfrowych).

## Bibliografia

* [Zalecenia ITU-T. T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
* [Wikipedia: JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

