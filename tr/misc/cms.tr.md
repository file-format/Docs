{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CMS Dosya Biçimi - Bağlantı Yöneticisi Hizmet Profili Dosyası",
  "description":"CMS dosyası ve CMS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## CMS dosyası nedir?

CMS dosyası, Microsoft Windows Connection Manager tarafından kullanılan profil bilgilerini içeren bir veri dosyasıdır. Uzak kullanıcıların bu profil bilgilerini kullanarak bir ağa bağlanmasına izin verir. Bir CMS dosyasında saklanan bilgiler, kullanıcının işletim sistemi ve uzak kullanıcı ile ağ arasında bağlantı kurmak için kullanılan izinler hakkındaki verileri içerir. CMS yöneticileri, CMS dosyaları oluşturmak için Bağlantı Yöneticisi Yönetici Seti'ni (CMAK) kullanır.

## CMS Dosya Biçimi - Daha Fazla Bilgi

CMS dosyaları, kullanıcı makinelerinde yaygın olarak bulunmaz. Bunlar, özellikle uzaktaki kullanıcıların bir ağa bağlanmasına izin vermek için kullanıldığından, bunları bir şirket ağına veya belirli bir amaca yönelik ofise bağlanmak için kullanılan bilgisayarlarda bulacaksınız. Çoğu durumda, yalnızca bir şirkete ayrılmış Sanal Özel Ağ (VPN) gibi bir kurumsal ağa bağlanmak için kullanılır. Bir ağ yöneticisi olarak, uzak bir konumdan şirket ağına erişmesine izin vermek için Bağlantı Yöneticisi ile böyle bir ağa erişim kuracaksınız.

### Insdie CMS nedir?

Bağlantı Yöneticisi kullanılarak bir CMS profil dosyası oluşturulur ve uzak kullanıcıya sağlanmadan önce diğer yapılandırma dosyalarıyla birlikte paketlenir. Bu ek dosyalar, bir [EXE](/tr/executable/exe/) dosyasında birlikte paketlenmiş bir CMP ve bir INF dosyası içerebilir. Bu eksiksiz paket, uzak kullanıcıya ağa bağlanması için sağlanır.

## Referanslar

* [Windows Bağlantı Yöneticisini anlama ve yapılandırma](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

