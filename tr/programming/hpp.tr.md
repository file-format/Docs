{
"tarih": "2023-06-08",
  "keywords": [
"hpp dosyası",
"hpp dosyası nedir",
"hpp dosyası neler içerir",
"hpp dosyası örneği",
"hpp dosyasının formatı nedir",
"dosya",
"hpp dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "HPP Dosya Formatı - C++ Başlık Dosyası",
  "description":"HPP dosyalarını oluşturabilen ve açabilen HPP formatı ve API'ler hakkında bilgi edinin.",
"linktitle": "HES",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"sonmod": "2023-06-08"
}

## .HPP dosyası nedir?

".hpp" dosya formatı, C++ programlama dilinde başlık dosyaları için yaygın olarak kullanılır. Başlık dosyaları genellikle C++ projesinde diğer kaynak kod dosyaları tarafından kullanılan işlevlerin, sınıfların, değişkenlerin ve sabitlerin bildirimlerini ve tanımlarını içerir.

Başlık dosyalarını kullanmanın amacı, kodun kendisini çoğaltmadan, birden fazla kaynak kod dosyasında ortak kodu paylaşmanın bir yolunu sağlamaktır. C++ kaynak dosyasının başlık dosyasındaki bildirimlere veya tanımlara erişmesi gerektiğinde, `#include' önişlemci yönergesini kullanarak başlık dosyasını içerir.

".hpp" dosya uzantısı genellikle bir dosyanın C++ başlık dosyası olduğunu belirtmek için kullanılır. Başlık dosyaları için bu özel uzantıyı kullanmak zorunlu değildir, ayrıca ".h" veya başka uzantılara sahip başlık dosyalarıyla da karşılaşabilirsiniz. Uzatma seçimi büyük ölçüde bir gelenek ve kişisel tercih meselesidir.

Bir C++ kaynak dosyası #include kullanarak başlık dosyasını içerdiğinde, derleyici başlık dosyasının içeriğini bir birim olarak derlemeden önce kaynak dosyayla etkili bir şekilde birleştirir. Bu, kaynak dosyanın başlık dosyasındaki bildirimlere ve tanımlara erişmesine olanak tanır ve derleyicinin tür denetimi ve kod oluşturması için gerekli bilgileri sağlar.

## HPP dosyası ne içerir?

".hpp" dosyasında bulabileceğiniz bazı genel içerikler şunlardır:

- **İşlev bildirimleri:** Başlık dosyaları genellikle gerçek uygulamaları olmayan işlev bildirimlerini içerir. Bu bildirimler işlevin adı, dönüş türü ve parametreleri hakkında bilgi sağlayarak diğer kaynak kod dosyalarının uygulama ayrıntılarını bilmeye gerek kalmadan işlevi kullanmasına olanak tanır.
- **Sınıf bildirimleri:** Başlık dosyaları, sınıf adı, üye değişkenleri, üye işlevleri ve erişim belirticileri dahil olmak üzere sınıf bildirimlerini içerebilir. Başlık dosyasına sınıf bildirimini dahil ederek, diğer kaynak kod dosyaları o sınıfın nesnelerini oluşturabilir ve üyelerine erişebilir.
- **Sabit bildirimler:** Başlık dosyaları, birden fazla kaynak kod dosyasında paylaşılması amaçlanan genel değişkenler veya numaralandırma değerleri gibi sabitleri tanımlayabilir. Bu sabitlere, diğer kaynak dosyalara başlık dosyası eklenerek ve bunların tanımlanmış sabitleri kullanmalarına izin verilerek erişilebilir.
- **Tür tanımları:** Başlık dosyaları, "typedef" anahtar sözcüğünü kullanan tür tanımlarını veya "using" anahtar sözcüğünü kullanan tür takma adlarını içerebilir. Bu tanımlar, mevcut türler için yeni adlar oluşturarak kodu daha okunabilir ve bakımı kolay hale getirir.
- **Satır içi işlev tanımları:** Bazı durumlarda başlık dosyaları satır içi işlev tanımları içerebilir. Satır içi işlevler, ayrı bir işlev olarak çağrılmak yerine çağrı sitesinde genişletilen küçük işlevlerdir. Başlık dosyasına satır içi işlev tanımının dahil edilmesi, derleyicinin işlev çağrısını doğrudan işlev gövdesiyle değiştirmesine olanak tanır ve potansiyel olarak performansı artırır.

## HPP Dosya Örneği

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## HPP dosyasının formatı nedir?

HPP düz bir metin dosyasıdır ancak C++ programlama dilinin genel kurallarına ve sözdizimine uyar. ".hpp" dosyasının genel formatı ve yapısının bir dökümü aşağıda verilmiştir:

- **Başlık korumaları:** Genellikle bir ".hpp" dosyası, aynı dosyanın birden fazla eklenmesini önlemek için başlık korumalarıyla başlar. Bu, '#ifndef', '#define' ve '#endif' gibi önişlemci direktifleri kullanılarak gerçekleştirilir. Başlık koruması, dosya içeriğinin derleme işlemi sırasında yalnızca bir kez dahil edilmesini sağlar.
- **İfadeleri dahil et:** Başlık korumalarından sonra, `#include' direktifini kullanarak diğer gerekli başlık dosyalarını ekleyebilirsiniz. Bunlar, standart kitaplık başlıklarını veya kodunuzun gerektirdiği diğer özel başlıkları içerebilir.
- **Bildirimler ve Tanımlar:** ".hpp" dosyasının birincil içeriği, bildirimler ve bazı durumlarda sınıfların, işlevlerin, sabitlerin, tür takma adlarının ve diğer öğelerin tanımlarıdır. Örneğin, sınıfları 'class' anahtar sözcüğünü kullanarak, işlevleri dönüş türlerini, adlarını ve parametre listesini kullanarak ve sabitleri ise 'const' anahtar sözcüğünü ve ardından türlerini ve adlarını kullanarak bildirebilirsiniz.
- **Satır İçi İşlev Tanımları:** Bazı durumlarda satır içi işlev tanımlarını doğrudan ".hpp" dosyasına ekleyebilirsiniz. Satır içi işlevler genellikle sınıf gövdesi içinde tanımlanır; bu, işlev tanımının bildiriminin yanında yer aldığı anlamına gelir. Bu, işlev tanımının önüne 'satır içi' anahtar sözcüğü getirilerek yapılabilir.
- **Ad Alanı Bildirimleri:** Kodunuzda ad alanları kullanıyorsanız, bunları ".hpp" dosyasında bildirebilirsiniz. Bu, 'ad alanı' anahtar sözcüğü ve ardından ad alanı adı kullanılarak ve ilgili kodun ad alanı bloğuna eklenmesiyle yapılır.

## Referanslar
* [Başlık dosyaları (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

