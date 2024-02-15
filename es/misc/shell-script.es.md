{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : "true",
  "title" : "Script de Shell: cómo ejecutarlo en Ubuntu y Linux",
  "description":"Aprenda qué es Shell Script y cómo ejecutarlo en Ubuntu y Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## ¿Qué es el script de Shell?

Los scripts de Shell implican escribir una serie de comandos en un archivo de texto sin formato, a menudo denominado **Script de Shell**. Estos scripts son ejecutados por un shell, que es un intérprete de línea de comandos. Los caparazones más comunes incluyen

1. Bash (Bourne otra vez SHell)
2. Zsh (Concha Z)
3. Pez.

Los scripts de Shell pueden variar desde simples frases ingeniosas hasta programas complejos, y se utilizan para realizar una amplia variedad de tareas, como manipulación de archivos, administración de sistemas y automatización de tareas repetitivas.

## Beneficios de las secuencias de comandos de Shell:

1.  **Automatización:** Los scripts de Shell permiten a los usuarios automatizar tareas repetitivas, ahorrando tiempo y reduciendo la posibilidad de errores humanos.
    
2.  **Personalización:** Los usuarios pueden crear scripts adaptados a sus necesidades específicas, proporcionando un alto grado de personalización.
    
3.  **Procesamiento por lotes:** Los scripts de Shell son excelentes para manejar tareas de procesamiento por lotes, donde es necesario ejecutar varios comandos en secuencia.
    
4.  **Administración del sistema:** Los scripts de Shell se usan comúnmente para tareas de administración del sistema, como copias de seguridad, rotación de registros e instalación de software.

## Escribir un script de Shell simple:

Creemos un script de shell básico que imprima un mensaje de saludo. Abra un editor de texto y cree un archivo llamado `greeting.sh`. Agregue las siguientes líneas:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Guarde el archivo y hágalo ejecutable ejecutando el siguiente comando en la terminal:

```
chmod +x greeting.sh
```

Ahora puedes ejecutar el script:

```
./greeting.sh
```

La salida debería ser:

```
Hello, welcome to the world of shell scripting!
```

## Ejecutar scripts de Shell en Ubuntu y Linux:

Ahora, discutiremos **cómo ejecutar un archivo .sh en Ubuntu y Linux**.

1.  **Haga que el script sea ejecutable:** Antes de ejecutar un script de shell, asegúrese de que sea ejecutable. Utilice el comando `chmod` como se mostró anteriormente.
    
2.  **Navegue al directorio de secuencias de comandos:** Abra una terminal y use el comando `cd` para navegar hasta el directorio que contiene su secuencia de comandos de shell.
    
3.  **Ejecute el script:** Ejecute el script escribiendo `./scriptname.sh` en la terminal, reemplazando scriptname con el nombre real de su script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Usando el comando Bash:** Si su script comienza con `#!/bin/bash` (conocido como **shebang**), también puede ejecutarlo usando el comando `bash`.

```
bash greeting.sh
```

## ¿Qué significa $@ en Shell Script?

En el script de shell, `$@` representa todos los argumentos de la línea de comandos pasados al script. A menudo se utiliza para hacer referencia a una lista de argumentos como entidades separadas. Cuando se usa entre comillas dobles, como `$@`, conserva argumentos individuales, teniendo en cuenta espacios y caracteres especiales.

Aquí hay una breve explicación:

- `$@`: Representa todos los parámetros posicionales (argumentos) pasados al script o función. Cada argumento se trata como una palabra independiente.
    
- `$@`: cuando está entre comillas dobles, conserva la separación de argumentos, permitiendo espacios o caracteres especiales dentro de argumentos individuales.
    

A continuación se muestra un ejemplo sencillo para ilustrar:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Cuando ejecuta este script con argumentos, por ejemplo:

```
bash example.sh arg1 "argument 2" arg3
```

Daría salida:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Como puede ver, `$@` representa todos los argumentos y `$@` conserva los argumentos individuales, incluso si contienen espacios.

