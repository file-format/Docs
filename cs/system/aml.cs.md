{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor AML - ACPI Machine Language File",
  "description":"Další informace o formátu souborů ACPI AML a rozhraních API, která mohou vytvářet a otevírat soubory AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Co je soubor AML?

Soubor AML je systémový soubor vytvořený pomocí jazyka ACPI (Advanced Configuration and Power Interface), který se používá pro konfiguraci vlastností hardwaru. Obsahuje strojově nezávislý bajtový kód, který se používá ke konfiguraci hardwaru i pro jednoduché operace, jako je vypnutí počítače. Soubory AML mohou obsahovat pokyny v závislosti na účelu, pro který má být na počítači nainstalován. Implementace standardů ACPI vám umožní zlepšit funkce správy napájení a robustní rozhraní pro konfiguraci zařízení na základní desce, jako jsou základní desky P55.

## Formát souboru ACPI AML

Soubory AML se ukládají jako binární soubory na disk s obsahem zapsaným v bajtovém kódu. Specifikace formátu souboru standardu ACPI jsou k dispozici na [uefi] (https://uefi.org/node/735). Jazyk byl navržen tak, aby nabízel stabilitu a zpětnou kompatibilitu a vyžadoval méně přepisování nebo přestavování aplikačního zásobníku.

## Specifikace formátu souboru AML

Soubor AML se skládá z tabulek DSDT a SSDT. Bajtový kód AML se čte a analyzuje od začátku každé z těchto tabulek. To poskytuje informace o definicích zařízení a objektů v oboru názvů ACPI. Pomocí těchto informací může interpret AML vygenerovat seznam všech zařízení dostupných v systému a jejich podporované vlastnosti a funkce.

### Příklad kódu ASL pro DSDT

Příklad kódu ASL pro DSDT je následující.

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

## Reference

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

