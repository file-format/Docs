---
date: 2020-11-11
keywords: myi, .myi, formato de archivo myi, cómo abrir archivos myi, extensión .myi, extensión myi
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de archivo MII
linktitle: MYI
description: "Obtenga información sobre el formato de archivo MYI y las API que pueden crear y abrir archivos MYI."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## ¿Qué es un archivo MYI? ##

MYI también se conoce como el archivo de índice MySQL MyISAM. Se utiliza para almacenar índices para la tabla MyISAM de MySQL. El índice de la base de datos MySQL define la estructura de la tabla y contiene el mecanismo de control para verificar la integridad de las tablas.

## Formato de archivo MYI ##

El archivo MYI tiene dos partes, el encabezado y los valores clave.

### Encabezado MYI ###

El encabezado contiene información sobre opciones, tamaños de archivo y claves. Las claves en MySQL se crean con un comando como

```sql
CREATE [UNIQUE] INDEX.
```

Los archivos que leen y escriben archivos MYI están en el directorio ./myisam. Tiene los siguientes archivos:

- mi_open.c: Este archivo contiene las rutinas que escriben cada sección de la cabecera.
- mi_create.c: Este archivo tiene las rutinas que llaman a las rutinas mi_open.c.
- myisamdef.h: Este archivo tiene las definiciones de la estructura.

El encabezado tiene las siguientes secciones:

- estado: El estado está escrito por mi_open.c, mi_state_info_write(). Esta estructura aparece una vez en el archivo.
- base: La base está escrita por mi_open.c, mi_base_info_write(). MI_BASE_INFO es la estructura correspondiente para la base en myisamdef.h. Esta estructura aparece una vez en el archivo.
- keydef: El keydef está escrito por mi_open.c, mi_keydef_write(). MI_KEYDEF es la estructura correspondiente para keydef en myisamdef.h. Es una estructura de múltiples ocurrencias que aparece para cada índice.
- recinfo: El recinfo está escrito por mi_open.c, mi_recinfo_write(). MI_COLUMNDEF es la estructura correspondiente para recinfo en myisamdef.h. Es una estructura de ocurrencia múltiple que aparece una vez de cada campo que aparece en una clave.

### Valores clave ###

Las páginas en MySQL se llaman bloques. Los valores clave están en bloques. Un bloque contiene información de un solo índice. Cada clave contiene el contenido completo de todas las columnas. La longitud normal del bloque es 0x0400 (1024) bytes. El puntero tiene un número de tamaño fijo (4 bytes) para tablas de filas fijas que contienen un número de fila ordinal. Si la clave es nula, el byte es 0x00. Un bloque normal tiene al menos un 65 % de su capacidad y, por lo general, un 80 % de su capacidad.

El archivo myisamdef.h contiene la siguiente información expresada en constantes. El número máximo de claves es 32 (MI_MAX_KEY) y el número máximo de segmentos en una clave es 16 (MI_MAX_KEY_SEG). La longitud máxima de la clave es 500 (MI_MAX_KEY_LENGTH). La longitud máxima del bloque es 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## Referencias ##

- [El archivo .MYI](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

