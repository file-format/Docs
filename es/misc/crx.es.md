{
"fecha": "2023-06-08",
  "keywords": [
"archivo crx",
"¿Qué es un archivo CRX?",
"cómo instalar el archivo crx en google chrome",
"cómo abrir un archivo crx",
"¿Qué contiene el archivo crx?",
"¿Cuál es el formato del archivo crx?",
"archivo",
"extensión de archivo crx",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CRX - Extensión de Google Chrome",
  "description":"Obtenga más información sobre el formato CRX y las API que pueden crear y abrir archivos CRX.",
"linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent" : "misc"
}
},
"lastmod": "2023-06-08"
}

## ¿Qué es un archivo CRX?

El formato de archivo CRX está asociado con las extensiones del navegador Google Chrome. Un archivo CRX es esencialmente un paquete comprimido que contiene los archivos y metadatos necesarios para instalar y ejecutar una extensión en Google Chrome. Mejora la funcionalidad o apariencia de un navegador web al proporcionar una característica o tema adicional.

Cuando se descarga e instala un archivo CRX en Google Chrome, el navegador verifica la integridad de la extensión utilizando una clave pública y una firma. Si la verificación es exitosa, Chrome extrae el contenido del archivo CRX e instala la extensión, dejándolo disponible para su uso. Los usuarios pueden administrar sus extensiones a través de la página Extensiones de Chrome, que permite habilitar, deshabilitar o eliminar extensiones instaladas.

## ¿Cómo instalar el archivo CRX en Google Chrome?

Para instalar un archivo CRX en Google Chrome, puedes seguir estos pasos:

1. Abra el navegador Chrome.
2. Escriba `chrome://extensions` en la barra de direcciones y presione Entrar.
3. Habilite el interruptor de palanca "Modo de desarrollador" ubicado en la esquina superior derecha de la página Extensiones.
4. Haga clic en el botón "Cargar descomprimido".
5. Localice y seleccione la carpeta que contiene el contenido extraído del archivo CRX (o simplemente seleccione el archivo CRX).
6. Haga clic en "Abrir" para instalar la extensión.

## ¿Qué contiene el archivo CRX?

Un archivo CRX contiene los archivos y metadatos necesarios para la extensión de Google Chrome. A continuación se muestra un desglose del contenido típico que se encuentra en un archivo CRX:

- **Archivo de manifiesto (manifest.json):** Este archivo es un archivo con formato JSON que incluye información sobre la extensión, como su nombre, versión, descripción, permisos y scripts en segundo plano. Define la estructura y comportamiento de la extensión.
- **Archivos JavaScript:** Estos archivos contienen el código que define la funcionalidad de la extensión. Pueden incluir scripts para manejar eventos, modificar páginas web o interactuar con las API de Chrome.
- **Archivos HTML, CSS y de imagen:** Las extensiones suelen incluir elementos de la interfaz de usuario, como ventanas emergentes o páginas de opciones. Los archivos HTML definen la estructura de estas interfaces, mientras que los archivos CSS controlan su apariencia. Los archivos de imagen se utilizan para iconos u otros recursos gráficos.
- **Archivos de recursos opcionales:** Las extensiones pueden incluir recursos adicionales, como archivos de localización para admitir varios idiomas. Estos archivos contienen traducciones de texto utilizado en la interfaz de usuario de la extensión.
- **Scripts en segundo plano:** Si una extensión tiene procesos en segundo plano o scripts que se ejecutan independientemente de la página web activa, estos scripts se incluirán en el archivo CRX.
- **Scripts de contenido:** Los scripts de contenido son scripts que se pueden inyectar en páginas web para modificar su comportamiento o interactuar con su contenido. Si la extensión utiliza secuencias de comandos de contenido, los archivos necesarios para esas secuencias de comandos estarán presentes en el archivo CRX.
- **Otros activos:** Dependiendo de los requisitos específicos de la extensión, se pueden incluir archivos adicionales como archivos de audio o video, fuentes o archivos de datos.

El formato de archivo CRX es esencialmente un paquete comprimido que contiene todos estos archivos y carpetas de forma estructurada. Cuando se instala el archivo CRX en Google Chrome, el navegador extrae el contenido y lo coloca en las ubicaciones apropiadas, lo que permite que la extensión se cargue y ejecute dentro del navegador.

## ¿Cuál es el formato del archivo CRX?

El formato de archivo CRX es un formato específico para empaquetar y distribuir extensiones de Google Chrome. Es esencialmente un archivo ZIP comprimido con diferentes extensiones de archivo. La estructura básica del archivo CRX es la siguiente:

- **Firma del archivo:** Los primeros 4 bytes del archivo contienen el número mágico "Cr24" (hexadecimal: 43 72 32 34) que sirve como firma para identificar el archivo como archivo CRX.
- **Número de versión:** Los siguientes 4 bytes representan el número de versión del formato CRX.
- **Longitud de la clave pública:** Los siguientes 4 bytes indican la longitud de la clave pública codificada utilizada para la verificación de la firma de la extensión.
- **Longitud de la firma:** Los 4 bytes siguientes especifican la longitud de la firma de la extensión.
- **Clave pública:** Esta sección contiene la clave pública codificada utilizada para verificar la integridad de la extensión.
- **Firma:** Esta sección contiene la firma de la extensión, que se genera al firmar el contenido de la extensión utilizando una clave privada correspondiente a la clave pública mencionada anteriormente.
- **Archivo ZIP:** Los bytes restantes del archivo CRX constituyen un archivo ZIP comprimido. Este archivo contiene todos los archivos y carpetas de extensión necesarios, incluidos archivos de manifiesto, archivos JavaScript, archivos HTML, archivos CSS, imágenes y cualquier otro recurso.

## Referencias
* [especificación de formato CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

