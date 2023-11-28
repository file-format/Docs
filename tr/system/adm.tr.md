{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM Dosyası - Yönetim Şablonu Dosya Formatı",
  "description":"ADM dosya formatı ve ADM dosyalarının nasıl açılacağı hakkında bilgi edinin.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## .ADM seçenek numarası

ADM dosyası, Microsoft Grup İlkeleri yazılımı tarafından kayıt defteri dosyasındaki kayıt defteri tabanlı ilke ayarlarının konumunu belirtmek için kullanılan bir şablon dosyasıdır. Sistem yöneticileri tarafından, grubun parçası olan bir grup bilgisayarı yönetme ilkesini tanımlamak için kullanılır. Bu bilgiler, grubun yönetimi için oluşturulan Grup İlkesi Nesnelerinin (GPO'lar) parçası haline gelir.

ADM dosyalarını Microsoft Grup İlkesi Nesne Düzenleyicisi'ni kullanarak açabilirsiniz.

## ADM Dosya Formatı - Daha Fazla Bilgi

ADM dosyaları, unicode formatlı metin dosyaları olarak saklanır. Bunlar öncelikle Windows Vista ve Windows 7 kayıt defterindeki kayıt defteri tabanlı ilke ayarlarının konumunu açıklamak için kullanıldı.

ADM dosyaları artık desteklenmiyor ve bunların yerini [ADMX](/tr/system/admx/) dosyaları aldı. GPA, Microsoft Windows Vista Service Pack 1 veya sonraki sürümünü çalıştıran bilgisayarlarda aşağıdaki varsayılan ADM dosyalarını yok sayar.

* sistem.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Referanslar

* [Yönetim Şablonu Dosyaları - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Yönetim Şablonu Dosyalarını Yönetme](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

