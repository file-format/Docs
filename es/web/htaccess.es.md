{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo HTACCESS - Formato de archivo Apache HTACCESS",
  "description" :"Tu guía de formato de archivo para saber qué es un archivo HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo HTACCESS?

Un archivo HTACCESS es un archivo de configuración de Apache que proporciona un mecanismo para permitir cambios de configuración para diferentes carpetas/directorios de un sitio web. Incluye directivas de configuración que son aplicables al directorio y subdirectorios.

Un archivo HTACCESS realiza una serie de comprobaciones, como definir la página de índice de un sitio web, enumerar la página de error 404 (Página no encontrada), realizar redireccionamientos de página 301 o 302, bloquear el acceso desde una dirección IP específica u otros sitios web. El uso de archivos .htaccess, por lo tanto, ralentiza el rendimiento general de su servidor Apache [HTTP](/es/web/http/).

## Formato de archivo HTACCESS

Los archivos HTACCESS se almacenan en el disco en formato de archivo de texto sin formato. Esto significa que puede abrir y editar estos archivos en cualquier editor de texto. No hay ningún nombre antes del "." en un archivo .htaccess, mostrando que es un archivo oculto dentro de la carpeta.

## Usos comunes de un archivo HTACCESS

Cinco usos comunes de un archivo HTACCESS son los siguientes.

### Mod_Reescribir

Se puede usar un archivo HTACCESS para designar y modificar cómo se muestran a los usuarios las URL y las páginas web de un sitio web.

### Autenticación

La autenticación se puede lograr con .htaccess creando un archivo de contraseña llamado .htpasswd. Esto permite a los visitantes del sitio proporcionar una contraseña si desean visitar una determinada sección de la página web.

### Páginas de error personalizadas

Puede crear páginas de error personalizadas como 400 Solicitud incorrecta, 401 Autorización requerida, 403 Página prohibida, 404 Archivo no encontrado y 500 Error interno con archivo .htaccess. Sin embargo, esto ralentizará el rendimiento del servidor, ya que todas estas comprobaciones se ejecutarán cuando se acceda a las páginas.

### Tipos MIME

Los archivos Apache HTACCESS se pueden modificar para incluir tipos de extensiones multipropósito de correo de Internet (MIME). Esto permite que su servidor admita la entrega de archivos de aplicaciones que no eran compatibles con el sitio.

### SSI

El lado del servidor incluye (SSI) actúa como un gran ahorro de tiempo en un sitio web. SSI se puede habilitar insertando el siguiente código en su archivo .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Ejemplo de archivo Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referencias

* [Tutorial del servidor Apache HTTP: archivos .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

