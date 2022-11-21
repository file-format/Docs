
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript Bayt Kodu Dosyası",
  "description":"Örnek ve ABC dosyalarını oluşturabilen ve açabilen API'lerle ABC dosya biçiminin ne olduğunu öğrenin.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Bir ABC dosyası nedir?

.abc uzantılı bir dosya, ActionScript betik dosyalarının derlenmesi sonucunda Flash derleyicisi tarafından oluşturulan bir ActionScript Bayt Kodu Dosyasıdır. ABC dosyasında bulunan bayt kodu, ActionScript Virtual Machine (AVM ve AVM2) tarafından yürütülür. Bayt kodu, sabit verilerden, AVM2 komut setinden gelen talimatlardan ve çeşitli meta verilerden oluşur. AVM veya AVM2'ye bir ABC dosyası yüklendiğinde doğrulamaya tabi tutulur. AVM2 Genel Bakışına uymuyorsa reddedilir. ABC dosyaları, uzun zaman önce durdurulan Adobe Flash Player'da açılabilir.

## ABC Dosya Biçimi - Daha Fazla Bilgi

ABC dosyaları, AVM veya AVM2 sanal makineleri tarafından okunabilen ikili dosya biçiminde diske kaydedilir. Dahili dosya yapısı, tüm sabit verileri, tip tanımlayıcıları, kodu ve meta verileriyle yürütülebilir kod bloğunu temsil eder.

## ABC Dosya Yapısı

ABC dosya yapısı aşağıda gösterildiği gibidir.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC Dosya Alanları

|Alan Adı|Açıklama|
---|---|
|minor_version, major_version|major_version ve minor_version değerleri, abcFile biçiminin ana ve ikincil sürüm numaralarıdır.|
|constant_pool|Sabit_pool, tamsayılar, çiftler, dizeler, ad alanları, ad alanı kümeleri ve çoklu adlardan oluşan değişken uzunluklu bir yapıdır.|
|method_count, method|method_count değeri, yöntem dizisindeki girişlerin sayısıdır. Yöntem dizisindeki her giriş, değişken uzunluklu bir method_info yapısıdır.|
|metadata_count, metadata|metadata_count'un değeri, meta veri dizisindeki girişlerin sayısıdır. Her meta veri girişi, bir adı bir dizi dize değeriyle eşleyen bir metadata_infostructure'dır. |
|class_count, instance, class|class_count'un değeri, örnek ve sınıf dizilerindeki girişlerin sayısıdır. |
|script_count, script|script_count'un değeri, script dizisindeki girişlerin sayısıdır. Her betik girişi, bu dosyadaki tek bir betiğin özelliklerini tanımlayan bir script_info yapısıdır. |
|method_body_count, method_body|metod_body_count'un değeri, method_body dizisindeki girişlerin sayısıdır. Her method_bodyentry, tek bir yöntem veya işlev için yönergeleri içeren değişken uzunluklu bir method_body_info yapısından oluşur.|

## Referanslar

* [Güçlü ABC (ActionScript Bayt Kodu) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

