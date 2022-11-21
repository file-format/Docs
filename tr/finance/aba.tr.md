{
  "date" : "2019-10-11",
  "keywords" :[ "aba dosyası", "aba dosya biçimi", "aba dosyası nedir", "dosya", "aba örneği", "aba dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - CemText Dosya Formatı",
  "description":"ABA dosya formatı ve ABA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## ABA dosyası nedir?

.aba uzantılı bir dosya, bankalar tarafından toplu işlemler için kullanılan bir Avustralya Bankacılar Birliği (ABA) veya [Cemtext](https://www.cemtexaba.com/) dosya biçimidir. Bankaların çoğu tarafından mali kayıt tutmak için kullanılır. Doğrudan Giriş dosyası olarak da bilinen ABA dosya formatı, Avustralya bankalarının çoğu tarafından toplu işlemler için varsayılan format olarak benimsenmiştir. Bank of Queensland, NAB ve Westpac tarafından kullanılmasına rağmen hala Standart format olarak kabul edilmemiştir. ABA dosyaları, Notepad++ gibi herhangi bir metin düzenleyiciyle açılabilir.


## ABA Dosya Biçimi

Bir ABA dosyası, bankacılık sistemlerine iletmek veya yüklemek üzere verileri depolamak için ASCII formatını kullanır. Biçim, toplu işlemleri işlemek için şirketlerin kendi finansal sistemlerine entegrasyonu kolaylaştırmak için basit tutulmuştur. Örneğin, bir bordro sisteminde, tek seferde işlenmek üzere bir grup işlem yüklenebilir. ABA dosya biçimi belirtimleri, [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) web sitesinde tam transkript olarak mevcuttur ve geliştiricilerin referansı için başvurulabilir .

Bir ABA dosyası, her satırın "kayıt" olarak bilindiği birden çok satırdan oluşur. Bir ABA dosyasında üç ana kayıt vardır:

* Açıklayıcı Kayıt
* Detay Kaydı
* Dosya Toplam Kaydı

### Açıklayıcı Kayıt

Bir `Tanımlayıcı Kayıt` Makara Sıra Numarası, Kullanıcının Finans Kuruluşunun Adı, Dosya sağlayan Kullanım Adı ve diğer bilgileri içerir.

### Detay Kaydı

`Detay Kaydı` tipinde Banka/Eyalet/Şube Numarası, alacak/borçlandırılacak Hesap numarası, Gösterge, İşlem Kodu, Tutar gibi bilgiler yer alır.

### Dosya Toplam Kaydı

"Dosya Toplam Kaydı" tipi, Kayıt Tipi 7, BSB Format Doldurucu, Dosya (Kullanıcı) Net Toplam Tutar, Dosya (Kullanıcı) Kredi Toplam Tutarı, Dosya (Kullanıcı) Borç Toplam Tutarı ve diğer bilgileri içerir.

### İşlem Kodları

Geçerli işlem kodlarının listesi aşağıdaki gibidir. ABA dosyalarında çoğu zaman "53 - Pay" kodu kullanılmaktadır. Bu işlem kodları borçları, kredileri ve stopaj vergilerini kapsar.

|Kod|İşlem Açıklaması|
---|---|
|13|Harici olarak başlatılan borç kalemleri|
|50|İşlem Kodu taşıyanlar hariç, dışarıdan başlatılan kredi kalemleri|
|51|Avustralya Hükümeti Güvenlik Menfaati|
|52|Aile Ödeneği|
|53|Ödeme|
|54|Emeklilik|
|55|Parti|
|56|Temettü|
|57|Tahvil/Senet Faizi|

## ABA Dosyası Örneği

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referanslar

* [Cemtext ABA](https://www.cemtexaba.com/)

