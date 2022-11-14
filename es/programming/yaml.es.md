{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","qué es un archivo yaml","cómo abrir un archivo yaml", "extensión", "archivo", "archivo yaml","formato de archivo yaml", "extensión .yaml" , "yaml vs json", "ejemplo de archivo YAML", "ejemplo de archivo docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Obtenga información sobre el formato de archivo YAML y las API que pueden crear y abrir un archivo YAML.",
  "title" :"Formato de archivo YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## ¿Qué es un archivo YAML? ##

**Archivo YAML** consta de un lenguaje YAML (YAML no es un lenguaje de marcado) que es un lenguaje de serialización de datos basado en Unicode; se usa para archivos de configuración, mensajería de Internet, persistencia de objetos, etc. YAML usa la extensión .yaml para sus archivos. Su sintaxis es independiente de un lenguaje de programación específico. Básicamente, YAML está diseñado para la interacción humana y para funcionar bien con los lenguajes de programación modernos. La compatibilidad con la serialización de estructuras de datos nativas arbitrarias aumentó la legibilidad de los archivos YAML, pero complicó un poco el proceso de análisis y generación de archivos.

## Breve historia ##

YAML se propuso por primera vez en 2001 y fue desarrollado por Clark Evans, Ingy döt Net y Oren Ben-Kiki. Primero se dijo que YAML significaba "Otro lenguaje de marcado más" para indicar su propósito como lenguaje de marcado. Más tarde se reutilizó como "YAML Aint Markup Language" para indicar su propósito como orientado a datos.


## Formato de archivo YAML ##

El archivo YAML consta de los siguientes tipos de datos

- **Escaleras**: Los escalares son valores como cadenas, enteros, booleanos, etc.
- **Secuencias**: Las secuencias son listas en las que cada elemento comienza con un guión (-). Las listas también se pueden anidar.
- **Asignaciones**: la asignación brinda la capacidad de listar claves con valores.

### Sintaxis ###

- **Espacio en blanco**: la sangría de espacio en blanco se utiliza para indicar el anidamiento y la estructura general.

```yaml
nombre: Juan Smith
contacto:
domicilio: 1012355532
oficina: 5002586256
Dirección:
calle: |
123 Callejón Tornado
suite 16
ciudad: East Centerville
estado: Kansas
```

- **Comentarios**: Los comentarios se escriben comenzando con el símbolo "#".

```yaml
# Este es un comentario YAML
```

- **Listas**: el guión (-) se usa para indicar miembros de la lista con cada miembro en una línea separada. Los miembros de la lista también se pueden encerrar entre corchetes ([...]) con los miembros separados por comas (,).

```yaml
  - A
  - B
  - C
```

```yaml
[A B C]
```

- **Matriz asociativa**: una matriz asociativa está rodeada por corchetes ({...}). Las claves y los valores están separados por dos puntos (:) y cada par está separado por una coma (,).

```yaml
  {name: John Smith, age: 20}
```

- **Cadenas**: la cadena se puede escribir con o sin comillas dobles (") o comillas simples (').

```yaml
Cadena de muestra
"Cadena de muestra"
'Cadena de muestra'
```

- **Contenido de bloque escalar**: el contenido escalar se puede escribir en notación de bloque usando lo siguiente:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

```yaml
datos: |
YAML
(YAML no es lenguaje de marcas)
es un lenguaje de serialización de datos
```

```yaml
datos: ?
YAML (YAML no es lenguaje de marcas)
es un lenguaje de serialización de datos
```

- **Documentos múltiples**: los documentos múltiples están separados por tres guiones (---) en una sola secuencia. Los guiones indican el inicio del documento. Los guiones también se utilizan para separar las directivas del contenido del documento. El final del documento se indica con tres puntos (...).

```yaml
  ---
Documento 1
  ---
Documento 2
...
```

- **Tipo**: Para especificar el tipo de valor se utilizan dobles signos de exclamación (!!).

```yaml
a: !!flotador 123
b: !!str 123
```

- **Etiqueta**: para asignar una etiqueta a una nota, se usa un ampersand (&) y para hacer referencia a ese nodo, se usa un asterisco (*).

```yaml
nombre: Juan Smith
facturar a: &id01
calle: |
123 Callejón Tornado
suite 16
ciudad: East Centerville
estado: Kansas

enviar a: *id01
```

- **Directivas**: los documentos YAML pueden estar precedidos por directivas en una transmisión. Las directivas comienzan con un signo de porcentaje (%) seguido del nombre y luego los parámetros separados por espacios.

```yaml
%YAML 1.2
  ---
Contenido del documento
```
## Ejemplo de archivo YAML
Aquí puede ver un **ejemplo de archivo docker yaml** a continuación:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML frente a JSON
Básicamente, tanto JSON como YAML se desarrollan para proporcionar un formato de intercambio de datos legible por humanos. El YAML se realiza como un superconjunto de formato JSON. Significa que podemos analizar JSON usando un analizador YAML. Aunque la implementación práctica de esta teoría es un poco complicada. Por lo tanto, a continuación se dan algunas diferencias básicas entre YAML y JSON:

|YAML| JSON|
---|---|
|Proceso complejo y lento de análisis de datos serializados |Análisis rápido y fácil de datos serializados JSON con su diseño más simple|
|Menos apoyo comunitario| Mayor apoyo y popularidad de la comunidad|
|Comentarios de apoyo| No admite comentarios|
|Capacidad de usar la referencia de otros objetos de datos| Imposible serializar estructuras complejas con referencias a objetos|
|La jerarquía se indica mediante caracteres de doble espacio. No se permiten caracteres de tabulación|Los objetos y matrices se indican entre llaves y corchetes.|
|Las comillas de cadena son opcionales, pero admite comillas simples y dobles.|Las cadenas deben estar entre comillas dobles.|
|El nodo raíz puede ser cualquiera de los tipos de datos válidos|El nodo raíz debe ser una matriz o un objeto.|


## Referencias ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

