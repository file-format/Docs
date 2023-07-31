{
  "date" : "2022-03-21",
  "keywords" :[ "archivo xpr", "formato de archivo xpr", "qué es un archivo xpr", "archivo", "ejemplo xpr", "extensión de archivo xpr","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo XPR: archivo gráfico de diseño de expresión de Microsoft",
  "description":"Obtenga información sobre el formato de archivo XPR y las API que pueden crear y abrir archivos XPR",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-21"
}

## ¿Qué es un archivo XPR?

Un archivo XPR es un archivo de imagen vectorial creado con el software Microsoft Expression Graphics (EGD), ahora descontinuado. Contiene información gráfica que se puede utilizar como maqueta de la interfaz de usuario. Los archivos XPR fueron reemplazados posteriormente por archivos .design en Microsoft Expression Design. Los archivos XPR se pueden abrir con Microsoft Expression Studio, que se suspendió durante bastante tiempo.

## Vulnerabilidad del formato de archivo XPR

Los archivos XPR se identificaron para beneficiar una vulnerabilidad en Microsoft Expression Design, lo que permite la ejecución de código remoto. En el problema informado, si un usuario abría un archivo .xpr legítimo que se encuentra en el directorio de la red junto con un archivo de biblioteca de vínculos dinámicos (DLL), Microsoft Expression Design podría intentar cargar el archivo DLL y ejecutar el código que contenía. Microsoft solucionó esto más tarde en una actualización de seguridad.

## Referencias

* [Una vulnerabilidad en el diseño de expresiones podría permitir la ejecución remota de código (2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)

