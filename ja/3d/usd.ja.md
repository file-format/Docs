{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd ファイル", "usd ファイル形式", "ファイル形式", "ファイル","拡張子", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - ユニバーサルシーン記述フォーマット",
  "description":"USD ファイルの形式と,USD ファイルを開いて作成できる API について学びます。",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## .USD ファイルとは何ですか?

拡張子が .usd のファイルは、デジタル コンテンツ作成アプリケーション間でデータを交換および拡張する目的でデータをエンコードするユニバーサル シーン記述ファイル形式です。 Pixar によって開発された [USD](https://openusd.org/release/intro.html) は、要素アセット (モデルなど) またはアニメーションを交換する機能を提供します。

## USDファイル形式

USD ファイルには、バイナリ形式 (クレート ファイルとも呼ばれます) または ASCII 形式のファイルを使用できます。これらのファイル形式は両方とも交換可能で、ソースを変更せずに参照を .usd アセットにリンクできます。 USD ファイル形式は、スクリプト作成用の Python バインディングを備えた一連の C++ ライブラリで構成されています。仮想セット、シーン、ショットなどの任意の数の 3D シーン要素を組み立てて編成し、それらをアプリケーションからアプリケーションに送信できます。

### 米ドルのデータ型

USD ファイル形式でサポートされている基本的なデータ型を次の表に示します。

|値型トークン |C++ 型 |説明|
---|---|---|
|ブール|ブール||
|uchar|uint8_t|8 ビット符号なし整数|
|int|int32_t|32 ビット符号付き整数|
|uint|uint32_t|32 ビット符号なし整数|
|int64|int64_t|64 ビット符号付き整数|
|uint64|uint64_t|64 ビット符号なし整数|
|half|GfHalf|16 ビット浮動小数点|
|float|float|32 ビット浮動小数点|
|double|double|64 ビット浮動小数点|
|タイムコード|SdfTimeCode|解決可能な時間を表す double|
|文字列|std::文字列|stl文字列|
|token|TfToken|インターンされた文字列を高速比較とハッシュ化|
|asset|SdfAssetPath|別のアセットへの解決可能なパスを表します|
|matrix2d|GfMatrix2d|倍精度の 2x2 行列|
|matrix3d|GfMatrix3d|倍精度の 3x3 行列|
|matrix4d|GfMatrix4d|倍精度の 4x4 行列|
|quatd|GfQuatd|倍精度クォータニオン|
|quatf|GfQuatf|単精度クォータニオン|
|quath|GfQuath|半精度クォータニオン|
|double2|GfVec2d|2 つの double のベクトル|
|float2|GfVec2f|2 float のベクトル|
|half2|GfVec2h|2 つの半分のベクトル|
|int2|GfVec2i|2 つの整数のベクトル|
|double3|GfVec3d|3 つの double のベクトル|
|float3|GfVec3f|3 つの float のベクトル|
|half3|GfVec3h|3 つの半分のベクトル|
|int3|GfVec3i|3 つの整数のベクトル|
|double4|GfVec4d|4 つの double のベクトル|
|float4|GfVec4f|4 つのフロートのベクトル|
|half4|GfVec4h|4 つの半分のベクトル|
|int4|GfVec4i|4 つの整数のベクトル|

## 米ドルの例

プレーン ASCII ファイル形式の USD ファイルの例は次のとおりです。

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
## 参照 ##

* [米ドルの紹介](https://openusd.org/release/intro.html)
* [USD API リファレンス](https://openusd.org/release/apiDocs.html)

