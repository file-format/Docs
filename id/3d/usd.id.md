{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "file usd", "format file usd", "format file", "file", "ekstensi", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Format Deskripsi Adegan Universal",
  "description":"Pelajari tentang format file USD dan API yang dapat membuka dan membuat file USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Apa itu file USD?

File dengan ekstensi .usd adalah format file Deskripsi Pemandangan Universal yang menyandikan data untuk tujuan pertukaran dan penambahan data di antara aplikasi pembuatan konten digital. Dikembangkan oleh Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) memberikan kemampuan untuk menukar aset elemen (seperti model) atau animasi.

## Format File USD

File USD dapat memiliki format biner (juga dikenal sebagai file Peti) atau file yang didukung ASCII. Kedua format file ini dapat dipertukarkan di mana referensi dapat ditautkan ke aset .usd tanpa mengubah sumbernya. Format file USD terdiri dari sekumpulan pustaka C++ dengan pengikatan Python untuk pembuatan skrip. Ini memungkinkan perakitan dan pengorganisasian sejumlah elemen adegan 3D seperti set virtual, adegan, dan bidikan untuk mengirimkannya dari aplikasi ke aplikasi.

### Jenis Data USD

Jenis data fundamental yang didukung oleh format file USD tercantum dalam tabel berikut.

|Token tipe nilai |Tipe C++ |Deskripsi|
---|---|---|
|bool|bool||
|uchar|uint8_t|8 bit unsigned integer|
|int|int32_t|bilangan bulat bertanda 32 bit|
|uint|uint32_t|32 bit unsigned integer|
|int64|int64_t|64 bit bilangan bulat bertanda|
|uint64|uint64_t|64 bit unsigned integer|
|setengah|GfHalf|titik apung 16 bit|
|float|float|32 bit floating point|
|ganda|ganda|titik apung 64 bit|
|timecode|SdfTimeCode|double mewakili waktu yang dapat diselesaikan|
|string|std::string|stl string|
|token|TfToken|menginternir string dengan perbandingan cepat dan hashing|
|aset|SdfAssetPath|mewakili jalur yang dapat diselesaikan ke aset lain|
|matrix2d|GfMatrix2d|matriks ganda 2x2|
|matrix3d|GfMatrix3d|matriks ganda 3x3|
|matrix4d|GfMatrix4d|matriks ganda 4x4|
|quatd|GfQuatd|angka empat presisi ganda|
|quatf|GfQuatf|angka empat presisi tunggal|
|quath|GfQuath|angka empat setengah presisi|
|ganda2|GfVec2d|vektor dari 2 ganda|
|float2|GfVec2f|vektor dari 2 float|
|half2|GfVec2h|vektor dari 2 setengah|
|int2|GfVec2i|vektor dari 2 int|
|ganda3|GfVec3d|vektor dari 3 ganda|
|float3|GfVec3f|vektor dari 3 float|
|half3|GfVec3h|vektor dari 3 setengah|
|int3|GfVec3i|vektor dari 3 int|
|ganda4|GfVec4d|vektor dari 4 ganda|
|float4|GfVec4f|vektor dari 4 float|
|half4|GfVec4h|vektor dari 4 setengah|
|int4|GfVec4i|vektor dari 4 int|

## USD Contoh

Contoh file USD dalam format file ASCII biasa adalah sebagai berikut.

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
## Referensi ##

* [Pengantar USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Referensi API USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

