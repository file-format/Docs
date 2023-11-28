{
"tarih": "2023-06-12",
  "keywords": [
"bak",
"bak dosyası",
"BAK Krom Yer İmleri",
"bak dosyası nedir",
"bak dosyası nasıl açılır",
"dosya",
"bak dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "BAK Dosya Formatı - Chromium Yer İmleri Yedeği",
  "description":"BAK Chromium Yer İşaretleri formatı ve BAK dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle": "BAK Krom Yer İmleri",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
      "parent": "misc"
}
},
"sonmod": "2023-06-12"
}

## BAK dosyası nedir?

Google Chrome ve Microsoft Edge gibi Chromium tabanlı web tarayıcıları bağlamındaki bir .bak dosyası, aslında yer işaretlerinizin yedek dosyasıdır. Bu yer imleri düz metin listesi olarak kaydedilir ve kullanılan dosya biçimi JSON'dur. Bu .bak dosyalarının amacı, yanlışlıkla silinmesi veya kaybolması durumunda geri yüklenebilecek bir yedekleme sağlayarak yer işaretlerinizi korumaktır.

Google Chrome da dahil olmak üzere Chromium tabanlı tarayıcılar bu yedekleme dosyalarını rutin olarak oluşturur ve bunlara genellikle "Bookmarks.bak" adını verir. Bunlar aslında yer işaretlerinizin belirli bir zamandaki anlık görüntüsüdür.

## Yer işaretlerinizi geri yüklemek için .bak dosyası nasıl kullanılır?

1. **Yedekleme dosyasını bulun:** Bu dosya genellikle Chromium profilinizle ilişkili belirli bir klasörde bulunur. Tam konum, işletim sisteminize bağlı olarak değişebilir.

Windows'ta: `C:\Kullanıcılar\'a bakın<YourUsername> \AppData\Local\Chromium\Kullanıcı Verileri\Default\Bookmarks.bak`.

MacOS'ta: "~/Library/Application Support/Chromium/Default/Bookmarks.bak" konumunda arama yapın.

Linux'ta: '~/.config/chromium/Default/Bookmarks.bak'ı kontrol edin.

3. Chromium tarayıcınızın kapalı olduğundan emin olun.
4. ".bak" uzantısını kaldırarak "Bookmarks.bak" dosyasını yeniden adlandırın; böylece dosyaya "Yer İşaretleri" adı verilir.
5. Chromium'u başlatın.

.bak dosyasını "Yer İşaretleri" olarak yeniden adlandırdığınızda Chromium, dosyayı mevcut yer işaretleri dosyası olarak kullanır ve önceki yer işaretleriniz geri yüklenmelidir.

## Chromium Yer İmleri Yedekleme

Chromium yer işaretlerinizi yedeklemek, kayıtlı önemli web sayfalarınızı ve URL'lerinizi kaybetmemenizi sağlamak için akıllıca bir önlemdir. Chromium, Google Chrome ve Microsoft Edge gibi diğer tarayıcılar için temel görevi gören açık kaynaklı bir tarayıcıdır. Chromium yer işaretlerinizi yedeklemek için şu adımları izleyin:

## Yöntem 1: Manuel Yedekleme

1. **Chromium'u açın**: Bilgisayarınızda Chromium tarayıcısını başlatın.

2. **Yer İşaretlerine Erişim**: Tarayıcı penceresinin sağ üst köşesindeki üç dikey noktaya (menü simgesi) tıklayın. Yer imleri alt menüsünü görüntülemek için açılır menüden "Yer İşaretleri"nin üzerine gelin.

3. **Yer İmlerini Dışa Aktar**: Yer imleri alt menüsünde "Yer İşareti yöneticisi"ni tıklayın. Bu, yer işaretlerinizi gösteren yeni bir sekme açacaktır.

4. **Yer İmlerini Dışa Aktar**: Yer imi yöneticisi sekmesinde, yer imleri yöneticisi menüsünü açmak için tekrar üç dikey noktaya (genellikle sağ üst köşede) tıklayın. Bu menüden "Yer işaretlerini dışa aktar"ı seçin.

5. **Konum Seçin**: Dışa aktarılan yer işaretleri dosyasını bilgisayarınızda nereye kaydetmek istediğinizi seçin. Varsayılan dosya adı "bookmarks.html"dir ancak isterseniz bunu değiştirebilirsiniz. Hatırlayacağınız bir yere kaydedin.

6. **Kaydet**: Yer işaretlerinizi HTML dosyası olarak kaydetmek için "Kaydet" veya "Dışa Aktar" düğmesini tıklayın.

Yer işaretleriniz artık bir HTML dosyası olarak yedeklendi. Bu dosyayı koruma amacıyla harici bir sürücüye veya bulut depolama alanına kopyalayabilirsiniz.

## Yöntem 2: Google Hesabıyla Senkronizasyon (varsa)

Chromium'da bir Google hesabında oturum açtıysanız yer işaretlerinizi güvende tutmak ve cihazlar arasında senkronize etmek için yerleşik senkronizasyon özelliğini de kullanabilirsiniz. Bu şekilde yer işaretleriniz otomatik olarak Google hesabınıza yedeklenecektir.

1. **Chromium'u açın**: Chromium tarayıcısını başlatın ve Google hesabınızda oturum açtığınızdan emin olun.

2. **Senkronizasyonu Etkinleştir**: Tarayıcı penceresinin sağ üst köşesindeki üç dikey noktayı (menü simgesi) tıklayın ve "Ayarlar"a gidin.

3. **Senkronizasyon ve Google hizmetleri**: Ayarlar sekmesinde, sol kenar çubuğundaki "Senkronizasyon ve Google hizmetleri"ni tıklayın.

4. **Verilerinizi Senkronize Edin**: "Senkronizasyon" altında, "Yer İmleri"nin açık olduğundan emin olun. Bu, yer işaretlerinizi Google hesabınızla senkronize edecektir.

Yer işaretleriniz artık otomatik olarak yedeklenecek ve Google hesabınızla senkronize edilecektir. Chromium'a sahip herhangi bir cihazda veya Google senkronizasyonunu destekleyen başka bir tarayıcıda Google hesabınızda oturum açarak bunlara erişebilirsiniz.

Özellikle yalnızca Google hesabınızın senkronizasyonuna bağlı olmayan yerel bir kopya istiyorsanız, yer işaretlerinizi periyodik olarak manuel olarak da yedeklemeyi unutmayın.

## BAK dosyası nasıl açılır

Yer imleri yedeklemenizin ham verilerini keşfetmek istiyorsanız, "Bookmarks.bak" dosyasını Microsoft Visual Studio Code (birden fazla platformda mevcuttur), Microsoft Notepad (Windows kullanıcıları için), Apple TextEdit gibi çeşitli metin düzenleyicilerle açabilirsiniz. (Mac kullanıcıları için) veya seçtiğiniz başka bir metin düzenleyicisini kullanın. Bunu yapmak, dosyada bulunan yer işaretlerini ve meta verileri görüntülemenize olanak tanır.

Çeşitli metin düzenleme yazılımlarını ve kod düzenleyicileri kullanarak "Bookmarks.bak" dosyasını açabilir ve içeriğini görüntüleyebilirsiniz. Yaygın olarak kullanılan bazı seçenekler şunlardır:

1. Visual Studio Kodu (VS Kodu)
2. Not Defteri (Windows)
3. TextEdit (Mac)
4. Yüce Metin
5. Not Defteri++
6.Atom
7. nano ve Vim (Linux)
8. WordPad (Windows)

## Diğer BAK dosyaları

**.bak** dosya uzantısını kullanan diğer dosya türleri şunlardır.

**Veri tabanı**
- [BAK - Veritabanı Yedekleme Dosyası](/tr/database/bak/)
- [BAK - Hızlı Sayfa Yasası! Veritabanı Yedeklemesi](/tr/database/bak-act/)
- [BAK - Microsoft SQL Server Veritabanı Yedeklemesi](/tr/database/bak-sqlserver/)

**Oyun**
- [BAK - Terraria Dünyası veya Oyuncu Yedeklemesi](/tr/game/bak-terraria/)

**Çeşitli**
- [BAK - Yedekleme Dosyası](/tr/misc/bak-backup/)
- [BAK - Final 2012 Puan Yedeklemesi](/tr/misc/bak-finale/)
- [BAK - MobileTrans Yedeklemesi](/tr/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Projesi Yedeklemesi](/tr/misc/bak-vegas/)

**Ayarlar**
- [BAK - Holo Başlatıcı Yedeği](/tr/settings/bak-holo/)

## Referanslar
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
