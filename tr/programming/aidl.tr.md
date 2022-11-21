{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL Dosyası - Android Arayüz Tanımlama Dili Dosyası",
  "description":"AIDL dosyalarını oluşturabilen ve açabilen örnek ve API'lerle AIDL dosya formatının ne olduğunu öğrenin.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## AIDL dosyası nedir?

Bir AIDL (Android Arayüz Tanımlama Dili) dosyası, Android geliştiricilerinin farklı uygulamalar arasında iletişim kurmasına olanak tanır. Programlama arabirimine bağlı olarak, hem istemci hem de hizmet, süreçler arası iletişim (IPC) kullanarak iletişim kurmayı kabul eder. AIDL dosyası, uygulamalar arasındaki iletişim için bu arayüzleri ve sözleşmeleri tanımlamak için [Java](/tr/programming/java/) kaynak kodunu içerir.

AIDL dosyalarını Google Android Studio veya Microsoft Notepad ve Notepad++ gibi herhangi bir metin düzenleyiciyle açabilirsiniz.

## AIDL Dosya Biçimi - Daha Fazla Bilgi

AIDL, uygulamalar arasındaki iletişim için arabirimleri içeren metin dosyalarıdır. Android işletim sistemi, bir işlemin başka bir işlemin belleğine erişmesine izin vermez. Bu, süreçlerin, temeldeki işletim sistemini anlamak için nesnelerini ilkel parçalara ayırmasına ve geliştirici için iletişim yapılarının sürecini oluşturmasına yol açar.

### AIDL tarafından hangi Veri Türleri desteklenir?

AIDL, varsayılan olarak aşağıdaki veri türlerini destekler.

* Java programlama dilindeki tüm ilkel türler (int, long, char, boolean vb.)
* Sicim
* Karakter Dizisi
* Liste
* Harita

## AIDL Dosya Örneği

Aşağıda örnek bir AIDL dosyası bulunmaktadır.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Referanslar

* [Android Arayüz Tanımlama Dili (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

