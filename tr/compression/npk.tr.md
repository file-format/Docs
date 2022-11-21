{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK Dosya Biçimi",
  "description":"NPK dosya formatı ve NPK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## NPK dosyası nedir?

NPK dosyası, yönlendirici işletim sisteminin yükseltilmesi için **MikroTik** yönlendiriciler tarafından kullanılan bir yazılım yükseltme paketi dosyasıdır. Yazılım güncellemelerini yüklemek için yönlendiriciye yüklenen sıkıştırılmış bir ikili arşiv olarak gelir. Bir NPK dosyalarının içerdiği bilgiler, IP adresi ve IP hizmeti gibi ağ bilgilerini, bağlayıcı bilgilerini (ethernet arabirimleri ve seri bağlantı noktası), e-posta kurulumunu, köprü yapılandırmasını ve yerel kullanıcı yönetimini içerir.

## NPK Dosya Biçimi

NPK dosyaları sıkıştırılmış ikili arşiv olarak saklanır. Sadece MikroTik'in kullandığı kapalı bir dosya formatıdır. 3. şahıslar aracılığıyla RouterOS eklentileri oluşturmak amaçlanmamıştır. NPK dosyaları MikroTik'in kendisi tarafından korunur ve bunların yükseltilmiş sürümleri [MikroTik](https://mikrotik.com/download) web sitesinin indirme bölümlerinden indirilebilir.

Bir yönlendiriciye bir NPK dosyası yüklendiğinde, yeniden başlatılmadığı sürece yönlendirici işletim sistemi etkili olmaz. Bu nedenle, yönlendirici işletim sisteminin yükseltilmesi için yeniden başlatma gerekir.

## Referanslar

* [MikroTik - Yönlendirici İşletim Sistemini Yükseltme](https://mikrotik.com/download)
* [NPK Dosyaları Nasıl Oluşturulur](https://forum.mikrotik.com/viewtopic.php?t=87126)

