{
  "date" : "2019-10-11",
  "keywords" :[ "dicom dosyası", "dicom dosya biçimi", "dicom dosyası nedir", "dosya", "dicom örneği", "dicom dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Dijital Görüntüleme ve İletişim Dosyası Formatı",
  "description":"DICOM dosya formatı ve DICOM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## DICOM dosyası nedir?

DICOM, Tıpta Dijital Görüntüleme ve İletişim'in kısaltmasıdır ve Tıp Bilişimi alanıyla ilgilidir. DICOM, çeşitli satıcılardan yazıcılar, sunucular, tarayıcılar vb. tıbbi görüntüleme cihazlarının entegrasyonu için kullanılır ve ayrıca benzersiz olması için her hastanın kimlik verilerini içerir. DICOM dosyaları, DICOM formatında görüntü verisi alabiliyorlarsa iki taraf arasında paylaşılabilir. DICOM'un iletişim kısmı, uygulama katmanı protokolüdür ve varlıklar arasında iletişim kurmak için TCP/IP'yi kullanır. Web hizmetleri tarafından desteklenen sürümler 1.0, 1.1, 2 veya üstüdür.

## Tarih ##

DICOM, American College of Radiology (ACR) ve National Electrical Manufacturers Association (NEMA) tarafından MRI'lar, CT taramaları ve ultrason görüntüleri gibi tıbbi görüntülerin değişimi ve görüntülenmesi için ortaklaşa geliştirilmiştir. Başlangıçta, makinelerin ürettiği görüntüleri çözmek zordu. Bu nedenle, ACR ve NEMA birlikte 1983'te bir ekip oluşturarak ilk standardı olan ACR/NEMA 300'ü 1985'te piyasaya sürdüler. Satıcılar arasında daha popüler olan ikinci versiyon 1988'de yayınlandı, ancak kısa süre sonra ikinci versiyonun da iyileştirilmesi gerektiği anlaşıldı. Standardın 3. versiyonu 1993 yılında "DICOM" adıyla yayınlandı. 3.0 hala en son sürümdür ancak 1993'ten beri sürekli olarak güncellenmektedir.

## DICOM Dosya Biçimi ##

DICOM, dosya formatı tanımı ile bir ağ iletişim protokolünün birleşimidir. DICOM, .DCM uzantısını kullanır. .DCM iki farklı formatta mevcuttur, yani format 1.x ve format 2.x. DCM Format 1.x'in ayrıca normal ve genişletilmiş iki sürümü mevcuttur. DICOM'un web hizmetleri için HTTP ve HTTPS protokolleri kullanılır.

### Dosya Başlığı ###

Dosya başlığı, 128 bayt Dosya Başlangıcı ve 4 bayt DICOM ön eki içerir.

**Giriş # 128 Bayt**|**Ön Ek # 4 Bayt “D, I, C, M**

**Başlangıç**, yaygın olarak kullanılan görüntü dosyası biçimleriyle uyumluluk sağlayan DICOM dosyasındaki görüntülere ve diğer verilere erişmek için kullanılır.

**Önek**, "DICM" dizesini büyük harflerle içerir.

### Veri Kümesi ###

Her dosya, ilgili IOD ile SOP örneğini ve SOP Sınıfını temsil eden tek bir veri seti içermelidir. Veri seti, gerçek dünya bilgilerinin temsilidir. Veri seti, veri öğelerini içerir ve veri öğeleri, o nesnenin özniteliklerinin değerlerini içerir. Niteliklerin yapısı, IOD'lerde belirtilir. Bir DICOM veri nesnesi, ad, kimlik vb. öğeler dahil olmak üzere bir dizi öznitelikten ve ayrıca görüntü piksel verilerini içeren bir özel öznitelikten oluşur.

### Veri Öğeleri ###

Veri öğesi, veri öğesi Etiketi, Değer uzunluğu ve Veri Öğesi için değerden oluşur. Tip 1 Gerekli Veri öğeleri, Tip 1C Koşullu Veri Öğeleri, Tip 2 Gerekli Veri Öğeleri, Tip 2C Koşullu Veri Öğeleri ve Tip 3 isteğe bağlı Veri Öğeleri olmak üzere 5 tür Veri öğesi vardır. Temel Üç tip veri elemanı yapısı aşağıdaki gibidir.

**Açık Sanal Gerçekliğe Sahip Veri Öğesi**

|Grup Numarası|Öğe Numarası|Değer Gösterimi|Ayrılmış|Değer Uzunluğu|Değer Alanı
---|---|---|---|---|---|
|2 Bayt|2 Bayt|2 Bayt|2 Bayt # 0x00, 0x00|4 Bayt|"Değer Uzunluğu Baytı"

**Açık Sanal Gerçekliğe Sahip Veri Öğesi**

|Grup Numarası|Öğe Numarası|Değer Gösterimi|Değer Uzunluğu|Değer Alanı
---|---|---|---|---|
|2 Bayt|2 Bayt|2 Bayt|2 Bayt|"Değer Uzunluğu Baytı"

**Örtük Sanal Gerçekliğe Sahip Veri Öğesi**


|Grup Numarası|Element Numarası|Değer Uzunluğu|Değer Alanı
---|---|---|---|
|2 Bayt|2 Bayt|4 Bayt|"Değer Uzunluğu Baytı"

1. **Veri Öğesi Etiketi**: Grup numarasını ve öğe numarasını temsil eden sıralı bir tam sayı
1. **Değer Temsili VR**: VR, veri Öğesinin VR'sini temsil eden bir karakter dizisidir.
1. **Değer Uzunluğu**: işaretsiz tamsayı, değer alanının açık uzunluğunu temsil ediyor mu?
1. **Değer Alanı**: Veri öğelerinin değerlerini açıklar.

## Aktarım Sözdizimi ##

Transfer sözdizimi, daha soyut sözdizimlerini açık bir şekilde temsil etmek için kodlamaya yönelik bir dizi kuraldır. Transfer sözdizimi yardımıyla iletişim kuran varlıklar, destekledikleri ortak kodlama teknikleri üzerinde anlaşırlar.

## SOP'ler ##

IOD ve DIMSE birliği bir SOP Sınıfı tanımlar. SOP Sınıfı tanımı, DIMSE Hizmet Grubundaki hizmetlerin veya IOD'nin Niteliklerinin kullanımını kısıtlayabilecek kuralları ve semantiği içerir. Hizmet Elemanlarına örnek olarak Depola, Al, Bul, Taşı vb. verilebilir. Nesne örnekleri CT görüntüleri, MR görüntüleridir, fakat aynı zamanda program listeleri, yazdırma kuyrukları vb. içerir.

## Hizmetler ##

DICOM, çoğunlukla veri iletişimi ile ilgili çeşitli hizmetler sunar. Her biri aşağıda kısaca açıklanmıştır:


**Mağaza:** DICOM Mağazası hizmeti, görüntüleri veya diğer nesneleri bir resim arşivleme ve iletişim sistemine (PACS) veya sunucuya gönderir.


**Depolama taahhüdü:** Depolama taahhüdü hizmeti, bir görüntünün herhangi bir ortam türünde cihazda kalıcı olarak saklandığını doğrulamak için kullanılır.


**Sorgula/geri al:** Bu hizmet, bir iş istasyonunun görüntü listelerini veya diğer nesneleri bulmasını ve ardından bunları PACS'den almasını sağlar.


**Modalite iş listesi:** Modalite iş listesi hizmeti, bir görüntü alma cihazı tarafından gerçekleştirilmek üzere programlanmış görüntüleme prosedürlerinin bir listesini verir.


**Yazdır:** Bu hizmet, görüntüleri yazıcıya gönderir.

## Numaraları IP üzerinden bağlantı noktası ##

DICOM aşağıdaki TCP ve UDP bağlantı noktalarını kullanır:

1. 104
1.2761
1. 2762
1. 11112

## Referanslar ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

