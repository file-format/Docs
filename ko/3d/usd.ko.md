{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "usd 파일", "usd 파일 형식", "파일 형식", "파일","확장자", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - 범용 장면 설명 형식",
  "description":"USD 파일 형식과 USD 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## .USD 파일이란?

확장자가 .usd인 파일은 디지털 콘텐츠 생성 응용 프로그램 간에 데이터를 교환하고 보강할 목적으로 데이터를 인코딩하는 범용 장면 설명 파일 형식입니다. Pixar에서 개발한 [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)는 기본 자산(예: 모델) 또는 애니메이션을 교환하는 기능을 제공합니다.

## USD 파일 형식

USD 파일은 바이너리 형식(Crate 파일이라고도 함) 또는 ASCII 지원 파일일 수 있습니다. 이 두 파일 형식은 소스를 변경하지 않고 참조를 .usd 자산에 연결할 수 있는 곳에서 서로 바꿔 사용할 수 있습니다. USD 파일 형식은 스크립팅을 위한 Python 바인딩이 포함된 C++ 라이브러리 세트로 구성됩니다. 가상 세트, 장면 및 샷과 같은 3D 장면 요소의 수에 관계없이 조립 및 구성하여 응용 프로그램에서 응용 프로그램으로 전송할 수 있습니다.

### USD 데이터 유형

USD 파일 형식에서 지원하는 기본 데이터 유형은 다음 표에 나열되어 있습니다.

|값 유형 토큰 |C++ 유형 |설명|
---|---|---|
|불|불|불||
|uchar|uint8_t|8비트 부호 없는 정수|
|int|int32_t|32비트 부호 있는 정수|
|uint|uint32_t|32비트 부호 없는 정수|
|int64|int64_t|64비트 부호 있는 정수|
|uint64|uint64_t|64비트 부호 없는 정수|
|half|GfHalf|16비트 부동 소수점|
|float|float|32비트 부동 소수점|
|이중|이중|64비트 부동 소수점|
|timecode|SdfTimeCode|결정 가능한 시간을 나타내는 double|
|문자열|표준::문자열|표준 문자열|
|token|TfToken|빠른 비교 및 해싱이 포함된 인턴 문자열|
|asset|SdfAssetPath|다른 자산에 대한 해석 가능한 경로를 나타냄|
|matrix2d|GfMatrix2d|2x2 2배 행렬|
|matrix3d|GfMatrix3d|2배의 3x3 행렬|
|matrix4d|GfMatrix4d|2배의 4x4 행렬|
|quatd|GfQuatd|배정밀도 쿼터니언|
|quatf|GfQuatf|단정밀도 쿼터니언|
|quath|GfQuath|절반 정밀도 쿼터니언|
|double2|GfVec2d|2배의 벡터|
|float2|GfVec2f|2개의 부동 소수점 벡터|
|half2|GfVec2h|2개의 절반의 벡터|
|int2|GfVec2i|2 정수의 벡터|
|double3|GfVec3d|배수 3개의 벡터|
|float3|GfVec3f|3개의 부동 소수점 벡터|
|half3|GfVec3h|하프 3의 벡터|
|int3|GfVec3i|3개의 정수로 구성된 벡터|
|double4|GfVec4d|4배의 벡터|
|float4|GfVec4f|4개의 부동 소수점 벡터|
|half4|GfVec4h|하프 4개의 벡터|
|int4|GfVec4i|4 정수의 벡터|

## USD 예

일반 ASCII 파일 형식의 USD 파일의 예는 다음과 같습니다.

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
## 참조 ##

* [USD 소개](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [USD API 레퍼런스](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

