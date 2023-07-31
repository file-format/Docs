{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo CMS: archivo de perfil de servicio de Connection Manager",
  "description":"Obtenga más información sobre el archivo CMS y las API que pueden crear y abrir archivos CMS",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## ¿Qué es un archivo CMS?

Un archivo CMS es un archivo de datos que contiene información de perfil utilizada por Microsoft Windows Connection Manager. Permite a los usuarios remotos conectarse a una red utilizando esta información de perfil. La información almacenada dentro de un archivo CMS incluye datos sobre el sistema operativo del usuario y los permisos que se utilizan para establecer una conexión entre un usuario remoto y la red. Los administradores de CMS utilizan el kit de administrador de Connection Manager (CMAK) para generar archivos CMS.

## Formato de archivo CMS: más información

Los archivos CMS no se encuentran comúnmente en las máquinas de los usuarios. Dado que estos se usan específicamente para permitir que los usuarios remotos accedan a una red, los encontrará en computadoras que se usan para conectarse a la red de una empresa o alguna oficina de construcción específica. En la mayoría de los casos, se usa para conectarse a una red organizacional como una red privada virtual (VPN) que está dedicada solo a una empresa. Como administrador de red, configurará el acceso a dicha red con Connection Manager para permitirle acceder a la red de la empresa desde una ubicación remota.

### ¿Qué es insdie CMS?

Un archivo de perfil de CMS se crea mediante Connection Manager y se empaqueta con otros archivos de configuración antes de proporcionarlo al usuario remoto. Estos archivos adicionales pueden incluir un archivo CMP y un archivo INF que se empaquetan junto con un archivo [EXE](/es/executable/exe/). Este paquete completo se proporciona al usuario remoto para conectarse a la red.

## Referencias

* [Comprender y configurar Windows Connection Manager](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

