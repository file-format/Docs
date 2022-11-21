{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","yaml dosyası nedir","yaml dosyası nasıl açılır", "uzantı", "dosya", "yaml dosyası","yaml dosya formatı", ".yaml uzantısı" , "yaml vs json" ,"YAML dosyası örneği", "docker yaml dosyası örneği"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" YAML dosya formatı ve YAML dosyası oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"YAML Dosya Biçimi",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## YAML dosyası nedir? ##

**YAML dosyası**, Unicode tabanlı bir veri serileştirme dili olan YAML (YAML Ain't Markup Language) dilinden oluşur; yapılandırma dosyaları, internet mesajlaşması, nesne kalıcılığı vb. için kullanılır. YAML, dosyaları için .yaml uzantısını kullanır. Sözdizimi, belirli bir programlama dilinden bağımsızdır. Temel olarak YAML, insan etkileşimi için ve modern programlama dilleriyle iyi çalışacak şekilde tasarlanmıştır. İsteğe bağlı yerel veri yapılarını serileştirme desteği, YAML dosyalarının okunabilirliğini artırdı, ancak ayrıştırma ve dosya oluşturma sürecini biraz karmaşık hale getirdi.

## Kısa Tarih ##

YAML ilk olarak 2001 yılında önerildi ve Clark Evans, Ingy döt Net ve Oren Ben-Kiki tarafından geliştirildi. YAML'nin ilk olarak bir biçimlendirme dili olarak amacını belirtmek için "Başka Bir İşaretleme Dili" anlamına geldiği söylendi. Daha sonra, amacının veri odaklı olduğunu belirtmek için "YAML İşaretleme Dili Değildir" olarak yeniden tasarlandı.


## YAML Dosya Biçimi ##

YAML dosyası aşağıdaki veri türlerinden oluşur

- **Skaler**: Skaler; Dizeler, Tamsayılar, Boolean'lar vb. değerlerdir.
- **Diziler**: Sıralar, her öğenin kısa çizgi (-) ile başladığı listelerdir. Listeler iç içe de olabilir.
- **Eşlemeler**: Eşleme, anahtarları değerlerle listeleme yeteneği sağlar.

### Sözdizimi ###

- **Boşluk**: Boşluk girintisi, yuvalamayı ve genel yapıyı belirtmek için kullanılır.

```yaml
isim: John Smith
İletişim:
ev: 1012355532
ofis: 5002586256
adres:
sokak: |
123 Kasırga Sokağı
Süit 16
şehir: Doğu Centerville
eyalet: KS
```

- **Yorumlar**: Yorumlar "#" simgesiyle başlayarak yazılır.

```yaml
# Bu bir YAML Yorumudur
```

- **Listeler**: Tire (-), her üyenin ayrı bir satırda olduğu liste üyelerini belirtmek için kullanılır. Liste üyeleri ayrıca köşeli parantezler ([...]) içine alınabilir ve üyeler virgülle (,) ayrılır.

```yaml
  - A
  - B
  - C
```

```yaml
[A, B, C]
```

- **İlişkili Dizi**: Bir ilişkisel dizi, kıvrımlı parantezler ({...}) ile çevrilidir. Anahtarlar ve değerler iki nokta üst üste (:) ile ayrılır ve her bir çift virgül (,) ile ayrılır.

```yaml
  {name: John Smith, age: 20}
```

- **Dizeler**: Dize, çift tırnak (") veya tek tırnak (') ile veya bunlar olmadan yazılabilir.

```yaml
Örnek Dizi
"Örnek Dizi"
"Örnek Dizi"
```

- **Skaler Blok içeriği**: Skaler içerik, aşağıdakiler kullanılarak blok notasyonunda yazılabilir:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
veri: |
YAML
(YAML İşaretleme Dili Değildir)
bir veri serileştirme dilidir
```

```yaml
veri: ?
YAML (YAML Biçimlendirme Dili Değildir)
bir veri serileştirme dilidir
```

- **Birden Çok Belge**: Birden çok belge, tek bir akışta üç tire (---) ile ayrılır. Tireler, belgenin başlangıcını gösterir. Kısa çizgiler, direktifleri belge içeriğinden ayırmak için de kullanılır. Belgenin sonu üç nokta (...) ile gösterilir.

```yaml
  ---
Belge 1
  ---
Belge 2
...
```

- **Type**: Değerin türünü belirtmek için çift ünlem işareti (!!) kullanılır.

```yaml
a: !!kayan 123
b: !!str 123
```

- **Etiket**: Bir nota etiket atamak için bir ve işareti (&) kullanılır ve bu düğüme referans vermek için bir yıldız işareti (*) kullanılır.

```yaml
isim: John Smith
fatura adresi: &id01
sokak: |
123 Kasırga Sokağı
Süit 16
şehir: Doğu Centerville
eyalet: KS

Gönderim yeri: *id01
```

- **Yönergeler**: YAML belgelerinden önce bir akışta yönergeler gelebilir. Yönergeler yüzde işaretiyle (%) başlar, ardından ad ve ardından boşluklarla ayrılmış parametreler gelir.

```yaml
%YAML 1.2
  ---
Belge içeriği
```
## YAML dosyası örneği
Aşağıda bir **docker yaml dosyası örneği** görebilirsiniz:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML ve JSON
Temel olarak, hem JSON hem de YAML, insanlar tarafından okunabilen bir veri değişim formatı sağlamak için geliştirilmiştir. YAML, JSON biçiminin bir üst kümesi olarak gerçekleştirilir. Bu, bir YAML ayrıştırıcısı kullanarak JSON'u ayrıştırabileceğimiz anlamına gelir. Bu teorinin pratik uygulaması biraz zor olsa da. Bu nedenle, YAML ve JSON arasındaki bazı temel farklılıklar aşağıda verilmiştir:

|YAML| JSON|
---|---|
|Serileştirilmiş verileri ayrıştırmanın karmaşık ve zaman alıcı süreci |Daha basit tasarımıyla JSON serileştirilmiş verileri hızlı ve kolay bir şekilde ayrıştırın|
|Daha az topluluk desteği| Daha geniş topluluk desteği ve popülaritesi |
|Yorumları destekler| Yorumları desteklemiyor |
|Diğer veri nesnelerinin referansını kullanabilme| Karmaşık yapıları nesne referanslarıyla seri hale getirmek imkansız|
|Hiyerarşi çift boşluk karakterleri kullanılarak gösterilir. Sekme karakterlerine izin verilmez|Nesneler ve Diziler köşeli ayraçlar ve parantezler içinde gösterilir.|
|Dize tırnaklar isteğe bağlıdır ancak tek ve çift tırnakları destekler.|Dizeler çift tırnak içinde olmalıdır.|
|Kök düğüm, geçerli veri türlerinden herhangi biri olabilir|Kök düğüm, bir dizi veya bir nesne olmalıdır.|


## Referanslar ##

- [YAML - Vikipedi](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

