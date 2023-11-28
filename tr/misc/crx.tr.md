{
"tarih": "2023-06-08",
  "keywords": [
"crx dosyası",
"crx dosyası nedir",
"crx dosyası google chrome'a nasıl yüklenir",
"crx dosyası nasıl açılır",
"crx dosyası neler içerir",
"crx dosyasının formatı nedir",
"dosya",
"crx dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CRX Dosya Formatı - Google Chrome Uzantısı",
  "description":"CRX formatı ve CRX dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"bağlantı başlığı": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"sonmod": "2023-06-08"
}

## .CRX dosyası nedir?

CRX dosya biçimi Google Chrome tarayıcı uzantılarıyla ilişkilidir. CRX dosyası aslında bir uzantının Google Chrome'a yüklenip çalıştırılması için gerekli dosyaları ve meta verileri içeren sıkıştırılmış bir pakettir. Ekstra bir özellik veya tema sağlayarak bir web tarayıcısının işlevselliğini veya görünümünü geliştirir.

Bir CRX dosyası Google Chrome'a indirilip yüklendiğinde, tarayıcı, ortak anahtar ve imzayı kullanarak uzantının bütünlüğünü doğrular. Doğrulama başarılı olursa Chrome, CRX dosyasının içeriğini çıkarır ve uzantıyı yükleyerek kullanıma hazır hale getirir. Kullanıcılar, yüklü uzantıların etkinleştirilmesine, devre dışı bırakılmasına veya kaldırılmasına olanak tanıyan Chrome Uzantıları sayfası aracılığıyla uzantılarını yönetebilir.

## CRX dosyası Google Chrome'a nasıl yüklenir?

Google Chrome'a bir CRX dosyası yüklemek için şu adımları takip edebilirsiniz:

1. Chrome tarayıcısını açın.
2. Adres çubuğuna "chrome://extensions" yazın ve Enter'a basın.
3. Uzantılar sayfasının sağ üst köşesinde bulunan "Geliştirici modu" geçiş anahtarını etkinleştirin.
4. "Ambalajsız yükle" butonuna tıklayın.
5. CRX dosyasının çıkarılan içeriğini içeren klasörü bulun ve seçin (veya yalnızca CRX dosyasının kendisini seçin).
6. Uzantıyı yüklemek için "Aç"a tıklayın.

## CRX dosyası ne içerir?

Bir CRX dosyası, Google Chrome uzantısı için gereken gerekli dosyaları ve meta verileri içerir. CRX dosyasında bulunan tipik içeriklerin bir dökümü aşağıda verilmiştir:

- **Manifest dosyası (manifest.json):** Bu dosya, adı, sürümü, açıklaması, izinleri ve arka plan komut dosyaları gibi uzantıyla ilgili bilgileri içeren JSON biçimli bir dosyadır. Uzantının yapısını ve davranışını tanımlar.
- **JavaScript dosyaları:** Bu dosyalar, uzantının işlevselliğini tanımlayan kodu içerir. Olayları işlemek, web sayfalarını değiştirmek veya Chrome'un API'leriyle etkileşimde bulunmak için komut dosyaları içerebilirler.
- **HTML, CSS ve resim dosyaları:** Uzantılar genellikle açılır pencereler veya seçenek sayfaları gibi kullanıcı arayüzü öğelerini içerir. HTML dosyaları bu arayüzlerin yapısını tanımlarken, CSS dosyaları da görünümlerini kontrol eder. Görüntü dosyaları simgeler veya diğer grafik varlıklar için kullanılır.
- **İsteğe bağlı kaynak dosyaları:** Uzantılar, birden fazla dili desteklemek için yerelleştirme dosyaları gibi ek kaynaklar içerebilir. Bu dosyalar, uzantının kullanıcı arayüzünde kullanılan metnin çevirilerini içerir.
- **Arka plan komut dosyaları:** Bir uzantının arka plan işlemleri veya etkin web sayfasından bağımsız olarak çalışan komut dosyaları varsa, bu komut dosyaları CRX dosyasına dahil edilecektir.
- **İçerik komut dosyaları:** İçerik komut dosyaları, davranışlarını değiştirmek veya içerikleriyle etkileşim kurmak için web sayfalarına eklenebilen komut dosyalarıdır. Uzantı içerik komut dosyaları kullanıyorsa, bu komut dosyaları için gerekli dosyalar CRX dosyasında bulunacaktır.
- **Diğer varlıklar:** Uzantının belirli gereksinimlerine bağlı olarak ses veya video dosyaları, yazı tipleri veya veri dosyaları gibi ek dosyalar dahil edilebilir.

CRX dosya formatı aslında tüm bu dosya ve klasörleri yapılandırılmış bir şekilde içeren sıkıştırılmış bir pakettir. CRX dosyası Google Chrome'a yüklendiğinde, tarayıcı içeriği çıkararak uygun konumlara yerleştirir ve uzantının tarayıcı içinde yüklenmesine ve çalıştırılmasına olanak tanır.

## CRX dosyasının formatı nedir?

CRX dosya formatı, Google Chrome uzantılarını paketlemek ve dağıtmak için özel bir formattır. Aslında farklı dosya uzantılarına sahip sıkıştırılmış bir ZIP arşividir. CRX dosyasının temel yapısı aşağıdaki gibidir:

- **Dosya imzası:** Dosyanın ilk 4 baytı, dosyayı CRX dosyası olarak tanımlamak için imza görevi gören sihirli sayı "Cr24" (onaltılık: 43 72 32 34) içerir.
- **Sürüm numarası:** Sonraki 4 bayt, CRX formatının sürüm numarasını temsil eder.
- **Genel anahtar uzunluğu:** Aşağıdaki 4 bayt, uzantı imza doğrulaması için kullanılan kodlanmış genel anahtarın uzunluğunu belirtir.
- **İmza uzunluğu:** Sonraki 4 bayt, uzantının imza uzunluğunu belirtir.
- **Genel anahtar:** Bu bölüm, uzantının bütünlüğünü doğrulamak için kullanılan kodlanmış genel anahtarı içerir.
- **İmza:** Bu bölüm, uzantının içeriğinin yukarıda belirtilen genel anahtara karşılık gelen özel bir anahtar kullanılarak imzalanmasıyla oluşturulan uzantının imzasını içerir.
- **ZIP arşivi:** CRX dosyasının kalan baytları sıkıştırılmış bir ZIP arşivinden oluşur. Bu arşiv, manifest dosyası, JavaScript dosyaları, HTML dosyaları, CSS dosyaları, resimler ve diğer kaynaklar dahil olmak üzere gerekli tüm dosya ve uzantı klasörlerini içerir.

## Referanslar
* [CRX biçimi spesifikasyonu](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

