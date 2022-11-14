{
  "date" : "2021-08-02",
  "keywords" :[ "archivo de registro", "formato de archivo de registro", "qué es un archivo de registro", "archivo", "ejemplo de registro", "extensión de archivo de registro", "extensión", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo REG y las API que pueden crear y abrir archivos REG",
  "title" :"REG - Archivo de registro de Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## ¿Qué es un archivo REG?
Un archivo REG es simplemente un archivo de texto con la extensión .reg. Estos archivos generalmente se crean exportando claves típicas del Registro. Estos archivos también se pueden usar como una copia de seguridad del registro (¡especialmente este paso es importante antes de realizar cambios!). Puede ver que algunos los pusieron a disposición como archivos descargables en los mismos sitios que le muestran cómo realizar un hackeo del Registro. Un archivo REG es útil para realizar cambios manuales en el Registro y exportar esos cambios. Simplemente limpie un poco el archivo y luego compártalo con otros.

## Formato de archivo REG
El formato de archivo REG se diseñó para exportar e importar partes del registro de Windows utilizando una sintaxis basada en INI. El Registro de Windows es una base de datos relacional o jerárquica que mantiene la configuración de bajo nivel para el sistema operativo Microsoft Windows y otras aplicaciones que utilizan el registro de Windows. Alternativamente, podemos decir que el registro o Registro de Windows se compone de información, opciones, configuraciones y otros valores para los programas y el hardware instalado en todas las versiones de los sistemas operativos Microsoft Windows.
### Sintaxis del archivo REG
Estos son algunos elementos clave como parte de la sintaxis de un archivo REG:
- **RegistryEditorVersion**: Por ejemplo, "Windows Registry Editor Version 5.00" para Windows 2000, Windows XP y Windows Server 2003.
- **Línea en blanco**: identifica el inicio de una nueva ruta de registro.
- **RegistryPathx**: la ruta de la subclave que contiene el primer valor que está importando.
- **DataItemNamex**: el nombre del elemento de datos que desea importar.
- **DataTypex**: el tipo de datos para el valor del registro.

Las claves se almacenan en archivos .reg usando la siguiente sintaxis:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Puede editar el valor predeterminado de una clave utilizando "@" en lugar de "Nombre del valor":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Ejemplo
Aquí hay un ejemplo de archivo REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Referencias

* [Registro de Windows- por Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Cómo agregar, modificar o eliminar subclaves y valores del registro mediante un archivo .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- subclaves-y-valores-de-registro-mediante-el-uso-de-un-archivo-reg-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


