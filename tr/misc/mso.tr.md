{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office Makro Referans Dosyası",
  "description":"MSO dosyası ve MSO dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## MSO dosyası nedir?

MSO dosyası, Microsoft Outlook kullanılarak bir HTML mesajı gönderildiğinde oluşturulan bir veri kapsayıcısı dosya biçimidir. Bu çoğunlukla Microsoft Office 2000 uygulamalarında olur. Çoğu durumda, e-posta iletisine **Oledata.mso** dosyası adı eklenir. E-posta alıcısı, böyle bir e-postayı açtığında, aynı yazılım yüklü olmasa bile dosyayı doğru şekilde görüntüleyebilir. MSO dosyaları [Microsoft Bileşik Belge Dosyası Biçimi (MCDF)](https://docs.Microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b) ile ilgilidir.

## Microsoft MSO Dosya Biçimi

MSO dosyaları, Nesne Bağlama ve Gömme (OLE) veya Bileşen Nesne Modeli (COM) yapılandırılmış depolama bileşik dosya uygulaması ikili dosya biçimi olarak da bilinen Microsoft Bileşik Belge Dosya Biçiminde (MCDF) kaydedilir.

### MSO Dosya Biçimi Yapısı

MSO dosya biçiminin dahili dosya biçimi yapısı, [Yapılar](https://docs.Microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd) belgesinde iyi tanımlanmıştır. ) bölümü. Dosya Ayırma Tablosu (FAT), sektör tahsisini ve sektör zincirlerini yönetir. 32 bit sektör numaralarından oluşan bir dizi içerir. Dizideki her indeks bir sektör numarasını temsil ederken, değeri zincirdeki bir sonraki sektörü veya özel bir değeri temsil eder.

## Referanslar

* [COM Yapılandırılmış Depolama](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Bileşik Belge Dosya Biçimi (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

