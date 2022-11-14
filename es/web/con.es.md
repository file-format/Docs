{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo CON - Formato de archivo de origen de la aplicación de concepto",
  "description" :"Obtenga información sobre qué es un archivo CON y las API que pueden crear y abrir archivos CON",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## ¿Qué es un archivo CON?

Un archivo CON es un archivo de código fuente para una aplicación desarrollada para **Concept Application Server**. Se utiliza para escribir aplicaciones para el intercambio de datos entre el servidor y el usuario. Se puede acceder a los archivos CON alojados en el servidor con un navegador web siempre que Concept Client esté instalado en el extremo del usuario. Concept Application server es un servidor web con un lenguaje de programación a pequeña escala que puede tener un motor de base de datos subconjunto [SQL](/es/database/sql/) (TinDB).

Los archivos CON se pueden abrir/ejecutar con RadGs Concept Application Server.

## Formato de archivo CON - Más información

Los archivos CON están alojados en el servidor y se accede a ellos mediante el navegador web en la máquina del usuario. Las [URL](/es/web/url/) de concepto son diferentes a las URL HTTP normales y comienzan con **concept://**.

### Ejemplo de URL de archivo CON

Se puede acceder a un archivo CON alojado en Concept Application Server a través de un navegador web utilizando direcciones URL como:

```
concept://domain.server.com/web_application/main.con.
```
## Referencias

* [Servidor de aplicaciones conceptuales] (https://github.com/Devronium/ConceptApplicationServer)

