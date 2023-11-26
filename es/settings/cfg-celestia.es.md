{
"fecha": "2023-09-27",
  "keywords": [
"cfg",
"archivo cfg",
"archivo de configuración cfg celestia",
"¿Qué es un archivo cfg?",
"cómo abrir un archivo cfg",
"archivo",
"extensión de archivo cfg",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CFG - Archivo de configuración de Celestia",
  "description":"Obtenga más información sobre el formato del archivo de configuración CFG Celestia y las API que pueden crear y abrir archivos CFG.",
"linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "configuración"
}
},
"última modificación": "2023-09-27"
}

## ¿Qué es un archivo CFG?

Un archivo de configuración de Celestia es un archivo de texto sin formato utilizado por Celestia, el programa de simulación de universos 3D. Estos archivos son vitales para personalizar cómo se comporta Celestia, qué objetos celestes se muestran y cómo aparece el programa. Sin embargo, editar estos archivos requiere especial atención porque los cambios inadecuados pueden interrumpir el proceso de carga de Celestia e impedir que se ejecute correctamente.

## Celestia

Celestia es un software de simulación astronómica 3D gratuito y de código abierto que permite a los usuarios explorar y visualizar el universo de manera muy realista e interactiva. Fue desarrollado por Chris Laurel y se lanzó por primera vez a principios de la década de 2000. Celestia está disponible para los sistemas operativos Windows, macOS y Linux.

Las características y aspectos clave de Celestia incluyen:

- **Visualización 3D realista:** Celestia proporciona una representación detallada y precisa de nuestro sistema solar, así como de estrellas, galaxias y otros objetos celestes. Utiliza texturas y modelos 3D de alta calidad para crear una experiencia visualmente inmersiva.

- **Extensa base de datos celeste:** El software viene con una amplia base de datos integrada de objetos celestes conocidos, incluidas estrellas, planetas, lunas, asteroides, cometas y naves espaciales. Los usuarios pueden localizar y explorar fácilmente estos objetos.

- **Precisión científica:** Si bien Celestia es una herramienta de visualización, su objetivo es representar objetos y fenómenos celestes con la mayor precisión posible, basándose en los datos científicos disponibles.

## Formatos de archivo utilizados por Celestia

Celestia utiliza varios formatos de archivo para diferentes aspectos de su simulación astronómica en 3D. Estos son algunos de los formatos de archivo clave empleados por Celestia:

1. **Archivos de configuración (.cel)**
- *Descripción*: Archivos de texto sin formato que permiten a los usuarios personalizar el comportamiento, la apariencia y el contenido de Celestia.
- *Propósito*: Personalizar configuraciones, definir ubicaciones y especificar objetos celestes.

2. **Modelos 3D y Mallas**
- *Formatos*: [.3ds](/es/3d/3ds/), [.obj](/es/3d/obj/), [.dae](/es/3d/dae/), .ac
- *Descripción*: Formatos de archivos de modelos 3D compatibles utilizados para representar cuerpos celestes y naves espaciales.
- *Propósito*: Mostrar objetos 3D dentro de Celestia.

3. **Archivos de textura**
- *Formatos*: [.jpg](/es/image/jpeg/), [.png](/es/image/png/), [.dds](/es/image/dds/)
- *Descripción*: Estos archivos proporcionan texturas de superficie para cuerpos celestes.
- *Propósito*: Mapear texturas en modelos 3D para una apariencia realista.

4. **Catálogos de estrellas y archivos de datos**
- *Formatos*: formatos personalizados, [.csv](/es/spreadsheet/csv/), [.tsv](/es/spreadsheet/tsv/)
- *Descripción*: Archivos de datos utilizados para representar estrellas y otros objetos celestes, lo que garantiza una simulación precisa.
- *Propósito*: Representación precisa de los objetos celestes.

5. **Mapas de cubos de textura**
- *Descripción*: Los mapas cúbicos se utilizan para simular la apariencia de objetos celestes distantes como las galaxias.
- *Propósito*: Renderizar objetos distantes con texturas realistas.

6. **Archivos de script**
- *Descripción*: Estos archivos contienen scripts personalizados escritos en el lenguaje de scripting de Celestia.
- *Propósito*: Permitir a los usuarios crear eventos dinámicos y animaciones dentro del universo de Celestia.

## Archivo de configuración de Celestia

Aquí hay una descripción básica de lo que puede hacer con el archivo de configuración de Celestia:

1. **Configuración de su ubicación**: puede especificar su ubicación en la Tierra utilizando parámetros de latitud, longitud y altitud. Esto le permite a Celestia mostrar con precisión el cielo nocturno desde su posición.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Personalizar sus opciones de visualización:** Puede ajustar varias opciones de visualización, como el campo de visión, la configuración de tiempo y las preferencias de renderizado.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Cargar objetos celestes:** Puedes agregar objetos celestes como estrellas, planetas, asteroides, naves espaciales y más a tu simulación. Cada objeto se define en el archivo de configuración con sus propiedades.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **Definición de naves espaciales:** Puedes crear tu propia nave espacial ficticia o usar naves reales especificando sus parámetros como posición, orientación y modelos 3D.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **Creación de guiones:** Puede escribir guiones en el lenguaje de secuencias de comandos personalizado de Celestia para crear animaciones y eventos dinámicos.

## ¿Cómo abrir el archivo CFG?

Programas que abren o hacen referencia a archivos CFG

- Celestia (Gratis) para (Windows, Mac, Linux)

## Otros archivos CFG

Aquí hay otros tipos de archivos que usan la extensión de archivo **.cfg**.

**Ajustes**
- [CFG - Archivo de configuración de Celestia](/es/settings/cfg-celestia/)
- [CFG - Archivo de conexión del servidor Citrix](/es/settings/cfg-citrix/)
- [CFG - Archivo de configuración MAME](/es/settings/cfg-mame/)
- [CFG - Archivo de configuración LightWave](/es/settings/cfg-lightwave/)

**Juego**
- [CFG - Archivo de lenguaje de marcado Wesnoth](/es/game/cfg-wesnoth/)
- [CFG - Archivo de configuración MUGEN](/es/game/cfg-mugen/)
- [CFG - Archivo de configuración del motor fuente](/es/game/cfg-sourceengine/)

**Sistema y miscelánea**
- [CFG - Archivo CFG](/es/system/cfg/)
- [CFG - Archivo de configuración del modelo Cal3D](/es/misc/cfg-cal3d/)

## Referencias
* [Celestia](https://en.wikipedia.org/wiki/Celestia)

