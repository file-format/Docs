
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS Dosyası - Ada Spesifikasyon Dosya Formatı",
  "description":"Örnek ve ADS dosyalarını oluşturabilen ve açabilen API'lerle ADS dosya biçiminin ne olduğunu öğrenin.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Bir ADS dosyası nedir?

Bir ADS dosyası, Ada programlama projesi için bir belirtim dosyasıdır. Java için bir sınıfa veya C++ durumunda başlık ve uygulama çiftine benzer. Ada paketinin genel ve özel belirtimleri .ads dosyasında saklanır. .adb dosyası, aksine uygulamayı veya Ada gövdelerini içerir. [C++](/tr/programming/cpp/) gibi, Ada da spesifikasyonlar ve OOP'den bağımsız uygulamalar arasında ayrım sunar.

ADS dosyaları Microsoft Notepad, Notepad++ ve Atom gibi herhangi bir metin düzenleyicide açılabilir.

## ADS Dosya Biçimi

ADS dosyaları basit düz metin dosyası biçimindedir ve herhangi bir metin düzenleyiciyle açılabilir/düzenlenebilir. Ada paketleri hiyerarşiler halinde düzenlenebilir. Bir alt birim aşağıdaki şekilde bildirilebilir:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Referanslar

* [Ada Paketleri](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

