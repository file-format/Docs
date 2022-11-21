{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd dosyası", "usd dosya biçimi", "dosya biçimi", "dosya","uzantı", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Evrensel Sahne Açıklama Formatı",
  "description":"USD dosya formatı ve USD dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## USD dosyası nedir?

.usd uzantılı bir dosya, dijital içerik oluşturma uygulamaları arasında veri alışverişi ve artırma amacıyla verileri kodlayan bir Evrensel Sahne Tanımı dosya biçimidir. Pixar tarafından geliştirilen [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html), temel varlıkları (modeller gibi) veya animasyonu değiştirme yeteneği sağlar.

## USD Dosya Biçimi

USD dosyaları, ikili biçime (Crate dosyaları olarak da bilinir) veya ASCII destekli dosyalara sahip olabilir. Referansların kaynakları değiştirmeden .usd varlıklarına bağlanabildiği bu dosya biçimlerinin her ikisi de birbirinin yerine kullanılabilir. USD dosya formatı, komut dosyası oluşturmak için Python bağlamaları içeren bir dizi C++ kitaplığından oluşur. Uygulamadan uygulamaya iletmek için sanal setler, sahneler ve çekimler gibi herhangi bir sayıda 3B sahne öğesinin birleştirilmesini ve düzenlenmesini sağlar.

### USD Veri Türleri

USD dosya biçimi tarafından desteklenen temel veri türleri aşağıdaki tabloda listelenmiştir.

|Değer türü belirteci |C++ türü |Açıklama|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bit işaretsiz tamsayı|
|int|int32_t|32 bit işaretli tamsayı|
|uint|uint32_t|32 bit işaretsiz tamsayı|
|int64|int64_t|64 bit işaretli tamsayı|
|uint64|uint64_t|64 bit işaretsiz tamsayı|
|yarım|GfHalf|16 bit kayan nokta|
|kayan|kayan|32 bit kayan nokta|
|double|double|64 bit kayan nokta|
|timecode|SdfTimeCode|çift çözülebilir bir zamanı temsil ediyor|
|string|std::string|stl string|
|token|TfToken|hızlı karşılaştırma ve hashleme ile dahili dize|
|asset|SdfAssetPath|başka bir varlığa giden çözülebilir bir yolu temsil eder|
|matrix2d|GfMatrix2d|2x2 ikili matris|
|matrix3d|GfMatrix3d|3x3 ikili matris|
|matrix4d|GfMatrix4d|4x4 ikili matris|
|quatd|GfQuatd|çift kesinlikli dördey|
|quatf|GfQuatf|tek duyarlıklı dördey|
|quath|GfQuath|yarı kesinlikli dördey|
|double2|GfVec2d|2 çiftin vektörü|
|float2|GfVec2f|2 yüzer vektörü|
|half2|GfVec2h|2 yarımın vektörü|
|int2|GfVec2i|2 int vektörü|
|double3|GfVec3d|3 çiftin vektörü|
|float3|GfVec3f|3 yüzer vektörü|
|half3|GfVec3h|3 yarımın vektörü|
|int3|GfVec3i|3 int vektörü|
|double4|GfVec4d|4 çiftin vektörü|
|float4|GfVec4f|4 yüzer vektörü|
|half4|GfVec4h|4 yarımın vektörü|
|int4|GfVec4i|4 int vektörü|

## USD Örneği

Düz ASCII dosya biçiminde bir USD dosyası örneği aşağıdaki gibidir.

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## Referanslar ##

* [USD'ye Giriş](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [USD API Referansı](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

