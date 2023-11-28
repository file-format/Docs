{
"tarih": "2023-03-07",
  "keywords": [
"reg dosyası",
"reg dosyası nedir",
"dosya",
"reg dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "REG Dosya Formatı - Windows Kayıt Defteri Dosyası",
  "description":"REG dosyalarını oluşturabilen ve açabilen REG formatı ve API'ler hakkında bilgi edinin.",
"bağlantı başlığı": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
      "parent": "system"
}
},
"sonmod": "2023-03-07"
}

## .REG dosyası nedir?

REG dosyası, Windows Kayıt Defteri verilerini içe veya dışa aktarmak için kullanılan bir dosya biçimidir. Windows Kayıt Defteri, Windows işletim sistemi ve yüklü uygulamalar için yapılandırma ayarlarını ve seçeneklerini saklayan hiyerarşik bir veritabanıdır. Kayıt defteri, kullanıcı tercihleri, uygulama ayarları, donanım ve yazılım yapılandırma verileri ve daha fazlası gibi bilgileri içerir.

REG dosyası genellikle ".reg" dosya uzantısına sahiptir ve belirli bir formatta bir dizi kayıt defteri girişi ve değeri içeren düz metin dosyasıdır. Biçim, dosyayı bir kayıt defteri dosyası olarak tanımlayan bir başlık bölümünden ve ardından kayıt defteri girişlerini temsil eden bir dizi anahtar ve değer çiftinden oluşur.

## REG Dosya Formatı - Daha Fazla Bilgi

Reg dosya biçiminin bir örneği:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Dosyanın ilk satırı kayıt defteri düzenleyicisinin sürümünü belirtir. Aşağıdaki satırlar, bir anahtar yolu biçiminde ve ardından bir değer adı ve değer verisi biçimindeki kayıt defteri girişlerini içerir. Bu örnekte, reg dosyası iki giriş içerir: biri Windows başlangıç listesine "Example.exe" adlı bir programı ekleyen, diğeri ise Windows Gezgini gelişmiş ayarlarındaki "Gizli" değerini "true" olarak ayarlayan.

Reg dosyaları, Not Defteri gibi bir metin düzenleyici kullanılarak oluşturulabilir ve düzenlenebilir. Genellikle yedekleme ve geri yükleme amaçlarının yanı sıra birden fazla bilgisayarı aynı kayıt defteri ayarlarıyla yapılandırmak için kullanılırlar.

## Windows Kayıt Defterini İçe Aktarma veya Dışa Aktarma

REG dosyası, Windows Kayıt Defterinden veri almak veya vermek için kullanılan bir dosya türüdür. Windows Kayıt Defteri, Windows işletim sistemi ve yüklü uygulamalar için yapılandırma ayarlarını ve seçeneklerini saklayan hiyerarşik bir veritabanıdır. Kayıt defteri, kullanıcı tercihleri, uygulama ayarları, donanım ve yazılım yapılandırma verileri ve daha fazlası gibi bilgileri içerir.

Reg dosyaları, kayıt defteri girişlerini oluşturmak veya değiştirmek için kullanılabilir ve bunlar genellikle yedekleme ve geri yükleme amacıyla ve aynı kayıt defteri ayarlarıyla birden fazla bilgisayarı yapılandırmak için kullanılır. Windows Kayıt Defterine yeni bir kayıt defteri girişi eklemek için reg dosyasını nasıl kullanacağınız aşağıda açıklanmıştır:

1. Notepad gibi bir metin düzenleyiciyi kullanarak yeni bir metin dosyası oluşturun.
2. Kayıt defteri girdisini doğru biçimde yazın. Biçim, dosyayı bir kayıt defteri dosyası olarak tanımlayan bir başlık bölümünden ve ardından kayıt defteri girişlerini temsil eden bir dizi anahtar ve değer çiftinden oluşur. İşte bir örnek:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Bu, geçerli kullanıcının kayıt defteri kovanındaki "Yazılım" anahtarının altında "Örnek" adında yeni bir anahtar oluşturur ve "Ayar1" değerini "Değer1" olarak ayarlar.

3. Dosyayı .reg dosya uzantısıyla kaydedin.
4. Yeni kayıt defteri girişini Windows Kayıt Defterine eklemek için .reg dosyasına çift tıklayın.

Girişi kayıt defterine eklemek istediğinizi onaylamanız istenecektir. Onayladıktan sonra yeni giriş kayıt defterine eklenecektir ve Kayıt Defteri Düzenleyicisi aracını kullanarak doğrulayabilirsiniz.

## Referanslar
* [Windows Kayıt Defteri](https://en.wikipedia.org/wiki/Windows_Registry)

