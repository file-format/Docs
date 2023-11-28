{
"fecha": "2023-06-08",
  "keywords": [
"archivo hpp",
"¿Qué es un archivo hpp?",
"¿Qué contiene el archivo hpp?",
"ejemplo de archivo hpp",
"¿Cuál es el formato del archivo hpp?",
"archivo",
"extensión de archivo hpp",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo HPP - Archivo de encabezado C++",
  "description":"Obtenga más información sobre el formato HPP y las API que pueden crear y abrir archivos HPP.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
"parent" : "programming"
}
},
"lastmod": "2023-06-08"
}

## ¿Qué es un archivo HPP?

El formato de archivo ".hpp" se usa comúnmente para archivos de encabezado en el lenguaje de programación C++. Los archivos de encabezado suelen contener declaraciones y definiciones de funciones, clases, variables y constantes que utilizan otros archivos de código fuente en el proyecto C++.

El propósito de utilizar archivos de encabezado es proporcionar una manera de compartir código común entre múltiples archivos de código fuente sin duplicar el código en sí. Cuando el archivo fuente de C++ necesita acceder a declaraciones o definiciones desde el archivo de encabezado, incluye el archivo de encabezado mediante la directiva de preprocesador `#include`.

La extensión de archivo ".hpp" se utiliza a menudo para indicar que un archivo es un archivo de encabezado C++. No es un requisito utilizar esta extensión específica para archivos de encabezado y también puede encontrar archivos de encabezado con ".h" u otras extensiones. La elección de la extensión es en gran medida una cuestión de convención y preferencia personal.

Cuando un archivo fuente de C++ incluye un archivo de encabezado usando `#include`, el compilador combina efectivamente el contenido del archivo de encabezado con el archivo fuente antes de compilarlo como una unidad. Esto permite que el archivo fuente acceda a declaraciones y definiciones en el archivo de encabezado, proporcionando la información necesaria para que el compilador realice la verificación de tipos y la generación de código.

## ¿Qué contiene el archivo HPP?

A continuación se muestran algunos contenidos comunes que puede encontrar en el archivo ".hpp":

- **Declaraciones de funciones:** Los archivos de encabezado a menudo incluyen declaraciones de funciones sin sus implementaciones reales. Estas declaraciones proporcionan información sobre el nombre de la función, el tipo de retorno y los parámetros, lo que permite que otros archivos de código fuente utilicen la función sin necesidad de conocer los detalles de implementación.
- **Declaraciones de clase:** Los archivos de encabezado pueden contener declaraciones de clase, incluido el nombre de la clase, variables miembro, funciones miembro y especificadores de acceso. Al incluir la declaración de clase en el archivo de encabezado, otros archivos de código fuente pueden crear objetos de esa clase y acceder a sus miembros.
- **Declaraciones de constantes:** Los archivos de encabezado pueden definir constantes, como variables globales o valores de enumeración que deben compartirse entre varios archivos de código fuente. Se puede acceder a estas constantes incluyendo el archivo de encabezado en otros archivos fuente, lo que les permite usar las constantes definidas.
- **Definiciones de tipos:** Los archivos de encabezado pueden contener definiciones de tipos que utilizan la palabra clave "typedef" o alias de tipos que utilizan la palabra clave "using". Estas definiciones crean nuevos nombres para tipos existentes, lo que hace que el código sea más legible y fácil de mantener.
- **Definiciones de funciones en línea:** En algunos casos, los archivos de encabezado pueden contener definiciones de funciones en línea. Las funciones en línea son funciones pequeñas que se expanden en el sitio de llamada en lugar de llamarse como funciones separadas. Incluir la definición de función en línea en el archivo de encabezado permite al compilador reemplazar la llamada a la función con el cuerpo de la función directamente, lo que potencialmente mejora el rendimiento.

## Ejemplo de archivo HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## ¿Cuál es el formato del archivo HPP?

HPP es un archivo de texto plano pero sigue las reglas generales y la sintaxis del lenguaje de programación C++. A continuación se muestra un desglose del formato general y la estructura del archivo ".hpp":

- **Protectores de encabezado:** Normalmente, un archivo ".hpp" comienza con protectores de encabezado para evitar inclusiones múltiples del mismo archivo. Esto se logra utilizando directivas de preprocesador como `#ifndef`, `#define` y `#endif`. La protección del encabezado garantiza que el contenido del archivo se incluya solo una vez durante el proceso de compilación.
- **Declaraciones de inclusión:** Después de las protecciones de encabezado, puede incluir otros archivos de encabezado necesarios usando la directiva `#include`. Estos pueden incluir encabezados de biblioteca estándar u otros encabezados personalizados requeridos por su código.
- **Declaraciones y Definiciones:** El contenido principal del archivo ".hpp" son las declaraciones y, en algunos casos, definiciones de clases, funciones, constantes, alias de tipos y otros elementos. Por ejemplo, puede declarar clases usando la palabra clave `class`, funciones usando su tipo de retorno, nombre y lista de parámetros, y constantes usando la palabra clave `const` seguida de su tipo y nombre.
- **Definiciones de funciones en línea:** En ciertos casos, puede incluir definiciones de funciones en línea directamente en el archivo ".hpp". Las funciones en línea generalmente se definen dentro del cuerpo de la clase, lo que significa que la definición de la función se incluye junto con su declaración. Esto se puede hacer anteponiendo la definición de función con la palabra clave "inline".
- **Declaraciones de espacios de nombres:** Si utiliza espacios de nombres en su código, puede declararlos dentro del archivo ".hpp". Esto se hace usando la palabra clave `namespace` seguida del nombre del espacio de nombres y encerrando el código relevante dentro del bloque de espacio de nombres.

## Referencias
* [Archivos de encabezado (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

