{
"fecha": "2023-06-12",
  "keywords": [
"hornear",
"archivo bak",
"Copia de seguridad de la base de datos de Microsoft SQL Server",
"¿Qué es un archivo bak?",
"cómo abrir un archivo bak",
"archivo",
"extensión de archivo bak",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo BAK - Copia de seguridad de la base de datos de Microsoft SQL Server",
  "description":"Obtenga más información sobre el formato de copia de seguridad de BAK SQL Server y las API que pueden crear y abrir archivos BAK.",
"linktitle": "Servidor SQL BAK",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver",
"parent": "base de datos"
}
},
"lastmod": "2023-06-12"
}

## ¿Qué es un archivo BAK?

Un archivo ".bak", en el contexto de Microsoft SQL Server, es un formato de archivo de respaldo que se utiliza para almacenar copias de una base de datos de SQL Server. Estos archivos contienen una instantánea de la base de datos en un momento específico, incluido su esquema, datos y otra información relacionada. Se generan utilizando la funcionalidad integrada de copia de seguridad y restauración de SQL Server y sirven para varios propósitos cruciales:

1. **Recuperación de datos:** Los archivos .bak proporcionan un medio para recuperar una base de datos en caso de pérdida de datos, corrupción u otros problemas. Al restaurar una base de datos desde un archivo .bak, puede revertirla a un estado anterior, minimizando el tiempo de inactividad y la pérdida de datos.

2. **Migración y clonación:** Los archivos de respaldo se utilizan a menudo para migrar bases de datos entre servidores o crear copias de bases de datos con fines de prueba, desarrollo o generación de informes. Ofrecen una forma consistente y eficiente de mover bases de datos entre entornos.

3. **Recuperación de un punto en el tiempo:** SQL Server le permite realizar una recuperación de un punto en el tiempo utilizando archivos .bak. Esto significa que puede restaurar una base de datos a un momento específico, lo que puede ser crucial para el cumplimiento normativo o la auditoría de datos.

4. **Recuperación ante desastres:** Los archivos .bak son una parte fundamental de la planificación de la recuperación ante desastres. Garantizan que sus datos estén seguros y puedan restaurarse rápidamente en caso de fallas de hardware, desastres naturales u otros eventos catastróficos.

## Cree un archivo .BAK en SQL Server

Para crear un archivo .bak en SQL Server, normalmente se utilizan comandos de SQL Server Management Studio (SSMS) o Transact-SQL (T-SQL), como BACKUP DATABASE o BACKUP LOG. A continuación se muestra un ejemplo simplificado de cómo se puede crear una copia de seguridad de una base de datos utilizando T-SQL:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## Restaurar un archivo .BAK en SQL Server

Para restaurar una base de datos desde un archivo .bak, puede usar el comando RESTORE DATABASE:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## ¿Cómo abrir un archivo BAK en SQL Server?

Para abrir y acceder a los datos almacenados en un archivo ".bak", normalmente necesitará restaurarlo en una instancia de Microsoft SQL Server. Estos son los pasos generales para abrir un archivo ".bak" usando SQL Server Management Studio (SSMS):

1. **Inicie SQL Server Management Studio**: abra SSMS en su computadora. Por lo general, puede encontrarlo en el menú Inicio o buscando "SQL Server Management Studio".

2. **Conéctese a una instancia de SQL Server**: en SSMS, conéctese a la instancia de SQL Server donde desea restaurar la base de datos. Necesitará los permisos necesarios para realizar esta operación.

3. **Restaurar base de datos**:

a. En el panel Explorador de objetos en el lado izquierdo, expanda la instancia de SQL Server.

b. Expanda el nodo "Bases de datos".

C. Haga clic derecho en "Bases de datos" y seleccione "Restaurar base de datos".

4. **Especifique origen y destino**:

a. En la página "General" del cuadro de diálogo "Restaurar base de datos", ingrese un nombre para la nueva base de datos en el campo "A la base de datos". Este será el nombre de la base de datos restaurada.

b. En la sección "Fuente", elija "Dispositivo" como tipo de medio de copia de seguridad.

C. Haga clic en el botón "..." junto al campo "Dispositivo" para buscar el archivo ".bak" que desea restaurar.

d. Seleccione el archivo ".bak" que desea abrir y haga clic en "Aceptar".

5. **Opciones de restauración**: revise y configure las opciones de restauración según sea necesario. Puede especificar si desea sobrescribir una base de datos existente, configurar opciones de recuperación y más. Asegúrese de configurar estas opciones de acuerdo con sus requisitos.

6. **Inicie la restauración**: una vez que haya configurado las opciones de restauración, haga clic en el botón "Aceptar" en el cuadro de diálogo "Restaurar base de datos". SQL Server comenzará el proceso de restauración.

7. **Acceder a la base de datos restaurada**: después de una restauración exitosa, puede acceder a la base de datos restaurada en SQL Server Management Studio como cualquier otra base de datos. Puede ejecutar consultas, ver tablas y trabajar con los datos dentro de la base de datos.

## Otros archivos BAK

Aquí hay otros tipos de archivos que usan la extensión de archivo **.bak**.

**Base de datos**
- [BAK - Archivo de copia de seguridad de la base de datos](/es/database/bak/)
- [BAK - ¡Ley Swiftpage! Copia de seguridad de la base de datos](/es/database/bak-act/)

**Juego**
- [BAK - Terraria World o copia de seguridad del jugador](/es/game/bak-terraria/)

**Varios**
- [BAK - Archivo de copia de seguridad](/es/misc/bak-backup/)
- [BAK - Copia de seguridad de marcadores de Chromium](/es/misc/bak-chromium/)
- [BAK - Copia de seguridad de la puntuación final de 2012](/es/misc/bak-finale/)
- [BAK - Copia de seguridad de MobileTrans](/es/misc/bak-mobiletrans/)
- [BAK - Copia de seguridad del proyecto de vídeo VEGAS](/es/misc/bak-vegas/)

**Ajustes**
- [BAK - Copia de seguridad del Lanzador Holo](/es/settings/bak-holo/)

## Referencias
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
