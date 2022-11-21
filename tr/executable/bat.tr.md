{
  "date" : "2021-06-24",
  "keywords" :[ "bat dosyası", "bat dosyası nedir", "dosya", "bat dosyası örneği", "uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"BAT dosya formatı ve BAT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"BAT - Toplu Dosya Biçimi",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## BAT dosyası nedir?
BAT dosyası, cmd.exe altında DOS ve Windows'un tüm sürümleriyle çalışan bir toplu iş dosyası olarak bilinir. Windows içinde bakım yardımcı programlarını çalıştırmak veya tipik programları başlatmak gibi farklı görevleri gerçekleştirmek için komut satırı yorumlayıcısı tarafından yürütülecek düz metin halinde bir dizi satır komutundan oluşur. Bir toplu iş dosyası, yorumlayıcı tarafından etkileşimli olarak kabul edilebilecek herhangi bir komutu içerebilir ve toplu iş dosyası içinde yazıldığı şekliyle koşullu dallanma ve döngüye olanak sağlayan kod yapısını kullanabilir.
## BAT dosya biçimi
Bir BAT dosya formatı, doğası gereği tekrar eden komut dizilerini otomatikleştirmek için dahil edilmiş basit bir betiktir. "Batch" terimi, toplu işleme için kullanılır, "etkileşimsiz yürütme" olarak kabul edilebilir. Bu nedenle, bir toplu iş dosyası birden fazla veri toplu işleyemez. Eski Disk İşletim Sisteminde (DOS), toplu iş dosyası, dosya adı ve .bat uzantısı yazılarak komut satırı arayüzü altında çalıştırılıyordu. Microsoft Windows gibi önceki Microsoft grafik arabirim tabanlı işletim sistemi DOS'a bağımlıydı. Kullanıcıların Windows'u onarma, optimize etme veya yeniden yükleme gibi tipik işlemleri gerçekleştirmek için DOS'u kullanması gerekiyordu. Daha sonra Microsoft, DOS işletim sistemine bağımlı olmayan Windows NT'yi piyasaya sürdü. Bu nedenle toplu iş dosyaları, modern Microsoft işletim sistemlerinde Komut İstemi veya **cmd.exe** kullanılarak çalıştırılabilir.
### Toplu dosya parametreleri
Komut istemi, toplu işin adına ve yoluna ve toplu işin içinden çağrılan dokuz parametreye başvurmak için **%0, %1 - %9** gibi bir dizi özel değişkeni destekler. Var olmayan parametreler, sıfır uzunluğa sahip bir dize ile değiştirilir. Bununla birlikte, ortam değişkenlerine benzer şekilde kullanılabilirler, ancak ortama kaydedilmezler. Microsoft ve IBM bu değişkenleri değiştirme parametreleri olarak adlandırırken, Novell, Digital Research ve Caldera onlar için değiştirme değişkenleri terimini tanıttı.

İşte bazı yararlı Batch dosyası komutları:
| komut | Açıklama |
------|------------|
| VER | Bu toplu iş komutu, kullanmakta olduğunuz MS-DOS sürümünü gösterir. |
|ASSOC| Bu, bir uzantıyı bir dosya türüyle (FTYPE) ilişkilendiren, mevcut ilişkilendirmeleri görüntüleyen veya bir ilişkilendirmeyi silen bir toplu komuttur. |
|CD| Bu toplu iş komutu, farklı bir dizinde değişiklik yapılmasına yardımcı olur veya geçerli dizini görüntüler. |
|CLS| Bu toplu komut ekranı temizler. |
|KOPYA| Bu toplu iş komutu, dosyaları bir konumdan diğerine kopyalamak için kullanılır. |
|SİL| Bu toplu iş komutu dizinleri değil dosyaları siler. |
|DIR| Bu toplu iş komutu, bir dizinin içeriğini listeler. |
|TARİH| Bu toplu komut, sistem tarihini bulmaya yardımcı olur. |
|EKO| Bu toplu komut, mesajları görüntüler veya komut yankısını açar veya kapatır. |
|ÇIKIŞ| Bu toplu iş komutu, DOS konsolundan çıkar. |
|MD| Bu toplu iş komutu, geçerli konumda yeni bir dizin oluşturur. |
|HAREKET| Bu toplu iş komutu, dosyaları veya dizinleri dizinler arasında taşır. |
|YOL| Bu toplu iş komutu, yol değişkenini görüntüler veya ayarlar. |
|DURAKLAT| Bu toplu komut, kullanıcıyı uyarır ve bir giriş satırının girilmesini bekler. |
|GÖSTER| Bu toplu komut, cmd.exe komut istemini değiştirmek veya sıfırlamak için kullanılabilir. |
|RD| Bu toplu iş komutu, dizinleri kaldırır, ancak dizinlerin kaldırılabilmesi için önce boş olmaları gerekir. |
|REN| Dosyaları ve dizinleri yeniden adlandırır |
|REM| Bu toplu iş komutu, toplu iş dosyalarındaki açıklamalar için kullanılır ve açıklamanın içeriğinin yürütülmesini engeller. |
|BAŞLAT| Bu toplu iş komutu, yeni pencerede bir program başlatır veya bir belge açar. |
|ZAMAN| Bu toplu komut, zamanı ayarlar veya görüntüler. |
|TÜR| Bu toplu iş komutu, bir dosyanın veya dosyaların içeriğini çıktıya yazdırır. |
|SES| Bu toplu iş komutu, birim etiketlerini görüntüler. |
|ÖZGÜR| Geçerli dizindeki dosyaların özniteliklerini görüntüler veya ayarlar |
|CHKDSK| Bu toplu iş komutu, diskte herhangi bir sorun olup olmadığını kontrol eder. |
|SEÇİM| Bu toplu iş komutu, kullanıcıya bir seçenekler listesi sağlar. |
|CMD| Bu toplu iş komutu, komut isteminin başka bir örneğini çağırır. |
|BİLGİ| Bu toplu iş komutu, dosya boyutuna göre 2 dosyayı karşılaştırır. |
|DÖNÜŞTÜR| Bu toplu iş komutu, bir birimi FAT16 veya FAT32 dosya sisteminden NTFS dosya sistemine dönüştürür. |
|SÜRÜCÜSORGU| Bu toplu iş komutu, kurulu tüm aygıt sürücülerini ve bunların özelliklerini gösterir. |
|GENİŞLET| Bu toplu iş komutu, dosyaları sıkıştırılmış .cab dolap dosyalarından ayıklar. |
|BUL| Bu toplu iş komutu, eşleşen satırların çıktısını alarak dosyalarda veya girişte bir dize arar. |
|BİÇİM| Bu toplu komut, bir diski FAT, FAT32 veya NTFS gibi Windows destekli dosya sistemini kullanacak şekilde biçimlendirir ve böylece diskin önceki içeriğinin üzerine yazar. |
|YARDIM| Bu toplu komut, Windows tarafından sağlanan komutların listesini gösterir. |
|IPCONFIG| Bu toplu komut, Windows IP Yapılandırmasını görüntüler. Bağlantıya göre yapılandırmayı ve bu bağlantının adını gösterir. |
|ETİKET| Bu toplu komut, bir disk etiketi ekler, ayarlar veya kaldırır. |
|DAHA FAZLA| Bu toplu komut, bir dosyanın veya dosyaların içeriğini her seferinde bir ekran olarak görüntüler. |
|NET| Kullanılan komuta bağlı olarak çeşitli ağ hizmetleri sağlar. |
|PING| Bu toplu komut, ICMP/IP "yankı" paketlerini ağ üzerinden belirlenen adrese gönderir. |
|KAPATMA| Bu toplu komut, bir bilgisayarı kapatır veya geçerli kullanıcının oturumunu kapatır. |
|SIRALAMA| Bu toplu komut, girdiyi bir kaynak dosyadan alır ve içeriğini A'dan Z'ye veya Z'den A'ya alfabetik olarak sıralar. Çıktıyı konsolda yazdırır. |
|SUBST| Bu toplu komut, yerel bir klasöre bir sürücü harfi atar, geçerli atamaları görüntüler veya bir atamayı kaldırır. |
|SİSTEM BİLGİSİ| Bu toplu komut, bir bilgisayarın ve işletim sisteminin yapılandırmasını gösterir. |
|GÖREV| Bu toplu iş komutu, bir veya daha fazla görevi sonlandırır. |
|GÖREV LİSTESİ| Bu toplu iş komutu, görev adı ve işlem kimliği (PID) dahil olmak üzere görevleri listeler. |
|KOPYALAMA| Bu toplu iş komutu, dosyaları ve dizinleri daha gelişmiş bir şekilde kopyalar. |
|AĞAÇ| Bu toplu iş komutu, geçerli dizinin tüm alt dizinlerinin bir ağacını herhangi bir özyineleme veya derinlik düzeyine kadar görüntüler. |
|FC |Bu toplu iş komutu, iki dosya arasındaki gerçek farkları listeler. |
|DISKPART |Bu toplu komut, disk bölümlerinin özelliklerini gösterir ve yapılandırır. |
|TITLE |Bu toplu iş komutu, konsol penceresinde görüntülenen başlığı ayarlar. |
|AYARLA | Geçerli sistemdeki ortam değişkenlerinin listesini görüntüler. |

## BAT dosyası örneği
Toplu komut dosyaları genellikle basit metin dosyaları olarak kaydedilir; bir sırayla yürütülen komutları içerir. Bu dosyalar .bat uzantılı olarak kaydedilir; **Command Interpreter** yazılımı kullanılarak tanınır ve yürütülür. Bu yazılım yerel olarak Microsoft Windows'ta **cmd.exe** adıyla bulunur.

İşte geçerli dizindeki tüm dosyaları silen örnek bir Toplu Komut Dosyası:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referanslar

* [Toplu Komut Dosyası - Hızlı Kılavuz](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Toplu dosya - Wikipewdia tarafından](https://en.wikipedia.org/wiki/Batch_file)

