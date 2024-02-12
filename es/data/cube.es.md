{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Archivo CUBE - Archivo cubo gaussiano - ¿Qué es el archivo .cube y cómo abrirlo?",
  "description" : "Obtenga más información sobre el archivo de cubo gaussiano y cómo abrirlo.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-es-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## ¿Qué es un archivo CUBE?

El formato de archivo CUBE, también conocido como archivo de cubo gaussiano (.cube), se utiliza en química computacional para almacenar datos moleculares, en particular información de densidad electrónica resultante de cálculos de química cuántica. Este formato se asocia comúnmente con el **paquete de software gaussiano**, que se usa ampliamente para realizar cálculos de estructuras electrónicas ab initio.

Los archivos de cubo gaussiano almacenan datos tridimensionales, que generalmente representan la densidad de electrones u otras propiedades de las moléculas, obtenidos mediante cálculos de química cuántica. El archivo contiene una sección de encabezado con metadatos (como origen, número de puntos de datos a lo largo de cada eje y espaciado), seguido de una cuadrícula de valores numéricos que representan propiedades de interés (por ejemplo, densidad de electrones) en cada punto de la cuadrícula en el espacio.

El archivo Gaussian Cube (.cube) es un archivo de texto sin formato con una estructura específica. El encabezado contiene información sobre el sistema molecular y la cuadrícula de datos, y los valores de los datos están organizados en formato de cuadrícula tridimensional. Los archivos de cubo gaussiano se utilizan a menudo para visualizar propiedades moleculares mediante software de visualización molecular. Programas como **VMD (Visual Molecular Dynamics)** o **PyMOL** pueden leer archivos de cubo gaussiano para mostrar superficies moleculares, densidad de electrones u otras propiedades calculadas.

## Ejemplo simplificado de archivo Cubo Gaussiano:

```
Ejemplo de archivo cúbico
Generado por gaussiano
   0 1 0 0 0 0 0 0 0 0
   0.0000000000000000E+00 0.0000000000000000E+00 0.0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (valores de datos para la densidad de electrones en cada punto de la cuadrícula)
```

## Acerca de Gauss

Gaussian es un conjunto de aplicaciones de software para química cuántica y química computacional. El enfoque principal de Gauss está en los métodos de química cuántica ab initio, que son enfoques altamente precisos pero computacionalmente intensivos para estudiar la estructura electrónica de las moléculas. El software se utiliza ampliamente en entornos académicos y de investigación para diversas aplicaciones, incluida la predicción de propiedades moleculares, el estudio de mecanismos de reacción y la exploración de estructuras moleculares.

## Acerca de NWChem

NWChem es un software de química computacional de código abierto diseñado para simulaciones de química cuántica de alto rendimiento. Emplea métodos ab initio como Hartree-Fock y la teoría funcional de la densidad, admite la computación paralela para cálculos eficientes en conglomerados y encuentra aplicaciones en diversos campos científicos, incluida la química computacional, la bioquímica y la ciencia de materiales. NWChem es conocido por su versatilidad, que permite a los investigadores estudiar varios sistemas químicos, y su naturaleza de código abierto fomenta las contribuciones y la personalización de la comunidad.

## Acerca de VMD

VMD, que significa Visual Molecular Dynamics, es un programa de visualización molecular potente y ampliamente utilizado para mostrar, analizar y animar trayectorias de dinámica molecular (MD), así como estructuras moleculares estáticas. Es particularmente popular en los campos de la química computacional, la biología molecular y la bioinformática estructural. VMD se destaca en la visualización de estructuras moleculares, proporcionando representaciones 3D de moléculas y complejos moleculares de alta calidad. Admite una variedad de formatos de archivos moleculares.

## Acerca de PyMOL

PyMOL es un sistema de visualización molecular y una herramienta de software que se utiliza para la visualización tridimensional de estructuras moleculares. Es particularmente popular en los campos de la biología estructural, la bioinformática y la química computacional. PyMOL proporciona representaciones 3D de alta calidad de estructuras moleculares, lo que permite a los usuarios visualizar y explorar formas, superficies e interacciones de macromoléculas biológicas.

## ¿Cómo abrir el archivo CUBE?

El archivo CUBE se puede abrir y hacer referencia a él utilizando los siguientes programas.

- **NWChem** (Gratis) para (Windows, MAC, Linux)

## Referencias
* [Formato de archivo de cubo gaussiano](https://paulbourke.net/dataformats/cube/)
