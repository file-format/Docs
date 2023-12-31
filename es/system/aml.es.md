{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo AML - Archivo de lenguaje de máquina ACPI",
  "description":"Obtenga más información sobre el formato de archivo ACPI AML y las API que pueden crear y abrir archivos AML",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## ¿Qué es un archivo AML?

Un archivo AML es un archivo de sistema creado con el lenguaje de configuración avanzada e interfaz de energía (ACPI) que se utiliza para configurar las propiedades del hardware. Contiene un código de bytes independiente de la máquina que se usa para configurar el hardware incluso para operaciones simples como apagar una computadora. Los archivos AML pueden contener instrucciones según el propósito para el que se instalen en la máquina. La implementación de los estándares ACPI le permite mejorar la funcionalidad de administración de energía y una interfaz robusta para configurar dispositivos de placa base como las placas base P55.

## Formato de archivo ACPI AML

Los archivos AML se guardan como archivos binarios en el disco con contenidos escritos en código de bytes. Las especificaciones de formato de archivo del estándar ACPI están disponibles en [uefi](https://uefi.org/). El lenguaje ha sido diseñado para ofrecer estabilidad y compatibilidad con versiones anteriores, lo que requiere menos reescrituras o reconstrucciones de la pila de aplicaciones.

## Especificaciones del formato de archivo AML

Un archivo AML se compone de tablas DSDT y SSDT. El código de bytes AML se lee y analiza desde el principio de cada una de estas tablas. Esto brinda información sobre las definiciones de dispositivos y objetos en el espacio de nombres ACPI. Con esta información, el intérprete de AML puede generar una lista de todos los dispositivos disponibles en el sistema y sus propiedades y funciones admitidas.

### Ejemplo de código ASL para un DSDT

Un ejemplo de código ASL para un DSDT es el siguiente.

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## Referencias

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

