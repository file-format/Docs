{
"fecha": "2023-06-08",
  "keywords": [
"archivo vmx",
"¿Qué es un archivo vmx?",
"ejemplo de archivo vmx",
"cómo abrir un archivo vmx",
"¿Qué contiene el archivo vmx?",
"¿Cuál es el formato del archivo vmx?",
"archivo",
"extensión de archivo vmx",
"extensión"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de archivo VMX: archivo de configuración de máquina virtual VMware",
  "description":"Obtenga más información sobre el formato VMX y las API que pueden crear y abrir archivos VMX.",
"enlacetítulo": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent": "configuración"
}
},
"lastmod": "2023-06-08"
}

## ¿Qué es un archivo VMX?

Un archivo VMX, también conocido como archivo de configuración de máquina virtual, es un archivo de texto sin formato utilizado por el software de virtualización VMware para definir los ajustes y la configuración de la máquina virtual (VM). Los archivos VMX contienen información como la configuración del hardware de la VM, asignaciones de discos virtuales, configuraciones de red y otros parámetros.

## Ejemplo de archivo VMX

A continuación se muestra un ejemplo de cómo se vería el archivo VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## ¿Qué contiene el archivo VMX?

Un archivo VMX contiene varios ajustes de configuración para la máquina virtual (VM). Estas son algunas de las configuraciones más comunes en el archivo VMX:

- `.encoding:` Especifica la codificación de caracteres utilizada en el archivo.
- `config.version:` Indica la versión del formato de archivo VMX.
- `virtualHW.version:` Especifica la versión del hardware virtual para la VM.
- `guestOS:` Especifica el sistema operativo invitado instalado en la VM.
- `memSize:` Define la cantidad de memoria asignada a la VM.
- `displayName:` Establece el nombre para mostrar o la etiqueta de la VM.
- `powerType:` Define el comportamiento de energía para diferentes operaciones (apagar, encender, restablecer, suspender).
- `floppyX:` Ajustes de configuración relacionados con unidades de disquete, como presencia y asignaciones de archivos.
- `numvcpus:` Especifica el número de CPU virtuales asignadas a la VM.
- `scsiX:` Ajustes de configuración para controladores SCSI y sus discos virtuales asociados.
- `ethernetX:` Ajustes de configuración para adaptadores de red, incluido el tipo de dispositivo virtual, el nombre de la red y el tipo de dirección.
- `ideX:` Ajustes de configuración para controladores IDE y sus discos virtuales asociados.
- `usbX:` Ajustes de configuración para dispositivos USB, como presencia y detalles de conexión.
- `sonido:` Ajustes de configuración para el adaptador de sonido virtual.
- `tools.syncTime:` Indica si la sincronización horaria con el sistema host está habilitada.
- `uuid.bios:` Especifica el UUID del BIOS de la VM.
- `uuid.location:` Especifica el UUID de ubicación de la VM.

## ¿Cómo abrir el archivo VMX?

No se recomienda abrir un archivo VMX manualmente. Cuando ejecuta una máquina virtual usando VMware Fusion, el software carga automáticamente la información del archivo VMX.

Sin embargo, si desea editar manualmente el archivo VMX, puede hacerlo utilizando cualquier editor de texto, por ejemplo, el Bloc de notas (Windows) o TextEdit (Mac).

## ¿Cuál es el formato del archivo VMX?

Un archivo VMX es un archivo de texto sin formato con un formato específico. El formato sigue una estructura de par clave-valor donde cada línea representa una opción de configuración independiente.

El formato general del archivo VMX es el siguiente:

```
key1 = value1
key2 = value2
key3 = value3
```

Cada línea consta de una clave seguida de un signo igual (=) y el valor correspondiente. La clave representa una configuración específica y el valor representa el valor asignado a esa configuración.

Por ejemplo, `memSize = "8192"` en el archivo VMX especifica que el límite de memoria de la máquina virtual es 8192 MB de RAM.

El formato del archivo VMX también puede incluir comentarios, indicados por un signo de almohadilla (#) al principio de la línea, que el software VMware ignora al analizar el archivo. Los comentarios se utilizan a menudo para proporcionar información adicional o explicaciones para configuraciones específicas.

## Referencias
* [Archivo VMX de muestra](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




