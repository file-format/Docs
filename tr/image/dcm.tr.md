{
  "date" : "2019-10-11",
  "keywords" :[ "dcm dosyası", "dcm dosya formatı", "dcm dosyası nedir", "dosya", "dcm örneği", "dcm dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCM Dosya Biçimi - Dijital Tıbbi Bilgi Dosyası",
  "description":"DCM dosya biçimi ve DCM dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## DCM dosyası nedir?

.dcm uzantılı dosyalar, MR, CT taramaları ve ultrason görüntüleri gibi hastaların tıbbi bilgilerini depolayan dijital görüntüleri temsil eder. DCM dosyaları, [DICOM](/tr/image/dicom/) (Tıpta Dijital Görüntüleme ve İletişim) görüntü dosyası biçimini kullanır ve referans için hastanın bilgilerini içerebilir. [Ulusal Elektrik Üreticileri Birliği](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) tarafından geliştirilmiştir ve tıbbi görüntülerin dağıtılması ve görüntülenmesi için görüntüleme dosyası biçimini standartlaştırması amaçlanmıştır.

## DCM Dosya Biçimi

DCM dosyaları, bilgileri DICOM görüntü biçiminde depolar. Bu dosyalar, bir DICOM IOD ile ilgili bir SOP örneğini temsil eden gerçek dünya bilgisi olan Veri Kümesini depolar. DICOM Dosyası Meta Bilgisi dosyada depolanır ve ardından gerçek veri setinin bayt akışı gelir.

### DICOM Dosyası Meta Bilgileri ##

Her DICOM dosyası, kapsüllenmiş veri seti için aşağıdakilerden oluşan bir kimlik bilgisi başlığı içerir:
* 128 baytlık bir Dosya Girişi
* 4 bayt DICOM Öneki
* Dosya Meta Öğeleri

Bu başlık, her DICOM dosyası için bir zorunluluktur.

### Dosya Meta Öğeleri ###
|Özellik Adı|Etiket|Tür| Özellik Açıklama
---|---|---|---|
|Dosya Önsözü|Etiket veya Uzunluk Alanı Yok|1|Uygulama Profili veya uygulamaya özel kullanım için sabit 128 baytlık bir alan mevcuttur. Bir Uygulama Profili veya belirli bir uygulama tarafından kullanılmıyorsa, tüm baytlar 00H olarak ayarlanacaktır. Dosya Kümesi Okuyucuları veya Güncelleyicileri, bu Dosyanın bir DICOM Dosyası olup olmadığını belirlemek için bu Girişin içeriğine güvenmeyecektir.
|DICOM Öneki|Etiket veya Uzunluk Alanı Yok|1|"DICM" karakter dizisini içeren dört bayt. Bu Önek, bu Dosyanın bir DICOM Dosyası olup olmadığını anlamak için kullanılmak üzere tasarlanmıştır.
|Dosya Meta Bilgileri Grup Uzunluğu|(0002,0000)|1|Bu Dosya Meta Öğesini (Değer alanının sonu) izleyen ve Grup 2 Dosya Meta Bilgisinin son Dosya Meta Öğesine kadar olan bayt sayısı
|Dosya Meta Bilgileri Sürümü|(0002,0001)|1|Bu, her bitin bu Dosya Meta Bilgileri başlığının sürümünü tanımladığı iki baytlık bir alandır. Sürüm 1'de birinci bayt değeri 00H'dir ve ikinci değer bayt değeri 01H'dir. Bu özelliğin ikinci baytın 0 (lsb) bitinin 1'e ayarlandığı Meta Bilgili Dosyaları okuyan uygulamalar, Dosya Meta Bilgilerini burada belirtilen şekilde yorumlayabilir. PS3.10 sürümü. Diğer tüm bitler kontrol edilmeyecektir.
|Medya Depolama SOP Sınıfı UID|(0002,0002)|1|Veri Kümesi ile ilişkili SOP Sınıfını benzersiz şekilde tanımlar. Medya depolama için izin verilen SOP Sınıfı UID'ler, PS3.4 - Medya Depolama Uygulama Profillerinde belirtilmiştir.
|Medya Depolama SOP Örneği UID|(0002,0003)|1|Dosyaya yerleştirilen ve Dosya Meta Bilgilerini takip eden Veri Kümesi ile ilişkili SOP Örneğini benzersiz olarak tanımlar.
|Aktarım Sözdizimi UID|(0002,0010)|1|Aşağıdaki Veri Kümesini kodlamak için kullanılan Aktarım Sözdizimini benzersiz olarak tanımlar. Bu Aktarım Sözdizimi, Dosya Meta Bilgileri için geçerli değildir.
|Uygulama Sınıfı UID|(0002,0012)|1|Bu dosyayı ve içeriğini yazan uygulamayı benzersiz şekilde tanımlar. Değişim sorunları olması durumunda dosyayı en son yazan uygulama türünün açık bir şekilde tanımlanmasını sağlar.
|Uygulama Sürümü Adı|(0002,0013)|3|Repertuarın en fazla 16 karakterini kullanarak Uygulama Sınıfı UID'si (0002,0012) için bir sürüm tanımlar.
|Kaynak Uygulama Varlığı Başlığı|(0002,0016)|3|Bu dosyanın içeriğini yazan (veya en son güncelleyen) AE'nin DICOM Uygulama Varlığı (AE) Başlığı. Kullanılırsa, ortam değişim sorunları durumunda hataların kaynağının izlenmesine olanak tanır.
|Özel Bilgi Oluşturucu UID'si|(0002,0100)|3|Özel bilgileri oluşturan kişinin UID'si (0002,0102).
|Özel Bilgiler|(0002,0102)|1C|Dosya Meta Bilgilerine yerleştirilen Özel Bilgileri içerir. Oluşturan (0002,0100)'de tanımlanacaktır. Özel Bilgi Oluşturucu UID'si (0002,0100) varsa gereklidir.

### Veri Kümesi Kapsülleme ###

Bir DICOM dosyası, tek bir SOP Sınıfıyla ilgili tek bir SOP Eşgörünümünü temsil eden tek bir Veri Kümesi içerir. DICOM Dosyası Meta Bilgisinin Transfer Söz Dizimi UID'si, Veri Kümesini kodlamak için kullanılan Transfer Sözdizimini tanımlayacaktır.

### Dosya Yönetimi Bilgileri Desteği ###

Ortam Formatı Katmanı, belirli bir DICOM Uygulama Profili için gerekirse aşağıdaki Dosya Yönetimi Bilgilerini sağlar.

* Dosya içeriği sahibi kimliği

* Dosya erişim istatistikleri (örneğin, oluşturma tarihi ve saati)

* Uygulama dosyası erişim kontrolü

* Fiziksel medya erişim kontrolü (örn. yazma koruması)

## Referanslar ##
* [DICOM Standardı](https://www.dicomstandard.org/current/)
* [DICOM Dosya Biçimi](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

