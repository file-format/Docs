{
"fecha": "2023-08-03",
  "keywords": [
"usr",
"archivo usr",
"¿Qué es un archivo usr?",
"cómo abrir un archivo usr",
"archivo",
"extensión de archivo usr",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo USR - Archivo de datos GPS de Lowrance",
  "description":"Obtenga más información sobre el formato USR y las API que pueden crear y abrir archivos USR.",
"linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
"parent": "gis"
}
},
"lastmod": "2023-08-03"
}

## ¿Qué es un archivo USR?

La extensión de archivo ".usr" también está relacionada con los dispositivos GPS de Lowrance. En particular, se utiliza para almacenar datos de GPS en un formato conocido como "formato de datos de usuario" (formato USR) que utilizan los dispositivos GPS de Lowrance.

Cuando utiliza una unidad GPS Lowrance, puede guardar sus puntos de referencia, tracks y rutas como archivos ".usr". Estos archivos suelen contener información como latitud, longitud, altitud, marca de tiempo y otros datos relacionados con sus actividades de GPS.

A continuación se muestran algunos usos comunes de los archivos .usr con dispositivos GPS Lowrance:

- **Puntos de referencia:** Los puntos de referencia son ubicaciones específicas marcadas en el GPS, como puntos de referencia, lugares de pesca favoritos o puntos de interés. Puede guardar estas ubicaciones como archivos .usr y pueden importarse, exportarse o compartirse con otros usuarios de GPS de Lowrance.

- **Pistas:** Las pistas representan la ruta registrada de sus movimientos GPS. Puede guardar sus registros de recorrido como archivos .usr, lo que le permitirá revisar y analizar sus rutas más tarde o compartirlas con otras personas.

- **Rutas:** Las rutas son rutas predefinidas que puedes crear y guardar en tu dispositivo GPS. Estas rutas también se pueden guardar como archivos .usr para usarlas o compartirlas en el futuro.

Para administrar archivos .usr en su dispositivo GPS Lowrance, normalmente utiliza software como "Insight Planner" o "Lowrance GPS Utility" de Lowrance para importar, exportar y manipular sus datos GPS.

## Formato de archivo USR - Más información

En los dispositivos GPS Lowrance iFinder, los archivos .usr se crean y guardan en la tarjeta de memoria MultiMediaCard (MMC) insertada en el dispositivo. Estos archivos contienen datos del usuario, como waypoints, tracks y rutas.

Para transferir los archivos .usr desde MMC a una computadora, puede seguir estos pasos:

- **Retire la MMC:** Retire con cuidado la tarjeta MultiMediaCard (MMC) del dispositivo GPS Lowrance iFinder.

- **Inserte MMC en la computadora:** Utilice un lector de tarjetas MMC apropiado para insertar la tarjeta de memoria en la ranura del lector de tarjetas de su computadora.

- **Localizar archivos .usr:** Una vez que su computadora reconozca el MMC, debería poder acceder a los archivos almacenados en él. Busque los archivos .usr, que contienen sus datos de GPS.

- **Conversión con GPSBabel:** Para convertir los archivos .usr a otro formato GPS, puede utilizar GPSBabel, que es una herramienta gratuita y de código abierto para trabajar con varios formatos de archivos GPS. GPSBabel admite una amplia gama de formatos de entrada y salida, lo que le permite convertir los archivos .usr a formatos compatibles con otro software o dispositivo GPS.

Puede descargar GPSBabel desde el sitio web oficial (http://www.gpsbabel.org/) e instalarlo en su computadora. Una vez instalado, puede utilizar la interfaz de línea de comandos del software o la interfaz gráfica de usuario (si está disponible) para realizar la conversión.

Por ejemplo, si desea convertir archivos .usr al formato GPX, puede usar un comando como:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

El comando anterior le indica a GPSBabel que lea el archivo de entrada "input.usr" en formato Lowrance USR y escriba el archivo de salida "output.gpx" en formato GPX.

- **Importar/Usar archivos convertidos:** Después de la conversión, tendrá sus datos de GPS en el nuevo formato (por ejemplo, GPX), que podrá usar con otro software o dispositivos GPS que admitan ese formato.

## ¿Cómo abrir el archivo USR?

Los programas que abren o hacen referencia a archivos USR incluyen

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Referencias
* [Electrónica Lowrance](https://en.wikipedia.org/wiki/Lowrance_Electronics)

