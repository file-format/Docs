{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku HDR - Co to jest plik obrazu HDR?",
  "description":"Poznaj format plików HDR i interfejsy API, które mogą tworzyć i otwierać pliki HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Czym jest plik HDR?

Plik HDR to format pliku obrazu rastrowego High Dynamic Range (HDR) do przechowywania zdjęć z aparatu cyfrowego. Pozwala edytorom zdjęć poprawiać kolory i jasność obrazów cyfrowych o ograniczonym zakresie dynamicznym. Ta modyfikacja może poprawić jasność wokół rogów, dając obraz zbliżony do naturalnego. Pliki HDR są zwykle zapisywane jako 32-bitowe obrazy rastrowe. Adobe Photoshop może tworzyć i otwierać pliki HDR.

Pliki HDR są również znane jako HDRI.

## Format pliku HDR — więcej informacji

Format pliku HDR jest oparty na oryginalnym formacie pliku Radiance Picture (.pic). Dane pikseli w pliku HDR są zwykle przechowywane bez kompresji, ale w niektórych przypadkach są kompresowane przy użyciu prostego systemu kodowania długości serii.

### Struktura pliku HDR

Plik obrazu HDR składa się z następujących trzech części:

* **Nagłówek:** Plik HDR jest identyfikowany przez pierwsze bajty w pliku obrazu, np. „#?RADIANCE”.
* **Ciąg rozwiązania:** Po nagłówku następuje pojedyncza linia rozwiązania, która składa się z 4 wartości; etykiety X i Y, po których następuje liczba całkowita. Kolejność X i Y oznacza rotację. Kombinacja X i Y z wartościami dodatnimi i ujemnymi obejmuje wszystkie możliwe orientacje i obroty obrazu.
* **Dane pikseli:** dane pikseli pliku HDR są nieskompresowane lub skompresowane przy użyciu kodowania o standardowej długości.

## Interfejsy API HDR/HDRI typu open source

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** — Wieloplatformowa, superszybka, pojedyncza biblioteka nagłówkowa [C++](/pl/programming/cpp/) pozwalająca uzyskać rozmiar i format obrazu bez ładowania/dekodowania.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Biblioteka Rust do pobierania rozmiaru i formatu obrazu bez ładowania/dekodowania. Obsługuje formaty [.avif](/pl/image/avif/), [.bmp](/pl/image/bmp/), [.cur](/pl/image/cur/), [.dds](/pl/image/dds/), [. gif](/pl/image/gif/), hdr (pic), [heic (heif)](/pl/image/heic/), [.icns](/pl/image/icns/), [.ico](/pl/image/ico/), [.jp2](/pl/image/jp2/), [jpeg (jpg)](/pl/image/jpeg/), [jpx](/pl/image/jpx/), ktx, [png](/pl/image/png/), [psd](/pl/image/psd/), qoi, tga, tiff (tif) i webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Implementacja HdrHistogram w Javie.

## Bibliografia

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [informacje o obrazie](https://github.com/xiaozhuai/imageinfo)

