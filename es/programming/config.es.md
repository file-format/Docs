{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Archivo de configuración",
  "description":"Obtenga información sobre el formato de archivo CONFIG con el ejemplo de CONFIG y las API que pueden crear y abrir archivos CONFIG",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## ¿Qué es un archivo CONFIG?
Un archivo CONFIG se conoce como archivo de configuración; se utiliza para configurar los parámetros y ajustes principales de varios programas informáticos. Algunos softwares solo leen sus **archivos de configuración** al inicio. Otros comprueban periódicamente los archivos de configuración en busca de cambios.

## Formato de archivo de configuración
El **formato de archivo CONFIG** se utiliza para los procesos del servidor, las aplicaciones de software y la configuración del sistema operativo. Un programador puede escribir código para indicarle a un software que lea los archivos de configuración una y otra vez después de cierto período de tiempo y aplique los cambios al proceso actual. No existen estándares definitivos ni convenciones sólidas para el sistema de archivos CONFIG. Por ejemplo, el archivo Web.config de Microsoft pertenece al formato de archivo CONFIG, que consiste en un conjunto de etiquetas basado en [XML](https://docs.fileformat.com/web/xml/); se puede editar con Microsoft Visual Studio o cualquier otro editor de texto.

## Ejemplos de archivos de configuración:
Dado que los archivos de configuración no se crean siguiendo ninguna regla, estándar o convención, es posible que estos archivos se hayan escrito utilizando diferentes formatos. Un archivo .config puede estar basado en XML, [JSON](https://docs.fileformat.com/web/json/) o cualquier otro formato. Los siguientes son ejemplos de archivos de configuración para sistemas operativos y software conocidos:

### Archivos de configuración en Linux
Cada programa de Linux es un archivo ejecutable que mantiene la lista de **códigos de operación** que ejecuta la CPU para realizar operaciones típicas. Las operaciones de casi todos los programas se pueden personalizar según sus requisitos cambiando sus archivos de configuración. Varios archivos de configuración en el sistema Linux están en el directorio /etc. Los archivos de configuración se pueden clasificar en las siguientes categorías:
|Categoría|Ejemplo| Comentarios|
---|---|---|
|Acceder a archivos|/etc/host.conf|Indica al servidor de dominio de red cómo buscar nombres de host.|
|Arranque e inicio/cierre de sesión|/etc/rc.d/rc.local|No oficial. Se puede llamar desde rc, rc.sysinit o /etc/inittab.|
|Sistema de archivos|/etc/mtools.conf|Configuración de todas las operaciones (mkdir, copiar, formatear, etc.) sobre un sistema de archivos tipo DOS.|
|Administración del sistema|/etc/shells|Contiene la lista de posibles “shells” disponibles para el sistema.|
|Redes|/etc/gated.conf|Configuración para gated. Usado solo por el demonio cerrado.|
|Comandos del sistema|/etc/logrotate.conf|Configuración del Dynamic Linker.|
|Daemons|/etc/httpd.conf|El archivo de configuración de Apache, el servidor Web. Este archivo normalmente no está en /etc.|
|Programas de usuario| /etc/lynx.cfg| Configuración de proxy|
### Ejemplo de archivo de CONFIGURACIÓN de AWS
Los ajustes de configuración y las credenciales que se utilizan con frecuencia se pueden guardar en archivos CONFIG que mantiene la CLI de AWS. El archivo CONFIG debe ser un archivo de texto sin formato que use el siguiente formato:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Ejemplo de archivo SSH CONFIG
El archivo de configuración del lado del cliente de OpenSSH se llama CONFIG y se almacena en el directorio .ssh. El archivo SSH CONFIG consta de la siguiente estructura:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Ejemplo de archivo CONFIG de Python
Un archivo CONFIG de Python podría verse así:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Referencias

* [Comprensión de los archivos de configuración de Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Configuración y configuración del archivo de credenciales](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Archivos de configuración en Python](https://martin-thoma.com/configuration-files-in-python/)

