{
  "date" : "2021-06-28",
  "keywords" :[ "archivo cgi", "qué es un archivo cgi", "archivo", "ejemplo cgi", "extensión de archivo cgi","extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo CGI y las API que pueden crear y abrir archivos CGI",
  "title" :"CGI - Archivo de script de interfaz de puerta de enlace común",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## ¿Qué es un archivo CGI?
Un archivo CGI se conoce como una secuencia de comandos de interfaz de puerta de enlace común que utiliza un servidor web para ejecutar un programa externo para procesar las solicitudes de los usuarios. El script que se guardó en un archivo con extensión .cgi generalmente está escrito en lenguajes de programación C o Perl. Se habían introducido desde los primeros días de la web, cuando los desarrolladores web querían conectar bases de datos a sus servidores web. Un servidor que admitiera una puerta de enlace común entre el servidor web y las bases de datos era adecuado para ejecutar el código CGI.

## Formato de archivo CGI
Los scripts CGI son utilizados por el servidor web para facilitar al propietario la configuración de cómo se manejará una URL. El procedimiento generalmente se realiza marcando un nuevo directorio (donde se encuentran principalmente los documentos) que contiene scripts CGI; su nombre comúnmente conocido es cgi-bin. Por ejemplo, /usr/local/apache/htdocs/cgi-bin podría elegirse como un directorio CGI en el servidor web. Cuando un navegador web solicita una URL que apunta a un archivo dentro del directorio CGI, entonces, en lugar de simplemente enviar ese archivo (/es/usr/local/apache/htdocs/cgi-bin/printenv.pl) al navegador web, el HTTP El servidor ejecuta la secuencia de comandos especificada y devuelve la salida de la secuencia de comandos al navegador web. En resumen, todo lo que el script CGI se envía a la salida estándar se transfiere al cliente web en lugar de mostrarse en una terminal de ventana.

### Ejemplo CGI

Siguiendo el script CGI escrito en Perl que muestra todas las variables de entorno pasadas por el servidor web:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

La salida será como la siguiente:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Usos de scripts CGI
Los archivos CGI que contienen los scripts CGI generalmente se usan para procesar datos de entrada del usuario y producir los datos de salida relevantes. La implementación de un wiki es uno de los ejemplos del programa CGI. Si el agente de usuario envía una solicitud del nombre de una entrada, el servidor web ejecuta el programa CGI. El programa CGI obtiene la fuente de la página de esa entrada, la convierte en HTML e imprime el resultado. El servidor web recibe la salida del programa CGI y la devuelve al agente de usuario. Luego, si el agente de usuario llama a la función de edición haciendo clic en el botón "Editar página", el programa CGI muestra un área de texto HTML u otro control de edición con el contenido de la página. Finalmente, si el agente de usuario hace clic en el botón "Publicar página", el programa CGI convierte el HTML actualizado en el código fuente de la página de esa entrada y lo guarda.



## Referencias

* [Interfaz de puerta de enlace común - por Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

