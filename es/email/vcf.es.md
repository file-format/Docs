{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Archivo de contacto virtual",
  "description":"Obtenga información sobre el formato de archivo VCF y las API que pueden crear y abrir archivos VCF",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ¿Qué es un archivo VCF?

VCF (formato de tarjeta virtual) o vCard es un formato de archivo digital para almacenar información de contacto. El formato se usa ampliamente para el intercambio de datos entre aplicaciones populares de intercambio de información. La mayoría de los sistemas operativos, como Windows y MacOS, vienen con aplicaciones predeterminadas para crear y abrir estos archivos. Un solo archivo VCF puede contener información de contacto para uno o varios contactos. Un archivo VCF generalmente contiene información como el nombre del contacto, la dirección, el número de teléfono, el correo electrónico, la fecha de nacimiento, las fotografías y el audio, además de otros campos. Al ser compatible con clientes y servicios de correo electrónico, no hay pérdida de datos durante la transferencia de contactos mediante el uso del formato vCard. El tipo de medio para el formato de archivo VCF es texto/vcard.

## Formato de archivo VCF

Los archivos VCF son textuales por naturaleza y son legibles por humanos. Estos se pueden abrir en editores de texto como Notepad en Microsoft Windows y TextEdit en MacOS. Sin embargo, si hay una imagen en el archivo, no se mostrará en el editor de texto.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) brinda soporte para abrir archivos VCF y convertirlos a otros formatos, como el popular formato [MSG](/es/email/msg/). Formato de archivo VCF mejorado con el tiempo desde la versión 2.1 a la 4.0 agregando información detallada al formato de archivo. El formato también se usa para exportar contactos telefónicos y luego importar en otro dispositivo.

{{< figure src="../VCF.png" alt="Formato de archivo VCF" >}}

### Ejemplo de VCF 2.1

A continuación se muestra un ejemplo de la versión 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### Ejemplo de VCF 3.0

A continuación se muestra un ejemplo de la versión 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### Ejemplo de VCF 4.0

A continuación se muestra un ejemplo de la versión 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Referencias

* [VCF - Por Wikipedia](https://en.wikipedia.org/wiki/VCard)

