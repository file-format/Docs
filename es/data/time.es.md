{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Archivo TIME: ¿Qué es el archivo .time? Hora en que se creó el archivo en Linux",
  "description" : "Obtenga más información sobre el archivo TIME y descubra la hora en la que se creó el archivo en Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## ¿Qué es un archivo TIEMPO?

El formato de archivo TIME fue utilizado por un sistema web llamado LIGHT, que ayudó a los usuarios a registrar, organizar y compartir sus vidas. Básicamente, almacenaba una colección de publicaciones y representaba una carpeta en la página de vida del usuario dentro del sistema.

## Cómo saber cuándo se creó un archivo en Linux

En Linux, puede utilizar el comando `stat` para saber cuándo se creó un archivo. Aquí sabrás como podrás hacerlo:

Abra una terminal y escriba el siguiente comando:

```
stat <file_path>
```

Reemplazar `<file_path> ` con la ruta al archivo que le interesa. Por ejemplo:

```
stat /path/to/your/file.txt
```

Este comando mostrará diversa información sobre el archivo, incluida su hora de creación. Busque la línea que comienza con Nacimiento o Archivo:. La hora de nacimiento indica cuándo se creó el archivo en el sistema de archivos.

A continuación se muestra un ejemplo de cómo podría verse el resultado:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

En este ejemplo, la hora de Nacimiento indica cuándo se creó el archivo.

