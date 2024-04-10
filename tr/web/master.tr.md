{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ANA Dosya - ASP.NET Ana Sayfa Dosya Formatı",
  "description" :"MASTER Dosya Formatı ve MASTER dosyalarını oluşturmak ve açmak için API'ler hakkında bilgi edinin.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## .MASTER dosyası nedir?

MASTER dosyası, ASP.NET ile oluşturulan bir ana web sayfası şablon dosyasıdır. MASTER dosyasıyla aynı düzene ve ayarlara sahip birden fazla sayfa oluşturmak için bir başlangıç noktası olarak kullanılır. Şablon MASTER dosyası, başlık, gezinme menüleri, alt bilgi, yazı tipi ve stil bilgilerine ilişkin ayarları içerir. MASTER dosyası kullanmak, birden fazla web sayfasını hızlı bir şekilde oluşturmanıza yardımcı olur.

Bir MASTER dosyasını Microsoft Visual Studio 2022 ve üstünü kullanarak açabilirsiniz.

## MASTER Dosya Formatı - Daha Fazla Bilgi

MASTER dosyası HTML dosya formatında oluşturulur ve kaydedilir ve diğer web sayfası dosyalarına benzer. Düzenlenebilir ve düzenlenemez bölümlere ayrılmıştır. Düzenlenebilir bölümler, kullanıcının gereksinimlerini karşılamak üzere değiştirilebilen bölümlerdir. MASTER dosyası Microsoft Visual Studio'da açıldığında düzenlenemeyen bölümler gri renkte görünür.

Ana Sayfalar, ana sayfanın kendisi ve bir veya daha fazla içerik sayfası olmak üzere iki parçadan oluşur.

### Usta sayfa

Ana sayfa .master uzantılı olup ASP.NET'te yapılmıştır. Statik metin, HTML etiketleri ve sunucu tarafı kontrollerinden oluşan önceden tanımlanmış bir düzene sahiptir. Sıradan .aspx sayfalarında @ Page yönergesi kullanılır. .master dosyaları durumunda bu, @ Master yönergesi ile değiştirilir.

### İçerik Sayfaları

İçerik sayfası, ana sayfanın yer tutucu kontrollerinin içeriğini temsil eder. Bunlar aslında ana sayfanın arkasındaki kod olan .aspx sayfalarıdır. İçerik sayfaları, aşağıda gösterildiği gibi kullanılacak ana sayfaya işaret eden bir MasterPageFile özniteliği dahil edilerek @ Page yönergesi kullanılarak bağlanır.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```
