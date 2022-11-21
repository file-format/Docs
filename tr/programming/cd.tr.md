{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","cd dosyası nedir","cd dosyası nasıl açılır", "uzantı", "dosya", "cd dosyası","cd dosya formatı", "cd dosya uzantısı" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio Sınıf Diyagram Dosyası",
  "description":"CD dosya formatı ve CD dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## CD dosyası nedir?

.cd uzantılı bir dosya, geçerli çözümdeki tüm sınıflar arasındaki yapı ve ilişki hakkında bilgi sağlayan bir Visual Studio sınıf diyagram dosyasıdır. Bir Visual Studio çözümü ([.sln](/tr/programming/sln/) ile temsil edilir), her biri birden çok farklı sınıfa sahip bir veya daha fazla proje içerebilir. Sınıf diyagramı dosyası, projeye sağ tıklanarak ve sınıf diyagramı seçeneği seçilerek oluşturulabilir.

## Sınıf Diyagramı (.cd) Dosya Biçimi - Daha Fazla Bilgi

Bir sınıf diyagramı dosyası, bir projedeki sınıfları XML düğümleri olarak temsil eden standart XML dosya biçiminde kaydedilir. Visual Studio kullanılamıyorsa, bu sınıf diyagramı dosyaları, XML dosyalarının açılmasını destekleyen herhangi bir uygulama programında açılabilir.

### Visual Studio Projesine Sınıf Diyagramları Nasıl Eklenir

Visual Studio'da, sınıf diyagramını eklemek istediğiniz Çözümü/Projeyi açın. Ardından, proje düğümüne sağ tıklayın ve ardından Ekle > Yeni Öğe'yi seçin. Veya Ctrl+Shift+A tuşlarına basın.

* Yeni Öğe Ekle iletişim kutusu açılır.

* Ortak Öğeler > Genel'i genişletin ve ardından şablon listesinden Sınıf Diyagramı'nı seçin. Visual C++ projeleri için, Sınıf Diyagramı şablonunu bulmak için Yardımcı Program kategorisine bakın.

### Sınıf Diyagramlarını (CD) Görüntülere Aktar

Visual Studio, sınıf diyagramlarını [PNG](/tr/image/png/), [JPEG](/tr/image/jpeg/) ve [BMP](/tr/image/bmp/) gibi görüntülere dönüştürmeye/dışa aktarmaya izin verir. Bu dışa aktarılan sınıf diyagramı dosyaları, dokümantasyon ve teknik veri paketi (TDP) kayıt tutma amacıyla kullanılabilir. Bir sınıf diyagramını görüntüye dönüştürmek için Microsoft Visual Studio içinden aşağıdaki adımlar kullanılabilir.

1. Sınıf şeması (.cd) dosyanızı açın.
1. Sınıf Diyagramı menüsünden veya diyagram yüzeyi kısayol menüsünden Diyagramı Görüntü Olarak Dışa Aktar'ı seçin.
1. Bir diyagram seçin.
1. İstediğiniz formatı seçin.
1. Dışa aktarmayı bitirmek için Dışa Aktar'ı seçin.

## Referanslar

* [Visual Studio'da Tasarım Dersleri](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

