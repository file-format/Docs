{
  "date" : "2019-10-11",
  "keywords" :[ "archivo aba", "formato de archivo aba", "qué es un archivo aba", "archivo", "ejemplo aba", "extensión de archivo aba","extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - Formato de archivo CemText",
  "description":"Obtenga información sobre el formato de archivo ABA y las API que pueden crear y abrir archivos ABA",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## ¿Qué es un archivo ABA?

Un archivo con extensión .aba es un formato de archivo de la Asociación de Banqueros de Australia (ABA) o [Cemtext](https://www.cemtexaba.com/) que utilizan los bancos para transacciones por lotes. Es utilizado por la mayoría de los bancos para el mantenimiento de registros financieros. También conocido como archivo de entrada directa, el formato de archivo ABA ha sido adoptado por la mayoría de los bancos australianos como formato predeterminado para transacciones por lotes. Todavía no ha sido reconocido como formato estándar a pesar de que ha sido utilizado por Bank of Queensland, NAB y Westpac. Los archivos ABA se pueden abrir con cualquier editor de texto como Notepad++.


## Formato de archivo ABA

Un archivo ABA utiliza el formato ASCII para almacenar datos para reenviar o cargar en sistemas bancarios. El formato se ha mantenido simple para facilitar la integración en el propio sistema financiero de las empresas para procesar lotes de transacciones. Por ejemplo, en un sistema de nómina, se puede cargar un lote de transacciones para procesarlas de una sola vez. Las especificaciones del formato de archivo ABA están disponibles como transcripción completa en el sitio web [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) y se pueden consultar como referencia para los desarrolladores. .

Un archivo ABA consta de varias líneas donde cada línea se conoce como un "registro". Hay tres registros principales en un archivo ABA:

* Registro Descriptivo
* Registro de detalles
* Registro total del archivo

### Registro descriptivo

Un 'Registro descriptivo' contiene información como el número de secuencia del carrete, el nombre de la institución financiera del usuario, el archivo de suministro del nombre del uso y otra información.

### Registro detallado

El tipo de 'Registro detallado' incluye información como Banco/Estado/Número de sucursal, Número de cuenta que se abonará/débitará, Indicador, Código de transacción, Monto y otra información.

### Registro total del archivo

El tipo de "Registro total del archivo" incluye el tipo de registro 7, el relleno de formato BSB, el monto total neto del archivo (usuario), el monto total del crédito del archivo (usuario), el monto total del débito del archivo (usuario) y otra información.

### Códigos de transacción

Una lista de códigos de transacción válidos es la siguiente. La mayoría de las veces, el código "53 - Pagar" se usa en los archivos ABA. Estos códigos de transacción abarcan débitos, créditos y retenciones de impuestos.

|Código|Descripción de la transacción|
---|---|
|13|Partidas de débito iniciadas externamente|
|50|Artículos de crédito iniciados externamente con excepción de aquellos que llevan Códigos de Transacción|
|51|Interés de seguridad del gobierno australiano|
|52|Asignación Familiar|
|53|Pago|
|54|Pensión|
|55|Adjudicación|
|56|Dividendo|
|57|Interés de obligaciones/pagarés|

## Ejemplo de archivo ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Referencias

* [ABA de Cemtext](https://www.cemtexaba.com/)

