{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Obtenga información sobre el formato de archivo MGX de reproducción de expansión de Age of Empires 2 y las API que pueden crear y abrir archivos MGX",
  "title" :"Archivo MII - Formato de archivo de avatar virtual de Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## ¿Qué es un archivo MII?

Un archivo MII es un formato de archivo de avatar virtual que se utiliza para almacenar avatares virtuales en la consola de juegos Nintendo Wii. Estos archivos contienen información como la apariencia, los movimientos y las animaciones del avatar. Se pueden usar en juegos, aplicaciones de redes sociales y otro software en la Wii. Un archivo MII también contiene otras características sobre el avatar, como el género, el color del cabello, el color de la piel, los rasgos faciales y el tipo de ojos.

Puede abrir un archivo MII usando el [Editor de mi avatar](https://rc24.xyz/goodies/mii/).

## Formato de archivo MII

El formato de archivo MII se define en detalle en [Wii Brew](https://wiibrew.org/wiki/Mii_data). Las cadenas en un archivo MII se almacenan en formato Unicode (UTF-16), big-endian.

### Bloque MI

Los datos del archivo MII se almacenan en el Wiimote en dos bloques. Cada bloque tiene una longitud de 750 bytes, con CRC de 2 bytes, lo que hace un total de 752 bytes. Cada bloque comienza con un valor de 4 bytes ('RNCD') que parece ser el número mágico para el formato de archivo MII.

## ¿Cómo crear archivos MII?

Hay algunas formas diferentes de crear avatares para Nintendo Wii:

1. `Usando el canal Mii incorporado en la Wii:` Este canal te permite crear avatares personalizados usando una variedad de herramientas, incluyendo rasgos faciales, forma del cuerpo y ropa. Una vez que haya creado su avatar, puede guardarlo como un archivo Mii y usarlo en juegos y otro software en la Wii.

1. `Usando la aplicación Mii Maker en Nintendo 3DS:` La aplicación Mii Maker te permite crear avatares personalizados usando la pantalla táctil y la cámara en tu Nintendo 3DS. Una vez que hayas creado tu avatar, puedes guardarlo como un archivo Mii y transferirlo a tu Wii a través de una conexión inalámbrica.

1. `Uso de software de terceros:` Algunos desarrolladores han creado software que te permite crear avatares personalizados para la Wii. Este software generalmente está diseñado para usarse en una computadora y puede requerir pasos adicionales para transferir el avatar a tu Wii.

1. `Uso de avatares prefabricados:` Algunos juegos y otro software de la Wii pueden venir con avatares prefabricados que puedes usar.

En todos los casos, necesitas tener una cuenta de Nintendo para crear y guardar tu avatar en la Wii.

## Referencias

* [Editor de mi avatar](https://rc24.xyz/goodies/mii/)
* [Wii Brew](https://wiibrew.org/wiki/Mii_data)

