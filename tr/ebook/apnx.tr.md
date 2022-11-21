{
  "date" : "2021-03-11",
  "keywords" :["APNX", "Amazon Sayfa Numarası Dizini", "uzantı", "dosya", "biçim", "eKitap", "Amazon Kindle"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Amazon APNX dosya biçimi ve APNX dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"APNX - Amazon Sayfa Numarası Dizini",
  "linktitle" : "APNX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-05-28"
}

## APNX dosyası nedir? ##

.apnx uzantısını kullanan Amazon Sayfa Numarası Dizini dosyası bir e-Kitap dosya türüdür; Amazon Kindle tarafından kullanılır. Bu dosyalar aslında Kindle cihazları tarafından kullanılan sayfalandırma dosyaları olarak bilinir. Bu nedenle, APNX dosyaları genellikle Kindle e-Kitaplarının sayfalarını işaretlemek için oluşturulur. Sayfalandırma özelliği, 3.1 ürün yazılımından bu yana Amazon Kindle cihazlarında başlatılmıştır. Sayfa dizinleri için APNX dosyasına bakar ve ardından onu orijinal basılı kitaptaki sayfa numaralarıyla eşler. Bu dosyalar, Amazon e-Kitap dosyalarıyla birlikte Kindle cihazlarına kaydedilir. APNX dosyalarını açamaz veya düzenleyemezsiniz.

## APNX Dosya Biçimi Özellikleri ##

### Düzen

|bayt| içerik| yorumlar|
---|---|---|
|4 |00010001 | Biçim tanımlayıcısı. 65537 küçük endian'ın değeri.|
|4 |sonrakinin başlangıcı | İlk başlığın bitiş konumundan sonraki ofset. Yeni bir başlık bilgi| dizisini başlatır.
|4 |uzunluk| İlk başlığın uzunluğu|
|N |ilk başlık | İçerik başlığını içeren dize. Bir sonraki sırayı başlatır|
|2 |bilinmeyen | Her zaman 1|
|2 |uzunluk | İkinci başlığın uzunluğu|
|2 |sayfa sayısı | Sayfaları temsil eden ikinci başlıktan sonraki toplam bayt sayısı. Bu toplam, pageMap tarafından yok sayılan baytları içerir.|
|2 |bilinmeyen | Her zaman 32|
|N |ikinci başlık | Sayfa eşleme başlığını içeren dize |
|4*N |doldurma | Sayfa eşleme başlığında verilen ilk sayı 0 bayt sayısını gösterir.|
|4*N |sayfa listesi ||

### İçerik Başlığı

İçerik başlığı, anahtar, değer çiftlerini içeren {} içine alınmış bir dizeden oluşur:

|içerik| yorumlar|
---|---|
|içerikKılavuzu| Rehber.|
|aşın | Kitabın Kindle sürümü için Amazon tanımlayıcısı.|
|cdeTürü | MOBI cdeType. E-kitaplar için her zaman EBOK olmalıdır.|
|fileRevisionId | Bu dosyanın revizyonu.|

#### Örnek
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Sayfa Eşleme Başlığı
Sayfa eşleme başlığı, anahtar, değer çiftleri içeren {} içine alınmış bir dizeden oluşur.

|içerik | yorumlar|
---|---|
|aşın | Sayfaların karşılık geldiği kağıt kitap için ISBN 10|
|sayfa Haritası| Üç değerli demet. Şuna benziyor: "(N,N,N)\
1) Sayfa numaralandırma sırasını başlatan başlıktan sonraki bayt sayısı\
2) bilinmeyen\
3) bilinmiyor\|
#### Örnek
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Sayfa Listesi

Sayfa listesi, ham HTML'deki bir ofsetler dizisidir. Her biri
değer, yeni bir sayfanın başlangıcıdır. Her giriş 4 baytlık bir büyük endian'dır
int.



## Referanslar

* [Amazon APNX dosya formatı](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)
* [APNX - MobileRead Wiki tarafından](https://wiki.mobileread.com/wiki/APNX)

