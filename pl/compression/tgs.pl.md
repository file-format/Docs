{
  "date" : "2019-10-11",
  "keywords" :["plik tgs", "format pliku tgs", "co to jest plik tgs", "plik", "przykład tgs", "rozszerzenie pliku tgs", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Telegram animowany format pliku naklejek",
  "description":"Poznaj format plików TGS i interfejsy API, które mogą tworzyć i otwierać pliki TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Czym jest plik TGS?

Plik z rozszerzeniem .tgs to plik animowanej naklejki, który został wprowadzony przez międzyplatformową usługę przesyłania wiadomości [Telegram](https://core.telegram.org/stickers#animated-stickers). Animowane naklejki są używane przez użytkowników aplikacji do przesyłania wiadomości do wysyłania bardziej ulepszonych i żywych treści w wiadomościach, w przeciwieństwie do statycznych grafik, które są nieruchomymi obrazami. Telegram początkowo używał formatu pliku [WEBP](/pl/image/webp/) dla naklejek ze zdjęciami. Format pliku TGS może przechowywać dane animacji w wyższych rozdzielczościach i mniejszym rozmiarze pliku w porównaniu ze statycznymi naklejkami WEBP. Pliki TGS można otwierać za pomocą aplikacji takich jak Telegram, 7-zip, Apple Archive Utility i Corel WinZip.

## Format pliku TGS

Telegram wprowadził format pliku TGS w lipcu 2019 roku w oparciu o bibliotekę Lottie. Plik TGS składa się z tekstu [JSON](/pl/web/json/), który jest eksportowany z animacji w programie Adobe After Effects. Wyeksportowany tekst JSON jest kompresowany przy użyciu kompresji gzip, która zmniejsza rozmiar pliku. Informacje JSON o pliku tekstowym są przechowywane w pliku tekstowym, który staje się podstawą wysokich współczynników kompresji.

### Specyfikacje naklejek TGS

Format pliku TGS nakłada pewne ograniczenia na tworzenie animowanych naklejek TGS. Animowany plik TGS:

* Rozmiar naklejki/płótna musi wynosić 512 x 512 pikseli.
* Obiekty naklejek nie mogą opuszczać płótna.
* Długość animacji nie może przekraczać 3 sekund.
* Wszystkie animacje muszą być zapętlone.
* Rozmiar naklejki nie może przekraczać 64 KB po wyrenderowaniu w Bodymovin.
* Wszystkie animacje muszą działać z szybkością 60 klatek na sekundę.

### Przykładowy tekst JSON TGS

Przykładowa animowana naklejka po rozpakowaniu zawiera następującą treść tekstową JSON.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Bibliografia ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

