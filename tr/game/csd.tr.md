{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"CSD Steam Oyun Veri Yedekleme Dosyası formatı ve API'ler hakkında bilgi edinin.",
  "title" :"CSD Dosya Formatı - Steam Oyun Veri Yedekleme Dosyası",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Bir CSD dosyası nedir?

Bir CSD dosyası, kullanıcıların **Valve** oyunlarını indirmesine ve yönetmesine izin veren oyun hizmeti **Steam** tarafından oluşturulan bir oyun yedekleme dosyasıdır. Silinen bir oyunu geri yüklemek için kullanılabilecek oyunlarla ilgili yedekleme verilerini içerir. Steam, oyunu yalnızca Steam aracılığıyla indirilmiş, yüklenmiş ve yamalanmışsa bir CSD dosyasından geri yükleyebilir. Oyunu CSD dosyasından geri yüklemek için Steam → Gamesteam'i Yedekle ve Geri Yükle seçeneğini kullanın ve dosyayı seçin.

## CSD Dosya Biçimi - Daha Fazla Bilgi

CSD dosya biçiminin dahili yapısı, herkese açık olarak mevcut değildir ve dosya biçimi belirtimleri, geliştiricinin referansı için mevcut değildir. CSD dosyalarına, yine Steam oyun dosyası biçimleri olan CSM ve ISS dosyaları eşlik eder.

### Steam Yedekleme Dosyaları Nerede Bulunur?

Steam yedekleme dosyalarının tamamı aşağıdaki konumlarda bulunabilir:

* C:\Program Dosyaları (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Özel yapılandırmalar ve yapılandırma betikleri
* \downloads\ - Çok oyunculu oyunlar için özel içerik
* \maps\ - Çok oyunculu oyunlar sırasında yüklenen veya indirilen özel haritalar
* \materials\ - Özel dokular ve kaplamalar
* \SAVE\ - Tek oyunculu kaydedilmiş oyunlar

Ancak, üçüncü taraflarca oluşturulmuş oyunların konumu farklı olabilir ve oyunun geliştiricisi tarafından belirlenir.

### CSD Yedekleme Dosyasından Geri Yükleme

Steam'i yükleyin ve doğru Steam hesabında oturum açın (daha fazla talimat için Steam'i Yükleme bölümüne bakın)
* Steam'i başlatın
* Steam uygulamasının sol üst köşesindeki "Steam" seçeneğine tıklayın
* "Oyunları yedekle ve geri yükle..." seçeneğini seçin
* "Önceki bir yedeği geri yükle"yi seçin
* Oyunun yedek dosyalarının konumuna göz atın
* Gerekli oyunları yüklemek için Steam pencerelerinden devam edin.

## Referanslar

* [Steam Yedekleme Özelliğini Kullanma](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

