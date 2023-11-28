{
"tarih": "2023-05-31",
  "keywords": [
"masaüstü dosyası",
"masaüstü dosyası nedir",
"masaüstü dosyası neler içeriyor",
"örnek masaüstü dosyası",
"masaüstü dosyası nasıl açılır",
"masaüstü dosyasının formatı nedir",
"dosya",
"masaüstü dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MASAÜSTÜ Dosya Formatı - Masaüstü Giriş Dosyası",
  "description":"MASAÜSTÜ dosyaları oluşturup açabilen MASAÜSTÜ formatı ve API'ler hakkında bilgi edinin.",
"linktitle": "MASAÜSTÜ",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
      "parent": "settings"
}
},
"sonmod": "2023-05-31"
}

## MASAÜSTÜ dosyası nedir?

.desktop dosyası, uygulama kısayollarını ve başlatıcılarını tanımlamak için Linux masaüstü ortamları tarafından kullanılan bir yapılandırma dosyasıdır. Bir uygulamanın adı, simgesi, çalıştırılacak komutu ve diğer özellikleri gibi meta veriler sağlar. Bu dosyalar genellikle Linux tabanlı sistemlerde uygulama menülerinde, masaüstü başlatıcılarda veya panellerde kısayollar oluşturmak için kullanılır.

## MASAÜSTÜ dosyası ne içeriyor?

Bir .desktop dosyası belirli bir formata uyar ve birkaç anahtar alan içerir:

- **[Masaüstü Girişi]:** Bu, .desktop dosyasının ana bölüm başlığıdır.
- **Ad:** Uygulamanın adını belirtir.
- **Yorum:** Uygulama hakkında kısa bir açıklama veya yorum sağlar.
- **Exec:** Uygulama başlatılırken yürütülecek komutu tanımlar.
- **Simge:** Uygulamayla ilişkili simge dosyasının yolunu belirtir.
- **Terminal:** Uygulamanın bir terminal penceresinde çalıştırılıp çalıştırılmayacağını belirtir.
- **Tür:** "Uygulama" veya "Bağlantı" gibi giriş türünü belirtir.
- **Kategoriler:** Uygulamanın menüde görüntülenmesi gereken kategorileri veya grupları belirtir.
- **StartupNotify:** Masaüstü ortamının uygulama için bir başlangıç bildirimi gösterip göstermeyeceğini belirtir.
- **NoDisplay:** Uygulamanın menülerden gizlenip gizlenmeyeceğini belirtir.
- **Eylemler:** Belirli bir dosyayı açmak gibi uygulamada gerçekleştirilebilecek ek eylemleri tanımlar.

## Örnek MASAÜSTÜ dosyası

Burada "MyTextEditor" adlı hayali bir metin düzenleyiciye ait bir .desktop dosyası örneği verilmiştir:

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Bu örnekte, .desktop dosyası "MyTextEditor" uygulamasını ilişkili özellikleriyle birlikte tanımlar. Ayrıca, uygulama başlatıcısının içerik menüsünden erişilebilen "Yeni Pencereyi Aç" ve "Mevcut Dosyayı Aç" olmak üzere iki ek eylem içerir.

Bir .desktop dosyasını '/usr/share/applications' veya '~/.local/share/applications' gibi belirli dizinlere yerleştirdiğinizde, masaüstü ortamı onu tanıyacak ve uygulamayı menülerde buna göre görüntüleyecek veya şuradan başlatılmasına izin verecektir. masaüstü.

## MASAÜSTÜ dosyası nasıl açılır?

Çeşitli yazılım programları .desktop dosyalarını açabilir ve işleyebilir. Bu programlar genellikle Linux tabanlı sistemlerdeki dosya yöneticileri veya masaüstü ortamlarıdır. İşte bazı örnekler:

- **Nautilus (Dosyalar):** GNOME masaüstü ortamı için varsayılan dosya yöneticisi.
- **Nemo:** Cinnamon masaüstü ortamının dosya yöneticisi.
- **Dolphin:** KDE Plazma masaüstü ortamı için varsayılan dosya yöneticisi.
- **Thunar:** Xfce masaüstü ortamı için varsayılan dosya yöneticisi.
- **KDE Menü Düzenleyicisi:** .desktop dosyalarını görüntülemenizi ve düzenlemenizi sağlayan, KDE Plazma masaüstü ortamına özel bir araç.

Bu dosya yöneticileri ve masaüstü ortamları, .desktop dosyalarını yönetmek için grafiksel arayüz sağlar. .desktop dosyalarının özelliklerini görüntülemenize ve düzenlemenize, uygulama başlatıcıları oluşturmanıza ve uygulama menülerindeki veya masaüstündeki kısayolları düzenlemenize olanak tanır.

.desktop dosyaları düz metin dosyalarıdır, dolayısıyla bunları seçtiğiniz bir metin düzenleyiciyle de açabilir ve düzenleyebilirsiniz. Yüklü programlar listesinden bir metin düzenleyici seçmek için .desktop dosyasına sağ tıklayın ve "Birlikte aç" veya "Başka bir uygulamayla aç"ı seçin.

## MASAÜSTÜ dosyasının formatı nedir?

.desktop dosya formatı belirli bir yapı ve formatı takip eder. Bölümler halinde düzenlenmiş bir dizi anahtar/değer çiftinden oluşan düz bir metin dosyasıdır. İşte formata genel bir bakış:

- **Bölüm Başlıkları:** Her bölüm köşeli parantez ([]) içine alınmış bir başlıkla başlar. Birincil bölüm genellikle uygulama veya başlatıcının ana meta verilerini içeren [Masaüstü Girişi] olarak adlandırılır.
- **Anahtar-Değer Çiftleri:** Her bölümde, anahtar/değer çiftlerini kullanarak özellikleri tanımlarsınız. Biçim "Anahtar=Değer"dir. Anahtar, özelliği tanımlar ve değer, ilgili verileri sağlar.
- **Özellik Söz Dizimi:** Özellik değerleri; dizeler, boole değerleri, dosya yolları veya listeler dahil olmak üzere farklı türlerde olabilir. Her özellik değerinin formatı türüne bağlıdır.
- **Yorumlar:** '#' sembolünü kullanarak .desktop dosyasına yorum ekleyebilirsiniz. Satırda '#' işaretinden sonra gelen her şey yorum olarak kabul edilir ve dikkate alınmaz.

## Referanslar
* [Masaüstü Giriş Dosyaları](https://www.baeldung.com/linux/desktop-entry-files)

