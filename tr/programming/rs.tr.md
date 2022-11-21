{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "dosya", "uzantı", "dosya formatı", "Rust programlama dili", "Programlama Kılavuzu", "RS örneği", "Rust", "VBScript"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Rust Programlama Dosyası",
  "description":"RS dosya formatı ve RS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## .rs dosyası nedir?

RS uzantılı bir dosya, Rust programlama diline aittir, performans ve güvenlik, özellikle güvenli güvenlik için tasarlanmış çok yönlü, üst düzey, genel kullanıcı programlama dilidir. Rust, sözdizimsel olarak С++'a benzer, ancak referansları doğrulamak için bir ödünç alma denetleyicisi kullanarak bellek güvenliğini garanti edebilir. Rust dili, çöp toplama olmaksızın bellek güvenliğini sağlar ve referans sayma normaldir.

## RS Dosya Biçimi ##

Rust ilk olarak Mоzilla Reseаrсh'ta Grаydоn Hоаre tarafından Dаve Hermаn, Brendаn Eiсh ve diğerlerinin katkılarıyla tasarlandı. Endüstride artan bir kullanım kazandı ve Microsoft, güvenli ve güvenlik açısından kritik yazılım bileşenleri için dili deniyor.

Rust, 2021 anketine katılanların yalnızca %7'si tarafından kullanılmasına rağmen, 2016'dan beri her yıl Stask Verflоw Geliştirici Anketinde "en sevilen programlama dili" olarak seçilmiştir. 0.4 sürümünden önceki geleneksel statik etiketleme ile birlikte, Rust ayrıca lastikleri de destekledi.

Lastik sistemi, özel bir kontrol ifadesi kullanılarak program ifadelerinden önce ve sonra iddiaları modellemiştir. Tutarsızlıklar, С veya С++ kodundaki iddialarda olduğu gibi, çalışma zamanında değil, tam zamanında keşfedilebilir. Lastik kavramı, ilk olarak NIL dilinde tanıtıldığı için Rust'a özgü değildi. Lastikler kaldırıldı, çünkü pratikte çok az kullanıldılar, ancak aynı işlevsellik Rust'ın taşıma anlamlarından yararlanılarak elde edilebilir.

Rust programlama dili, daha hızlı, daha güvenilir yazılım yazmanıza yardımcı olur. Yüksek seviyeli ergonomi ve düşük seviyeli kontrol, programlama dili tasarımında genellikle çelişkilidir; Rust, çatışan zorluklara meydan okur. Dengeli, güçlü teknik beceriklilik ve harika bir geliştirici deneyimi sayesinde, Rust size düşük düzeyli ayrıntıları (bellek kullanımı gibi) geleneksel olarak ortaya çıkan tüm zorluklar olmadan kontrol etme olanağı sağlar.

 

## Kısa Tarih ##

Dil, 2006 yılında Mоzilla çalışanı Grаydоn Hоаre tarafından başlatılan kişisel bir projeden doğdu ve projeye muhtemelen mantarların paslı ailesinden adının verildiğini belirtti. Mоzilla projeyi 2009'da desteklemeye başladı ve 2010'da duyurdu. İlk kararlı sürüm olan Rust 1.0, 15 Mayıs 2015'te yayınlandı. sürümler, ardından altı hafta süren beta sürümlerle test edildi. 6 Nisan 2021'de Google, Аndroid Oрen Sоurсe Рrоjeсt içinde Rust için С/С++'ya bir alternatif olarak suрроrt duyurdu.

## Teknik Şartname ##

Rust, son derece tutarlı ve son derece güvenli sistemler ve büyük ölçekte programlama, yani büyük sistem bütünlüğünü koruyan sınırlar oluşturma ve sürdürme için bir dil olarak tasarlanmıştır. Bu, güvenliğe, bellek düzeninin kontrolüne ve tutarlılığa vurgu yapan bir özellik setine yol açtı.


Rust dili bellek açısından güvenli olacak şekilde tasarlanmıştır. Boş sınırlayıcılara, sarkan sınırlayıcılara veya veri yarışlarına izin vermez. Veri değerleri, yalnızca tümü girdilerinin önceden başlatılmasını gerektiren sabit bir form seti aracılığıyla başlatılabilir. Bağlantılı liste veya ikili ağaç veri yapılarında olduğu gibi geçerli veya NULL olan listeleri çoğaltmak için, Rust veri kitaplığı bir seçenek türü sağlar. Rust, yaşam sürelerini yönetmek için sözdizimi ekledi. Güvenli olmayan kod, güvensiz anahtar sözcüğünü kullanarak bu kısıtlamalardan bazılarını alt üst edebilir.


Rust dili otomatik çöp toplama kullanmaz. Bellek ve diğer kaynaklar, kaynak toplama, orijinal referans sayımı ile başlatma kuralıyla yönetilir.


Rust, çok düşük ek yük ile kaynakların deterministik yönetimini sağlar. Rust, değerlerin yığınla tahsisini tercih eder ve örtülü boksu yeniden gerçekleştirmez. Çalışma zamanı referans sayımını içermeyen referansların (simgeyi kullanan) kavramı vardır. Bu tür sınırlayıcıların güvenliği, sarkan sınırlayıcıları ve diğer tanımsız davranış biçimlerini önleyerek tam zamanında doğrulanır.


Rust, tüm değerlerin benzersiz bir sahibi olduğu bir sahiplik sistemine sahiptir. Değerler değişmez referansla, &T kullanılarak, değişken referansla, & mut T kullanılarak veya değere göre, T kullanılarak taşınabilir.


## RS Dosya Biçimi Örneği ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Referans ##

* [RS - Wikipedia'dan](https://en.wikipedia.org/wiki/Rust_(programming_language))



