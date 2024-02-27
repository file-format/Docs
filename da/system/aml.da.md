{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML-fil - ACPI Machine Language File",
  "description":"Lær om ACPI AML filformat og API'er, der kan oprette og åbne AML filer.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml-da",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Hvad er en AML fil?

En AML-fil er en systemfil, der er oprettet med sproget Advanced Configuration and Power Interface (ACPI), der bruges til at konfigurere hardwareegenskaber. Den indeholder maskinuafhængig bytekode, der bruges til at konfigurere hardware, selv til simple operationer som f.eks. at lukke en computer ned. AML-filer kan indeholde instruktioner afhængigt af formålet, som det skal installeres til på maskinen. Implementering af ACPI-standarderne giver dig mulighed for at forbedre strømstyringsfunktionaliteten og en robust grænseflade til konfiguration af bundkortenheder såsom P55 bundkort.

## ACPI AML filformat

AML-filer gemmes som binære filer på disk med indhold skrevet i bytekode. Filformatspecifikationerne for ACPI-standarden er tilgængelige på [uefi](https://uefi.org/). Sproget er designet til at tilbyde stabilitet og bagudkompatibilitet, hvilket kræver færre omskrivninger eller ombygninger af applikationsstakken.

## AML-filformatspecifikationer

En AML-fil består af DSDT- og SSDT-tabeller. AML-bytekoden læses og analyseres fra begyndelsen af hver af disse tabeller. Dette giver information om definitionerne af enheder og objekter i ACPI-navneområdet. Ved hjælp af disse oplysninger kan AML-fortolkeren generere en liste over alle tilgængelige enheder i systemet og deres understøttede egenskaber og funktioner.

### Eksempel ASL-kode for en DSDT

Et eksempel på ASL-kode for en DSDT er som følger.

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

## Referencer

* [ACPI AML](https://wiki.osdev.org/AML)

* [DSDT](https://wiki.osdev.org/DSDT)

* [SSDT](https://wiki.osdev.org/SSDT)


