{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo Torrent - Archivo BitTorrent",
  "description":"Obtenga información sobre los archivos TORRENT y las API que pueden crear y abrir archivos TORRENT",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## ¿Qué es un archivo TORRENT?

Un archivo TORRENT es un archivo de texto que utilizan BitTorrent y otros programas P2P (peer-to-peer) para descargar e intercambiar contenido. El contenido descargable puede incluir documentos, videos, juegos, películas y otros medios disponibles en Internet. Incluye información de metadatos sobre los contenidos y la ubicación de los medios que se descargarán. El software como BitTorrent usa información de este archivo, como el nombre, el tamaño del archivo y la estructura de carpetas para descargar datos. Los archivos torrent se pueden convertir a otros formatos de archivo como [PDF](/es/pdf/) en línea.

## ¿Qué es Torrent? El formato de archivo TORRENT para el intercambio de datos

Torrenting es el concepto de intercambio (descarga y carga) de archivos de datos utilizando la red BitTorrent. A diferencia de los servidores convencionales donde los datos se cargan para que otros accedan y los descarguen, los archivos torrent se recuperan y envían mediante la red torrent. Cuando un usuario abre un archivo .torrent en aplicaciones como BitTorrent, el software comienza a descargar el contenido del archivo bit a bit. Si varios usuarios tienen el mismo archivo, BitTorrent divide las descargas entre todos los usuarios para acelerar el proceso de descarga. Al mismo tiempo, la computadora del usuario que está descargando el archivo también se convierte en la fuente del archivo para enviarlo a otros usuarios que también están descargando el mismo archivo.

### Estructura de un archivo TORRENT

Un archivo torrent es una combinación de una lista de archivos e información de metadatos sobre todas las partes del archivo que se descargarán. Contiene la siguiente información en forma de claves.

- `anunciar`: la URL del rastreador que se anuncia a otros pares para informar sobre la disponibilidad del archivo
- `info` — Esto se asigna a un diccionario cuyas claves dependen de si se comparten uno o más archivos:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `longitud` — tamaño del archivo en bytes.
- `ruta`: una lista de cadenas correspondientes a nombres de subdirectorios, el último de los cuales es el nombre real del archivo
- `longitud`: el tamaño del archivo en bytes (solo cuando se comparte un archivo)
- `name` — nombre de archivo donde se guardará el archivo
- `longitud de pieza` — número de bytes por pieza. Esto es comúnmente 28 KiB = 256 KiB = 262,144 B.
- `piezas`: una lista hash que es una concatenación del hash SHA-1 de cada pieza.

## ¿Es seguro y legal el uso de torrents?

El protocolo de torrents para el intercambio de datos entre usuarios P2P es seguro, ya que es solo el medio para compartir cualquier tipo de archivo. Por lo tanto, el protocolo en sí no es inseguro ni ilegal. Sin embargo, el contenido compartido a través de la red puede contener archivos o medios que pueden violar el estado legal de los documentos compartidos. En tal caso, el intercambio de dichos datos puede dar lugar a acciones legales contra las partes involucradas en el intercambio público de dichos archivos.

## Referencias

* [Archivo TORRENT - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

