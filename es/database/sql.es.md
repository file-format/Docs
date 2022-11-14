{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "extensión", "archivo", "formato de archivo", "Tipo de archivo de base de datos", "Formato de archivo de base de datos", "Archivos de base de datos" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Obtenga más información sobre el formato de archivo SQL y las API que pueden crear y abrir archivos SQL",
  "title" :"Formato de archivo SQL: un archivo de datos de lenguaje de consulta estructurado",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## ¿Qué es un archivo SQL?

Un archivo con extensión .sql es un archivo de lenguaje de consulta estructurado (SQL) que contiene código para trabajar con bases de datos relacionales. Se utiliza para escribir sentencias SQL para operaciones CRUD (Crear, Leer, Actualizar y Eliminar) en bases de datos. Los archivos SQL son comunes cuando se trabaja con bases de datos de escritorio y basadas en la web. Existen varias alternativas a SQL, como Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL y varias otras. Los editores de consultas de Microsoft SQL Server, MySQL y otros editores de texto sin formato, como el Bloc de notas en el sistema operativo Windows, pueden abrir archivos SQL.

## Breve historia

* Desarrollado e introducido por Donal D. Chamberlin y Raymond F. Boyce en IBM a principios de la década de 1970
* Se utiliza para almacenar y recuperar datos del sistema de gestión de base de datos cuasi-relacional original de IBM, System R
* Comenzó a utilizarse en productos comerciales basados en su prototipo System R, incluidos System/38, SQL/DS y DB2, que estuvieron disponibles comercialmente en 1979, 1981 y 1983, respectivamente.
* Adoptado oficialmente por los grupos de estándares ANSI e ISO como estándar "Database Language SQL" para sistemas de administración de bases de datos relacionales (RDBMS) en 1986

## Formato de archivo SQL

Los archivos SQL están en formato de texto sin formato y pueden constar de varios elementos de lenguaje. Se pueden agregar varias declaraciones a un solo archivo SQL si su ejecución es posible sin depender unas de otras. Estos comandos SQL pueden ser ejecutados por editores de consultas para realizar operaciones CRUD.

### Elementos del lenguaje SQL

Los elementos del lenguaje SQL se enumeran a continuación.

|Elemento|Descripción|
---|---|
|Cláusulas| Componentes constitutivos de sentencias y consultas.|
|Expresiones| Puede producir valores escalares o tablas que constan de columnas y filas de datos|
|Predicados| Especifique las condiciones que se pueden evaluar a la lógica de tres valores SQL (3VL) (verdadero/falso/desconocido) o valores de verdad booleanos y se utilizan para limitar los efectos de las declaraciones y consultas, o para cambiar el flujo del programa.|
|Consultas| Recupere los datos en función de criterios específicos. Este es un elemento importante de SQL.|
|Declaraciones| Puede tener un efecto persistente en esquemas y datos, o puede controlar transacciones, flujo de programas, conexiones, sesiones o diagnósticos.|

### Ejemplo SQL
La siguiente instrucción SQL crea una tabla denominada **DATOS**, seguida de comandos `INSERT` adicionales para insertar registros en esta tabla.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Referencias ##

* [SQL de Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Sintaxis SQL](https://en.wikipedia.org/wiki/SQL_syntax)

