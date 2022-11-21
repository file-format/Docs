{
  "date" : "2019-10-11",
  "keywords" :[ "ico dosyası", "ico dosya biçimi", "ico dosyası nedir", "dosya", "ico örneği", "ico dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Görüntü Dosyası Biçimi",
  "description":"ICO dosya formatı ve ICO dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## ICO dosyası nedir?

ICO uzantılı dosyalar, [Microsoft Windows](https://www.microsoft.com/en-us/windows) üzerindeki bir uygulamanın temsili için simge olarak kullanılan görüntü dosyası türleridir. Bunlar, ekranın gereksinimlerine uyacak şekilde farklı boyut, renk desteği ve çözünürlükte gelir. Microsoft Windows'daki başka bir benzer görüntü dosyası formatı, imleç temsili için [CUR](/tr/image/cur/) biçimidir ve görüntü başlığında bir sıcak nokta tanımlar. MacOS'ta ICNS dosya biçimleri, ICO dosyalarıyla aynı amaca hizmet eder. Çeşitli çevrimiçi web siteleri ve uygulamalar, bu tür dosyaları oluşturma ve [BMP](/tr/image/bmp/), [PNG](/tr/image/png/), vb. gibi diğer görüntü biçimlerini simge dosyası biçimine dönüştürme özelliği sağlar. ICO dosyaları için resmi IANA kayıtlı İnternet ortam türü image/vnd.microsoft.icon'dur.

## Kısa Tarih ##

Simgeler, Microsoft Windows 1.0'ın piyasaya sürülmesiyle tanıtıldı. Bunlar 32x32 boyutundaydı ve tek renkliydi. Win32'nin gelişiyle birlikte, 256x256 piksele kadar boyutta gerçek renkli simge görüntüleri için destek sunuldu. Windows XP, 32 bit renkli simge görüntülerini destekleyen ilk kişi oldu ve simgeye gölgeler, kenar yumuşatma ve cam benzeri efektler gibi yarı saydam alanların eklenmesine izin verdi. Microsoft, Windows XP için yalnızca 48×48 piksele kadar olan simge boyutlarını önermektedir. Windows Vista, Windows Gezgini'ne 256×256 piksellik bir simge görünümü ve sıkıştırılmış [PNG](/tr/image/png/) biçimi desteği ekledi. Daha yüksek çözünürlükler ve yüksek DPI modları kullanan kullanıcılar için daha büyük simge biçimleri (256×256 gibi) önerilir.

## ICO Dosya Biçimi ##

Tek bir ICO dosyası, birden çok boyutta ve renk derinliğinde bir veya daha fazla küçük görüntüden oluşur. Farklı boyutlarda görüntülerin varlığı, farklı ekran çözünürlüklerinde uygun ölçekleme içindir. ICO/CUR dosyalarındaki tüm değerler [little-endian](https://en.wikipedia.org/wiki/Little-endian) bayt düzeninde gösterilir.

ICO dosyası bir Simge başlığından, bir Simge Dizininden,

|Alan|Açıklama
---|---|
|Icon Header|ICO dosyası hakkında genel bilgileri saklar.
|Dizin[1..n]|Dosyadaki her görüntü hakkında genel bilgileri saklar.
|Simge #1|Eski AND/XOR DIB biçimindeki veya daha yeni PNG biçimindeki ilk görüntü için gerçek "veriler"
|...|
|Icon #n|Son simge görüntüsü için veriler

### Başlık ###

|Ofset|Boyut (bayt cinsinden)|Amaç
---|---|---|
|0|2|Ayrıldı. Her zaman 0 olmalıdır.
|2|2|Görüntü türünü belirtir: Simge (.ICO) görüntüsü için 1, imleç (.CUR) görüntüsü için 2. Diğer değerler geçersiz.
|4|2|Dosyadaki görüntü sayısını belirtir.

### Dizin ###

ICONDIR yapısı olarak temsil edilen bir ICO dosyasında bulunan dizin, dosyadaki her görüntü için bir ICONDIRECTORY yapısı içerir. Aynısını, tüm görüntü bitmap verilerinin bitişik bir bloğu izler. Bu, aşağıda gösterildiği gibidir.

|Ofset|Boyut|Açıklama
---|---|---|
|0 (0)|1|Genişlik, 256 piksel ise 0 olmalıdır
|1 (1)|1|Yükseklik, 256 piksel ise 0 olmalıdır
|2 (2)|1|Renk sayısı, 256'dan fazla renk varsa 0 olmalıdır
|3 (3)|1|Ayrılmış, 0 olmalıdır
|4 (4)|2|.ICO biçimindeyken renk düzlemleri 0 veya 1 veya .CUR biçimindeyken X etkin noktası olmalıdır
|6 (6)|2|.ICO biçimindeyken piksel başına bit veya .CUR biçimindeyken Y etkin noktası
|8 (8)|4|Bit eşlem verilerinin bayt cinsinden boyutu.
|12 (C)|4|Dosyada ofset.

## Referanslar ##

* [ICO - Wikipedia Tarafından](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

