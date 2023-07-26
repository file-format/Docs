{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MK3D Dosya Biçimi",
  "keywords" :[ "mk3d", "matroska video", "mkv formatı", "stereoskopik 3d", "StereoMod", "video", "dosya", "biçim" ],
  "description":"Matroska tarafından oluşturulan stereoskopik 3d videolar için MK3D dosya formatı ve MK3D dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## MK3D dosyası nedir? ##

MK3D dosyaları, Matroska video formatları ailesine aittir. Bu dosyalar aslında Matroska 3D formatı kullanılarak oluşturulmuş **stereoskopik 3d** videolar. MKV dosya Kabı, stereoskopik 3B video öğelerinin türünü tanımlamak için bir StereoMode alanının değerini kullanır. Mavi ve kırmızı renkleri ayırarak eski stereo 3D videoları görüntülemek için bir StereoMode değeri de mevcuttur (AnaGlyph)

## Teknik detaylar ##
3D videolar aşağıdaki iki şekilde sıkıştırılabilir:

- Her göz için ayrı iz.
- Her göz takibini tek bir izde birleştirin.

MKV dosya kabı bunların her ikisini de destekler.

İçerisindeki 3D malzeme ile daha kolay olan single-track videolar için uçakların mono veya sol sağ kombine track'te birleştirilmesine karar veren **StereoMode** alanını ayarlamanız gerekir. Aşağıdaki StereoMode alan değerlerinden birini kullanabilirsiniz:

|Değer | Açıklama |
|---|---|
|0| mono|
|1| yan yana (önce sol göz)|
|2| üst-alt (önce sağ göz)|
|3| üst-alt (sol göz önce gelir)|
|4| dama tahtası (sağ önce gelir)|
|5| dama tahtası (sol ilk)|
|6| satır serpiştirilmiş (sağ ilk)|
|7| satır serpiştirilmiş (sol ilk)|
|8| sütun serpiştirilmiş (önce sağ)|
|9| sütun serpiştirilmiş (sol ilk)|
|10| anaglif (mavi/kırmızı)|
|11| yan yana (önce sağ göz)|
|12| anaglif (yeşil/eflatun)|
|13| her iki göz de bir Blokta bağlanmıştır (sol göz önce gelir) (alan sıralı modu)|
|14| her iki göz de bir Blokta bağlanmıştır (sağ göz önce gelir) (alan sıralı modu)|

Birden çok yol için, MKV kabının her bir yolun işlevselliğine ayrı ayrı karar vermesi gerekir. **TrackCombinePlanes** ile **TrackOperation**, işi yapmak için kullanılır.


## Referanslar ##

- [Matroska Spesifikasyon Notları](https://www.matroska.org/technical/notes.html)
- [Stereo 3D Video ve MK3D Dosyaları için MKV Dosya Kabı Desteği](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

