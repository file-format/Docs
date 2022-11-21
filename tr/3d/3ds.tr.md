{
  "date" : "2019-10-11",
  "keywords" :[ "3DS","dosya", "biçim", "dosya türü", "uzantı","3DS dosyası nedir?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"3DS dosya formatı ve 3DS dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "title" :"3DS Dosya Biçimi",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## 3DS dosyası nedir?

.3ds uzantılı bir dosya, Autodesk 3D Studio tarafından kullanılan 3D Ses (DOS) ağ dosyası formatını temsil eder. Autodesk 3D Studio, 1990'lardan beri 3D dosya formatı pazarındadır ve şimdi 3D modelleme, animasyon ve işleme ile çalışmak için 3D Studio MAX'a dönüşmüştür. Bir 3DS dosyası, sahnelerin ve görüntülerin 3B temsili için veriler içerir ve 3B veri içe ve dışa aktarma için popüler dosya biçimlerinden biridir. Bir sahneyi işlemek için köşeler ve çokgenler oluşturmak üzere kamera konumları, Kafes verileri, aydınlatma bilgileri, görüntü alanı yapılandırmaları, yumuşatma grubu verileri, bitmap referansları ve nitelikler gibi bilgileri dikkate alır.

## 3DS Dosya Biçimi - Daha Fazla Bilgi
3DS, temelinde bir ikili dosya formatıdır ve verilerin depolanması ve alınması için önceden tanımlanmış bir yapıyı takip eder. İkili dosya formatı, 3DS dosya formatının metin tabanlı dosya formatlarına kıyasla daha hızlı olmasını sağlar. Bir 3DS dosyasındaki veriler parçalar halinde saklanır.

### 3DS Yığın

Bir 3DS dosyasındaki her parça, bir kimlik, bir sonraki bloğun konumu için bloğun uzunluğu ve verilerin kendisini içeren bir veri bloğudur. Yığın kimliği, 3DS dosya formatı okuyucularının tanımadıkları blokları atlamalarına izin verir. Ayrıca formatın genişletilebilirliğine de yardımcı olur. Her parça, birlikte sahneyi oluşturan şekiller, aydınlatma ve görüntüleme bilgileriyle ilgili bilgileri depolar. Parçalar, bir 3DS dosyasında hiyerarşik bir yapıda düzenlenir ve gösterimde XML Belge Nesnesi ağacına benzer.

**Yığın Kimliği:** Bir öbeğin ilk iki baytı, dosya okuyucunun okuma sırasında bunu göz önünde bulundurmaya mı yoksa atlamaya mı karar vermesine olanak tanıyan bir yığın tanımlayıcısını temsil eder.

**Yığın uzunluğu:** Yığın kimliğinin ardından, parçanın uzunluğunu temsil eden 4 baytlık bir tamsayı (little-endian cinsinden) gelir. Bu uzunluk ayrıca verinin uzunluğunu, alt bloklarının uzunluğunu ve 6 baytlık başlığı da içerir.

**Yük:** Parçanın uzunluğunu, yığın için gerçek veri baytları takip eder ve ardından aynı hiyerarşik yapıdaki birkaç derinliğe genişletilebilen alt yığınları gelir.

### Bir Parçanın Yapısı

Basit bir yığının hiyerarşik yapısı aşağıda gösterildiği gibidir:

**Bir yığın**

|başlangıç|bitiş|boyut|ad
--- | --- | --- | ---
|0|1|2|Yığın Kimliği
|2|5|4|Sonraki Yığın

Parçalar, kimlikleri tarafından tanımlanan, üzerlerine dayatılan bir hiyerarşiye sahiptir. Bir 3ds dosyası, Birincil öbek kimliği 4D4Dh'ye sahiptir. Bu her zaman dosyanın ilk öbeğidir. Birincil yığında bulunanlar ana parçalardır.

**Ana Parçalar**

|id|Açıklama
--- | ---
|3D3D|Nesne ağı verilerinin başlangıcı.
|B000|Anahtar kare oluşturucu verilerinin başlangıcı.

Kimlik bloğundan sonraki Sonraki Yığın işaretçisi, bir sonraki Ana yığına işaret eder.
Bir Ana yığından hemen sonra başka bir yığın gelir. Bu, ana parçalar kapsamında izin verilen herhangi bir başka tür yığın olabilir.
Kafes açıklaması (3D3D) için, herhangi bir katları olabilir.

**3D3D'nin alt parçaları - Ağ Bloğu**


|id|Açıklama
--- | ---
|1100|bilinmiyor
|1200|Arka Plan Rengi.
|1201|bilinmiyor
|1300|bilinmiyor
|1400|bilinmiyor
|1420|bilinmiyor
|1450|bilinmiyor
|1500|bilinmiyor
|2100|Ortam Renk Bloğu
|2200|sis?
|2201|sis?
|2210|sis?
|2300|bilinmiyor
|3000|bilinmiyor
|4000|Nesne Bloğu
|7001|bilinmiyor
|AFFF|bilinmiyor

**4000'lik Alt Parçalar - Nesne Açıklama Bloğu**
Subchunk 4000'in ilk öğesi, nesne adının bir ASCIIZ dizisidir.
Bir nesnenin ağ, ışık veya kamera olabileceğini unutmayın.

|id|Açıklama
--- | ---
|4010|bilinmiyor
|4012|gölge?
|4100|Üçgen Çokgen Nesne
|4600|Hafif
|4700|Kamera

## Referanslar

* [Geometri Dosya Biçimleri - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6 -824B-5062C5AE0B32-htm.html)
* [3DS - Wikipedia Tarafından](https://en.wikipedia.org/wiki/.3ds)

