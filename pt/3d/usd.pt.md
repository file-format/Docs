{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "arquivo usd", "formato de arquivo usd", "formato de arquivo", "arquivo", "extensão", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Formato de descrição de cena universal",
  "description":"Saiba mais sobre o formato de arquivo USD e as APIs que podem abrir e criar arquivos USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## O que é um arquivo USD?

Um arquivo com extensão .usd é um formato de arquivo de descrição de cena universal que codifica dados para fins de intercâmbio e aumento de dados entre aplicativos de criação de conteúdo digital. Desenvolvido pela Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) oferece a capacidade de trocar ativos elementares (como modelos) ou animação.

## Formato de arquivo USD

Os arquivos USD podem ter formato binário (também conhecido como arquivos Crate) ou arquivos com suporte ASCII. Ambos os formatos de arquivo são intercambiáveis, onde as referências podem ser vinculadas a ativos .usd sem alterar as fontes. O formato de arquivo USD consiste em um conjunto de bibliotecas C++ com ligações Python para script. Ele permite a montagem e organização de qualquer número de elementos de cena 3D, como cenários virtuais, cenas e tomadas para transmiti-los de aplicativo para aplicativo.

### Tipos de dados em USD

Os tipos de dados fundamentais suportados pelo formato de arquivo USD estão listados na tabela a seguir.

|Token de tipo de valor |Tipo C++ |Descrição|
---|---|---|
|bool|bool||
|uchar|uint8_t|inteiro sem sinal de 8 bits|
|int|int32_t|inteiro com sinal de 32 bits|
|uint|uint32_t|inteiro sem sinal de 32 bits|
|int64|int64_t|inteiro com sinal de 64 bits|
|uint64|uint64_t|inteiro sem sinal de 64 bits|
|half|GfHalf|ponto flutuante de 16 bits|
|float|float|ponto flutuante de 32 bits|
|double|double|ponto flutuante de 64 bits|
|timecode|SdfTimeCode|double representando um tempo resolvível|
|string|std::string|stl string|
|token|TfToken|string interna com comparação rápida e hash|
|asset|SdfAssetPath|representa um caminho resolvível para outro ativo|
|matriz2d|MatrizGf2d|matriz de duplos 2x2|
|matriz3d|MatrizGf3d|matriz de duplos 3x3|
|matriz4d|MatrizGf4d|matriz de duplos 4x4|
|quatd|GfQuatd|quatérnio de precisão dupla|
|quatf|GfQuatf|quatérnio de precisão simples|
|quath|GfQuath|quatérnio de meia precisão|
|double2|GfVec2d|vetor de 2 doubles|
|float2|GfVec2f|vetor de 2 floats|
|metade2|GfVec2h|vetor de 2 metades|
|int2|GfVec2i|vetor de 2 ints|
|double3|GfVec3d|vetor de 3 duplos|
|float3|GfVec3f|vetor de 3 floats|
|metade3|GfVec3h|vetor de 3 metades|
|int3|GfVec3i|vetor de 3 ints|
|double4|GfVec4d|vetor de 4 duplos|
|float4|GfVec4f|vetor de 4 floats|
|metade4|GfVec4h|vetor de 4 metades|
|int4|GfVec4i|vetor de 4 ints|

## Exemplo USD

Um exemplo de um arquivo USD no formato de arquivo ASCII simples é o seguinte.

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
## Referências ##

* [Introdução ao USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Referência da API do USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

