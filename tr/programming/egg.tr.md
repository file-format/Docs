{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"YUMURTA Dosya Biçimi - Python Dağıtım Dosyası",
  "description":"EGG dosya formatı ve EGG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## YUMURTA dosyası nedir?

Python yumurtaları olarak da bilinen bir EGG dosyası, Python dağıtımlarının daha eski bir dağıtım biçimidir. Bu, .egg uzantılı [ZIP](/tr/compression/zip/) sıkıştırılmış bir arşivdir ve dağıtımla ilgili meta bilgilerle birlikte Python uygulamasının kaynak dosyalarını içerir. EGG dosyaları Windows Yürütülebilir [EXE](/tr/executable/exe/) dosyasına alternatiftir ancak platformlar arasıdır. Python dağıtımları için bu eski format, 2010'un başlarında daha yeni Wheel (WHL) dosya formatı ile değiştirilmiştir.

## YUMURTA Dosya Biçimi

EGG dosyaları sıkıştırılmış ZIP arşivleri olarak kaydedilir. Bu, .egg uzantısını .zip ile değiştirirseniz Corel WinZIP, Microsoft Explorer veya RARLAB WinRAR gibi standart açma programları ile açabileceğiniz anlamına gelir.

EGG dosyaları, Python tarafından sağlanan **distutils** paketi kullanılarak oluşturulabilir. EGG dosyaları oluşturabilen ve açabilen başka bir araç **SetupTools**'tur. EGG dosyaları **easy_install** kullanılarak bir paket olarak kurulabilir.

`NOT - EGG dosya formatı, yeni tekerlek WHL dosya formatı lehine yürürlükten kaldırılmıştır.`

## Referans ##

* [Python YUMURTA](https://python101.pythonlibrary.org/chapter38_eggs.html)

