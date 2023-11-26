{
  "date" : "2023-01-31",
  "keywords" :["ejecutar archivo", "qué es un archivo de ejecución", "archivo", "cómo abrir un archivo de ejecución", "ejecutar extensión de archivo", "extensión"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga información sobre el formato de archivo RUN y las API que pueden crear y abrir archivos RUN.",
  "title" :"Formato de archivo RUN - Archivo ejecutable de Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## ¿Qué es un archivo RUN?

El formato de archivo .run se usa comúnmente para distribuir software o instaladores de aplicaciones en el entorno Linux. Para instalar el software, deberá hacer que el archivo sea ejecutable, lo que se puede hacer usando el siguiente comando:

```bash
chmod +x file_name.run 
```

Luego, puede ejecutar el archivo usando el siguiente comando:

```bash
./file_name.run 
```

El proceso de instalación puede variar según el archivo y programa específico que esté intentando instalar.

El formato de archivo .run es un tipo de script de shell que se utiliza para distribuir software o instaladores de aplicaciones en el entorno Linux. Es un paquete autónomo que incluye todo lo necesario para instalar el software, incluidos archivos binarios, bibliotecas y archivos de configuración.

Es importante tener en cuenta que los archivos .run también pueden contener código malicioso, por lo que siempre es una buena idea verificar el origen del archivo y escanearlo en busca de virus antes de ejecutarlo.

Además, algunos archivos .run pueden requerir privilegios de root para ejecutarse e instalarse, por lo que es posible que deba utilizar el comando "sudo" para ejecutar el archivo con permisos elevados:

```bash
sudo ./filename.run
```

## ¿Cómo abrir el archivo RUN?

Para abrir un archivo .run, debe hacerlo ejecutable, lo que se puede hacer con el comando "chmod":

```bash
chmod +x filename.run 
```

Una vez que el archivo sea ejecutable, puede ejecutarlo escribiendo:

```bash
./filename.run
```

Ejecutar un archivo .run no es lo mismo que abrirlo en un editor de texto. Al ejecutar un archivo .run se ejecutarán sus instrucciones, que pueden ser cualquier cosa, desde instalar un programa hasta ejecutar un script. Para ver el contenido de un archivo .run, debe abrirlo en un editor de texto, como nano o vim:

```
nano filename.run
```
o
```
vim filename.run
```

## Referencias
* [Cómo ejecutar archivos .bin y .run en Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


