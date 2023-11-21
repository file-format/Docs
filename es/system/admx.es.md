{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo ADMX: formato de archivo de plantilla administrativa de política de grupo",
  "description":"Obtenga más información sobre el formato de archivo ADMX y cómo abrir archivos ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## ¿Qué es un archivo ADMX?

Un archivo ADMX es un archivo de configuración de políticas utilizado por el software de políticas de grupo de Microsoft Windows que administra un grupo de computadoras en un grupo. Es un archivo de plantilla administrativa basado en XML y se introdujo con Windows Vista Service Pack 1. Los archivos ADMX contienen ajustes de configuración para cuentas de usuario, configuraciones de sistema operativo y aplicaciones. Los archivos ADMX se utilizan para almacenar e implementar las configuraciones para la gestión centralizada de muchos sistemas informáticos.

Puede crear o editar archivos ADMX utilizando cualquier editor de texto compatible con XML o el editor de objetos de política de grupo de Microsoft.

## Formato de archivo ADMX - Más información

Los archivos ADMX se almacenan en el formato de archivo universal [XML](/es/web/xml/) que es legible por humanos. Es un formato de archivo multilingüe y permite a los administradores de sistemas de diferentes idiomas trabajar con los mismos archivos ADMX. Los archivos ADMX reemplazaron el antiguo formato de archivo [ADM](/es/system/adm/), que es un formato de archivo de texto con formato Unicode. Los archivos ADMX especifican las claves de registro que se cambian cuando se cambia una determinada configuración de política de grupo.

### ¿Qué puedo hacer con el archivo ADMX?

Los archivos ADMX definen qué acciones se permitirán a las computadoras de los usuarios que forman parte de un grupo. La política de grupo impone las reglas establecidas en combinación con el software Active Directory. Los archivos ADMX se administran desde el almacén central del sistema operativo Windows, que es una ubicación central en el dominio.

Un archivo ADMX implementado en un entorno de trabajo puede permitir a los administradores implementar políticas como:

* Controlar el uso de internet.
* Descarga de ciertos tipos de archivos.
* Uso de dispositivos extraíbles en los sistemas.

## Referencias

* [Archivos de plantilla administrativa - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestión de archivos de plantilla administrativa](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

