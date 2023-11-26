{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo ADM - Formato de archivo de plantilla administrativa",
  "description":"Obtenga información sobre el formato de archivo ADM y cómo abrir archivos ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## ¿Qué es un archivo ADM?

Un archivo ADM es un archivo de plantilla utilizado por el software de políticas de grupo de Microsoft para especificar la ubicación de la configuración de políticas basadas en el registro en el archivo de registro. Lo utilizan los administradores del sistema para definir la política para administrar un grupo de computadoras que forman parte del grupo. Esta información pasa a formar parte de los objetos de política de grupo (GPO) que se crean para la gestión del grupo.

Puede abrir archivos ADM utilizando el Editor de objetos de política de grupo de Microsoft.

## Formato de archivo ADM - Más información

Los archivos ADM se almacenan como archivos de texto con formato Unicode. Se utilizaron principalmente para describir la ubicación de las configuraciones de políticas basadas en el registro en el registro de Windows Vista y Windows 7.

Los archivos ADM ya no son compatibles y han sido reemplazados por los archivos [ADMX](/es/system/admx/). GPA ignora los siguientes archivos ADM predeterminados en computadoras que ejecutan Microsoft Windows Vista Service Pack 1 o posterior.

* sistema.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Referencias

* [Archivos de plantilla administrativa - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestión de archivos de plantilla administrativa](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

