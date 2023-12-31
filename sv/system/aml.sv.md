{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML File - ACPI Machine Language File",
  "description":"Läs mer om ACPI AML-filformat och API:er som kan skapa och öppna AML-filer.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Vad är AML fil?

En AML-fil är en systemfil som skapats med språket Advanced Configuration and Power Interface (ACPI) som används för att konfigurera hårdvaruegenskaper. Den innehåller maskinoberoende bytekod som används för att konfigurera hårdvara även för enkla operationer som att stänga av en dator. AML-filer kan innehålla instruktioner beroende på vilket syfte de ska installeras för på maskinen. Implementering av ACPI-standarderna låter dig förbättra strömhanteringsfunktionaliteten och ett robust gränssnitt för att konfigurera moderkortsenheter som P55-moderkort.

## ACPI AML filformat

AML-filer sparas som binära filer på skiva med innehåll skrivet i bytekod. Filformatspecifikationerna för ACPI-standarden finns på [uefi](https://uefi.org/). Språket har utformats för att erbjuda stabilitet och bakåtkompatibilitet, vilket kräver mindre omskrivningar eller ombyggnader av applikationsstacken.

## AML-filformatspecifikationer

En AML-fil består av DSDT- och SSDT-tabeller. AML-bytekoden läses och tolkas från början av var och en av dessa tabeller. Detta ger information om definitionerna av enheter och objekt i ACPI-namnområdet. Med hjälp av denna information kan AML-tolken generera en lista över alla enheter som är tillgängliga i systemet, och deras egenskaper och funktioner som stöds.

### Exempel ASL-kod för en DSDT

Ett exempel på ASL-kod för en DSDT är följande.

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

## Referenser

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

