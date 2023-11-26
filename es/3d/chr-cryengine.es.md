{
"fecha": "2023-10-11",
   "keywords":[
"chr",
"archivo chr",
"archivo de caracteres chr cryengine",
"cómo abrir un archivo chr",
"archivo",
"extensión de archivo chr",
"extensión",
"archivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CHR: archivo de caracteres CryENGINE",
   "description":"Obtenga más información sobre el formato de archivo de caracteres CHR CryENGINE y las API que pueden crear y abrir archivos CHR.",
"linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
"parent": "3d"
}
},
"último mod": "2023-10-11"
}

## ¿Qué es un archivo CHR?

El archivo CHR en el contexto de CryENGINE se refiere a un **Archivo de caracteres CryENGINE**. CryENGINE es un motor de juego desarrollado por Crytek y estos archivos se utilizan para almacenar modelos de personajes y datos asociados para su uso en videojuegos y otras aplicaciones en tiempo real.

## Archivo de caracteres CryENGINE

Un archivo de caracteres CryENGINE normalmente contiene los siguientes componentes:

1. **Modelo de personaje**: Este es un modelo 3D de personaje, incluyendo su geometría, texturas y animaciones. Estos modelos suelen crearse utilizando software como Autodesk Maya o Blender y luego se importan a CryENGINE.
    




















2. **Datos de animación**: CryENGINE admite animaciones complejas para personajes, por lo que el archivo ".chr" puede incluir varias animaciones como caminar, correr, saltar y más. Estas animaciones normalmente se almacenan como datos de fotogramas clave.
    




















3. **Información de rigging**: rigging se refiere al proceso de creación de una estructura esquelética para el modelo de personaje, que permite aplicar animaciones al modelo. El archivo ".chr" puede contener información sobre la jerarquía ósea y cómo la malla del personaje está conectada a este esqueleto.
    




















4. **Datos de materiales y texturas**: la información sobre los materiales utilizados en el modelo de personaje y los mapas de textura asociados pueden incluirse en el archivo ".chr". CryENGINE admite renderizado físico, por lo que estos materiales pueden ser bastante detallados.
    




















5. **Datos físicos**: si el personaje está destinado a interactuar con el mundo del juego, el archivo ".chr" puede incluir datos físicos como formas de colisión o restricciones para la física de muñecos de trapo.
    




















6. **Ajustes de configuración**: varios ajustes de configuración relacionados con el comportamiento del personaje en el mundo del juego, como el comportamiento de la IA o eventos programados, también pueden formar parte del archivo ".chr".

## Motor grito

CryENGINE es un potente motor de juegos desarrollado por Crytek, una empresa alemana de videojuegos. Es conocido por sus capacidades gráficas de vanguardia y se ha utilizado para crear algunos videojuegos visualmente impresionantes y tecnológicamente avanzados. A continuación se muestran algunas características e información clave sobre CryENGINE:

1. **Gráficos y renderizado**: CryENGINE es reconocido por sus capacidades gráficas avanzadas. Admite funciones como iluminación global en tiempo real, iluminación y sombras dinámicas de alta calidad, renderizado basado físicamente (PBR) y texturas de alta resolución. Estas características contribuyen a crear mundos de juego realistas y visualmente impresionantes.
    




















2. **Motor de física**: CryENGINE incluye un motor de física incorporado que permite interacciones realistas entre objetos en el mundo del juego. Admite funciones como física de cuerpo rígido, física de cuerpo blando y física de muñeco de trapo, lo que lo hace adecuado para crear entornos dinámicos e inmersivos.
    




















3. **Terreno y vegetación**: CryENGINE proporciona herramientas para crear entornos exteriores amplios y detallados. Admite la edición del terreno, la ubicación de la vegetación y los sistemas climáticos dinámicos, lo que permite a los desarrolladores crear entornos exteriores amplios y realistas.
    




















4. **Animación de personajes**: CryENGINE incluye herramientas sólidas para la animación de personajes. Admite complejas plataformas de personajes, animación facial y un sistema de árbol de mezcla que permite a los desarrolladores crear animaciones y movimientos de personajes realistas.
    




















5. **Sistema de IA**: El motor presenta un sistema de IA que permite la creación de NPC inteligentes (personajes no jugadores) e IA enemiga. Los desarrolladores pueden programar el comportamiento y las interacciones de la IA para crear experiencias de juego desafiantes e inmersivas.
       





















6. **Secuencias de comandos**: CryENGINE utiliza un lenguaje de secuencias de comandos llamado "Schematyc" que permite a los desarrolladores crear interacciones y lógica de juego. Además, es compatible con C++ para necesidades de programación más avanzadas.

## Formatos de archivo utilizados por CryENGINE

Estos son algunos de los tipos de archivos comunes asociados con CryENGINE:

1. **cryproj**: archivos de proyecto CryENGINE. Estos archivos almacenan configuraciones y ajustes específicos del proyecto para un proyecto de juego en particular.
    




















2. **.level**: Los archivos de nivel contienen datos del mundo del juego en 3D, incluido el terreno, los objetos, la iluminación y otras configuraciones específicas del nivel. Los niveles son un componente fundamental del diseño de juegos en CryENGINE.
    




















3. **.cgf**: Formato de geometría de caracteres. Estos archivos contienen datos de modelos 3D para personajes, objetos y otros activos del juego. Los archivos CGF pueden incluir geometría, texturas y datos de animación.
    




















4. **.chrparams**: Archivos de parámetros de caracteres. Estos archivos almacenan ajustes y configuraciones para modelos de personajes y sus animaciones.
    




















5. **.dds**: Formato de textura DirectX. CryENGINE suele utilizar archivos DDS para almacenar texturas, incluidos mapas difusos, mapas normales y otros tipos de texturas.
    




















6. **.cryshader**: archivos CryENGINE Shader. Estos archivos definen cómo se representan los materiales y objetos en el mundo del juego, especificando sombreadores, propiedades de los materiales y más.
    




















7. **.crytif**: Archivo de información de textura. Estos archivos almacenan información adicional sobre texturas, como configuraciones de compresión, mapas MIP y otros detalles relacionados con las texturas.
    




















8. **.cdf**: Archivo de definición de caracteres. Los archivos CDF se utilizan para definir recursos de personajes y sus propiedades, incluidos archivos adjuntos, estados de animación y configuraciones relacionadas con los personajes.
    




















9. **.dds**: CryENGINE también utiliza archivos DDS (DirectDraw Surface) para varios mapas de textura, como mapas normales, mapas especulares y mapas difusos.
    




















10. **.anim**: Archivos de animación. Estos archivos almacenan datos de animación para personajes y objetos, incluidos fotogramas clave, posiciones de huesos y secuencias de animación.
    




















11. **.xml**: Los archivos XML se pueden usar para diversas configuraciones y definiciones de datos dentro de CryENGINE, como lógica de juego, comportamiento de IA y más.
    




















12. **.pak**: [archivos PAK](/es/game/pak/) son archivos de almacenamiento que se utilizan para empaquetar activos y recursos del juego, lo que los hace más eficientes para la distribución y carga del juego.

## ¿Cómo abrir el archivo CHR?

Los programas que abren archivos CHR incluyen

- **Crytek CryENGINE SDK** (prueba gratuita) para Windows

**Subtipo:** Archivos de imágenes 3D

## Otros archivos CHR

Aquí hay otros tipos de archivos que usan la extensión de archivo **.chr**.

**3D**
- [CHR - Archivo de personajes CryENGINE](/es/3d/chr-cryengine/)
- [CHR - Archivo de personajes de 3ds Max](/es/3d/chr-3ds/)

**Fuente y juego**
- [CHR - Conjunto de caracteres de Borland](/es/font/chr/)
- [CHR - ¡Club de literatura Doki Doki! Archivo de personaje](/es/game/chr-doki/)

## Referencias
- [Motor Cry](https://en.wikipedia.org/wiki/CryEngine)

