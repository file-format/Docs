{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo LOCK - ¿Qué es un archivo Lock?",
  "description":"Más información sobre el formato de archivo LOCK y su .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## ¿Qué es un archivo LOCK?

Un archivo **LOCK** es un archivo renombrado que utilizan las aplicaciones y los sistemas operativos para marcar un archivo o algún dispositivo como bloqueado. Esto le dice a otras aplicaciones que no usen el archivo a menos que esté libre de la aplicación que lo está usando. En la mayoría de los casos, estos archivos de bloqueo están vacíos, pero en otros casos, pueden contener información relacionada con el bloqueo, como propiedades y configuraciones.

A veces, el .NET Framework de Microsoft utiliza el archivo .lock para crear copias **lockeed** de un archivo de base de datos. En tal caso, se abrirá una copia del archivo de la base de datos con la extensión .lock. Esto no permite que el usuario realice cambios en el archivo mientras lo está utilizando otro usuario.

## Formato de archivo LOCK - Más información

Cada aplicación crea un archivo LOCK y su formato de archivo es específico para la aplicación. Estos archivos de bloqueo se pueden guardar tanto en texto como en formato de archivo binario.

La presencia de archivos de bloqueo impide el acceso simultáneo de un recurso a varios archivos que intentan acceder a ese recurso. Se crea una copia del archivo original con la extensión .lock como sufijo a su nombre. Esto le dice a otras aplicaciones que tengan acceso de solo lectura al archivo. Por ejemplo, resource.dat se convertirá en resource.data.lock.

Para el lenguaje de programación Ruby, puede encontrar el archivo **gemfile.lock**. Aquí es donde Bundler mantiene un registro de las versiones exactas que se instalaron. Por lo tanto, cuando un proyecto/biblioteca se mueve a otra máquina, el paquete en ejecución buscará en el archivo Gemfile la versión relevante exacta.

## Bloquear archivo en Linux

Linux admite dos tipos de bloqueos de archivos: bloqueos de aviso y bloqueos obligatorios.

* **Bloqueos de aviso**: tipo de bloqueo que no se aplica. En este caso, los procesos participantes cooperan entre sí adquiriendo bloqueos de forma explícita. Si esto no es posible, se ignoran los bloqueos de aviso.

* **Bloqueos obligatorios**: en caso de bloqueo obligatorio, el sistema operativo impone el bloqueo del archivo evitando que otros procesos lean o escriban el archivo. Esto no requiere ninguna cooperación entre los procesos.

el bloqueo obligatorio no requiere ninguna cooperación entre los procesos participantes. Una vez que se activa un bloqueo obligatorio en un archivo, el sistema operativo evita que otros procesos lean o escriban el archivo.

## Referencias

* [GemFile y Gemfile.lock en Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Bloqueo en Linux](https://www.baeldung.com/linux/file-locking)

