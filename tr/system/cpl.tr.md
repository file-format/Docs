{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "uzantı", "dosya", "biçim", "sistem", "Denetim Masası Dosyası", "Windows", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Kontrol Paneli Dosyası",
  "description":"CPL dosya formatı ve CPL dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .cpl dosyası nedir? ##

Bir CPL dosyası, bir "sistem" dosyası türüdür. Windows işletim sistemi tarafından kullanılır. Bir CPL dosyası, Denetim Masası Dosyası'nın kısaltmasıdır. Bu dosyalar, bir Microsoft Windows işletim sisteminde kontrol paneliyle açılan ve diğerlerinin yanı sıra Fare, Ekranlar, Ağ İletişimi gibi kontrol panelinde bulunan araçları temsil etmek ve açmak için kullanılan ikili dosyalardır. CPL dosyaları genellikle cihazınızdaki sistem klasöründe saklanır. Bu dosyalar manuel olarak açılmamalıdır.


## CPL Dosya Biçimi ##

Windows işletim sisteminizdeki farklı CPL dosyaları, farklı kontrol paneli öğelerini temsil edecek şekilde bağlanır. Tüm kontrol paneli öğeleri bir CPL dosyasına bağlıdır ve öğelerine ".cpl" eki eklenmiştir.

Biçimleriyle birlikte bazı yaygın CPL dosyası türleri şunlardır:

* Inetcpl.cpl – Cihazınızdaki İnternet özellikleri için
* Appwiz.cpl – Cihazınıza Program özellikleri eklemek veya kaldırmak için
* Desk.cpl – Görüntü özellikleri için
* Main.cpl – Fare, Yazı Tipleri, Klavye ve Yazıcılar ile ilgili özellikler için.
* Netcpl.cpl – Ağ ile ilgili özellikler için
* System.cpl – Sistemle ilgili özellikler ve Yeni Donanım Ekleme sihirbazı için
* TimeDate.cpl – Tarih veya Saat özellikleri için
* Mlcfg32.cpl – Microsoft Exchange veya Windows Mesajlaşma özellikleri için
* Intl.cpl – Bu, Bölgesel Ayarlar özellikleriyle ilgilidir
* Modem.cpl – Modemle ilgili özellikler için
* Themes.cpl – Masaüstü Temalarını ve özelliklerini saklar.
* Password.cpl – Şifre özellikleri için
* Mmsys.cpl – Multimedya özellikleri için
* Wgpocpl.cpl – Microsoft Mail Postanesi ile ilgilidir

## Kısa Tarih ##

CPL dosya türü, Microsoft Windows tarafından geliştirilmiştir ve Windows 1.0'dan bu yana Windows işletim sisteminin ayrılmaz bir parçasıdır. Hala tüm Windows sürümlerinde kullanılmaktadır ve tüm kontrol paneli öğesi özellikleri bu dosya türü kullanılarak depolanmaktadır.

## CPL Örneği ##

Örnek bir CPL dosyası aşağıda görülebilir:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
