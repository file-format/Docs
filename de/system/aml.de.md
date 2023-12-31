{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML-Datei - ACPI-Maschinensprachendatei",
  "description":"Erfahren Sie mehr über das ACPI AML-Dateiformat und APIs, die AML-Dateien erstellen und öffnen können.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
"Bezeichner": "System-AML",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Was ist eine AML-Datei?

Eine AML-Datei ist eine Systemdatei, die mit der Sprache Advanced Configuration and Power Interface (ACPI) erstellt wurde, die zum Konfigurieren von Hardwareeigenschaften verwendet wird. Es enthält maschinenunabhängigen Bytecode, der verwendet wird, um Hardware selbst für einfache Vorgänge wie das Herunterfahren eines Computers zu konfigurieren. AML-Dateien können je nach Zweck, für den sie auf dem Computer installiert werden sollen, Anweisungen enthalten. Durch die Implementierung der ACPI-Standards können Sie die Energieverwaltungsfunktionalität und eine robuste Schnittstelle zum Konfigurieren von Motherboard-Geräten wie den P55-Motherboards verbessern.

## ACPI AML-Dateiformat

AML-Dateien werden als Binärdateien auf Disc gespeichert, deren Inhalt in Bytecode geschrieben ist. Die Dateiformatspezifikationen des ACPI-Standards sind auf [uefi](https://uefi.org/) verfügbar. Die Sprache wurde entwickelt, um Stabilität und Abwärtskompatibilität zu bieten, wodurch weniger Umschreibungen oder Neuerstellungen des Anwendungsstapels erforderlich sind.

## AML-Dateiformatspezifikationen

Eine AML-Datei besteht aus DSDT- und SSDT-Tabellen. Der AML-Bytecode wird vom Anfang jeder dieser Tabellen gelesen und geparst. Dies gibt Auskunft über die Definitionen von Geräten und Objekten im ACPI-Namespace. Anhand dieser Informationen kann der AML-Interpreter eine Liste aller im System verfügbaren Geräte und ihrer unterstützten Eigenschaften und Funktionen erstellen.

### Beispiel-ASL-Code für eine DSDT

Ein Beispiel eines ASL-Codes für eine DSDT ist wie folgt.

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

## Verweise

* [ACPI-AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

