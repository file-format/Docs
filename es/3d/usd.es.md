{
  "date" : "2021-02-01",
  "keywords" :[ "usd", "archivo usd", "formato de archivo usd", "formato de archivo", "archivo","extensión", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - Formato de descripción de escena universal",
  "description":"Obtenga más información sobre el formato de archivo USD y las API que pueden abrir y crear archivos USD",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## ¿Qué es un archivo USD?

Un archivo con extensión .usd es un formato de archivo de descripción de escena universal que codifica datos con el fin de intercambiar y aumentar datos entre aplicaciones de creación de contenido digital. Desarrollado por Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) brinda la capacidad de intercambiar activos elementales (como modelos) o animación.

## Formato de archivo USD

Los archivos USD pueden tener formato binario (también conocido como archivos Crate) o archivos respaldados por ASCII. Ambos formatos de archivo son intercambiables donde las referencias se pueden vincular a activos .usd sin cambiar las fuentes. El formato de archivo USD consta de un conjunto de bibliotecas de C++ con enlaces de Python para secuencias de comandos. Permite el ensamblaje y la organización de cualquier cantidad de elementos de escena 3D, como decorados virtuales, escenas y tomas, para transmitirlos de una aplicación a otra.

### Tipos de datos USD

Los tipos de datos fundamentales admitidos por el formato de archivo USD se enumeran en la siguiente tabla.

|Token de tipo de valor |Tipo C++ |Descripción|
---|---|---|
|bool|bool||
|uchar|uint8_t|entero sin signo de 8 bits|
|int|int32_t|entero con signo de 32 bits|
|uint|uint32_t|entero sin signo de 32 bits|
|int64|int64_t|entero con signo de 64 bits|
|uint64|uint64_t|entero sin signo de 64 bits|
|mitad|GfHalf|coma flotante de 16 bits|
|flotante|flotante|coma flotante de 32 bits|
|doble|doble|coma flotante de 64 bits|
|código de tiempo|SdfTimeCode|doble que representa un tiempo resoluble|
|cadena|std::cadena|cadena stl|
|token|TfToken|cadena interna con comparación rápida y hashing|
|asset|SdfAssetPath|representa una ruta resoluble a otro activo|
|matriz2d|GfMatriz2d|matriz 2x2 de dobles|
|matrix3d|GfMatrix3d|matriz 3x3 de dobles|
|matrix4d|GfMatrix4d|matriz 4x4 de dobles|
|quatd|GfQuatd|cuaternión de doble precisión|
|quatf|GfQuatf|cuaternión de precisión simple|
|quath|GfQuath|cuaternión de precisión media|
|doble2|GfVec2d|vector de 2 dobles|
|float2|GfVec2f|vector de 2 floats|
|mitad2|GfVec2h|vector de 2 mitades|
|int2|GfVec2i|vector de 2 enteros|
|doble3|GfVec3d|vector de 3 dobles|
|float3|GfVec3f|vector de 3 floats|
|half3|GfVec3h|vector de 3 mitades|
|int3|GfVec3i|vector de 3 enteros|
|doble4|GfVec4d|vector de 4 dobles|
|float4|GfVec4f|vector de 4 flotadores|
|half4|GfVec4h|vector de 4 mitades|
|int4|GfVec4i|vector de 4 enteros|

## Ejemplo de USD

Un ejemplo de un archivo USD en formato de archivo ASCII simple es el siguiente.

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
## Referencias ##

* [Introducción a USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [Referencia de la API de USD](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

