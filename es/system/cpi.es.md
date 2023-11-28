{
"fecha": "2023-10-18",
   "keywords":[
"ipc",
"archivo cpi",
"archivo de información de página de códigos cpi",
"cómo abrir un archivo cpi",
"archivo",
"extensión de archivo cpi",
"extensión",
"archivo"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo CPI: archivo de información de página de códigos",
   "description":"Obtenga más información sobre el formato de archivo de información de página de códigos CPI y las API que pueden crear y abrir archivos CPI.",
"linktitle":"IPC",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
"parent" : "system"
}
},
"último mod": "2023-10-18"
}

## ¿Qué es un archivo CPI?

Un archivo `.cpi`, en el contexto de los sistemas operativos Microsoft Windows y DOS, suele ser **"Archivo de información de página de códigos".** Estos archivos contienen información sobre las páginas de códigos utilizadas para la codificación de texto y las asignaciones de juegos de caracteres. Las páginas de códigos son esenciales para mostrar y procesar texto en varios idiomas y conjuntos de caracteres.

En el contexto de Windows y DOS, las páginas de códigos se utilizan para definir cómo se representan y codifican los caracteres en diferentes idiomas y regiones. Estas páginas de códigos determinan cómo se almacenan los caracteres en la memoria y se muestran en la pantalla. Cada página de códigos tiene un identificador único y los archivos `.cpi` almacenan información sobre estas páginas de códigos, incluidos detalles como asignaciones de caracteres e información de fuentes.

Los archivos `.cpi` se encuentran comúnmente en los directorios del sistema Windows o DOS y desempeñan un papel crucial al permitir que el sistema operativo muestre texto correctamente para diferentes configuraciones regionales y conjuntos de caracteres. Ayudan al sistema a comprender cómo interpretar y representar caracteres de diferentes idiomas y codificaciones.

## Archivos de información de página de códigos

Echemos un vistazo más de cerca a los archivos de información de página de códigos (.cpi) y cómo funcionan dentro del marco de MS-DOS y versiones anteriores de Microsoft Windows:

1. **Codificación de caracteres y páginas de códigos**: las páginas de códigos son un componente fundamental de cómo se codifica y muestra el texto en la computadora. Definen la codificación de caracteres para un idioma o conjunto de caracteres específico. Cada página de códigos asigna valores numéricos (puntos de código) a los caracteres, lo que permite que la computadora los represente y muestre. Por ejemplo, la página de códigos 437 se usa comúnmente en Estados Unidos y Europa occidental, mientras que la página de códigos 850 se usa para la codificación Latin-1.
    







2. **Inicialización del sistema**: Durante la inicialización del sistema (cuando se inicia la computadora), MS-DOS y versiones anteriores de Windows leerían archivos `.cpi` para determinar qué páginas de códigos admitir. Esta información fue crucial para la representación de texto, la entrada de teclado y las conversiones de juegos de caracteres.
    







3. **Compatibilidad con pantalla y teclado**: estos archivos brindan información sobre cómo se deben mostrar los caracteres en la pantalla y qué conjuntos de caracteres o páginas de códigos deben ser compatibles con la entrada del teclado. Diferentes páginas de códigos definen diferentes conjuntos de caracteres, por lo que estos archivos ayudan al sistema operativo a saber cómo manejar la entrada del usuario y mostrar el texto correctamente.
    







4. **Localización**: los archivos `.cpi` son esenciales para la localización del sistema operativo. Permiten que el sistema se adapte a diferentes idiomas, regiones y conjuntos de caracteres, lo que permite a los usuarios de todo el mundo utilizar MS-DOS o Windows en sus idiomas preferidos.
    







5. **Múltiples archivos `.cpi`**: en una computadora con soporte multilingüe, es posible que encuentre varios archivos `.cpi` correspondientes a diferentes páginas de códigos. Por ejemplo, el sistema podría tener "437.cpi" para Estados Unidos, "850.cpi" para Latin-1, "852.cpi" para Europa Central, etc. El archivo apropiado se carga según la configuración regional del usuario o la página de códigos seleccionada.
    







6. **Información de fuente**: Además de las asignaciones de caracteres, estos archivos pueden contener información de fuente, especificando qué fuentes usar para cada página de códigos. Esto es importante para representar el texto con el estilo y tamaño adecuados.
    







7. **Sistemas heredados**: los archivos `.cpi` eran más comunes en versiones anteriores de MS-DOS y Windows. Las versiones modernas de Windows (como Windows 10 y posteriores) suelen utilizar Unicode para la codificación de texto, que admite una amplia gama de caracteres e idiomas. Unicode simplifica el procesamiento de textos para entornos multilingües y es estándar para el software moderno.

## ¿Cómo abrir el archivo CPI?

Abrir el archivo .CPI (información de página de códigos) no es una acción típica del usuario y, por lo general, estos archivos no deben abrirse manualmente. El sistema operativo los utiliza para administrar la codificación de texto y los juegos de caracteres, y el sistema accede y utiliza automáticamente su contenido.

Sin embargo, si está interesado en ver el contenido del archivo .CPI con fines informativos, puede intentar abrirlo con un editor de texto o un visor hexadecimal. Así es como puedes intentar abrir el archivo .CPI:

1. **Editor de texto**: puede utilizar un editor de texto como el Bloc de notas (en Windows) o cualquier editor de texto sin formato en otros sistemas operativos para abrir y ver el archivo .CPI. Tenga en cuenta que el contenido de los archivos .CPI no está diseñado para ser legible por humanos y es posible que vea series de caracteres que son difíciles de interpretar.
    







2. **Visor hexadecimal**: se puede utilizar un visor hexadecimal o un editor hexadecimal para abrir e inspeccionar el contenido del archivo .CPI en su formato binario sin formato. Los editores hexadecimales proporcionan una vista más detallada de los datos del archivo, lo que puede resultar útil si intentas comprender su estructura. Ejemplos de dicho software incluyen HxD, Hex Fiend (para macOS) y 010 Editor.

## Otros archivos CPI

Aquí hay otros tipos de archivos que usan la extensión de archivo **.cpi**.

**Sistema de vídeo**
- [CPI - Información del videoclip AVCHD](/es/video/cpi/)
- [CPI - Archivo de información de página de códigos](/es/system/cpi/)

## Referencias
* [Página de códigos](https://en.wikipedia.org/wiki/Code_page)

