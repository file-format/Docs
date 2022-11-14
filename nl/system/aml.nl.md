{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML-bestand - ACPI-machinetaalbestand",
  "description":"Meer informatie over ACPI AML-bestandsindeling en API's die AML-bestanden kunnen maken en openen.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Wat is een AML-bestand?

Een AML-bestand is een systeembestand dat is gemaakt met de Advanced Configuration and Power Interface (ACPI)-taal die wordt gebruikt voor het configureren van hardware-eigenschappen. Het bevat machine-onafhankelijke bytecode die wordt gebruikt om hardware te configureren, zelfs voor eenvoudige bewerkingen zoals het afsluiten van een computer. AML-bestanden kunnen instructies bevatten, afhankelijk van het doel waarvoor het op de machine moet worden geïnstalleerd. Door de implementatie van de ACPI-standaarden kunt u de energiebeheerfunctionaliteit en een robuuste interface voor het configureren van moederbordapparaten zoals de P55-moederborden verbeteren.

## ACPI AML-bestandsindeling

AML-bestanden worden opgeslagen als binaire bestanden op schijf met inhoud geschreven in bytecode. De specificaties van het bestandsformaat van de ACPI-standaard zijn beschikbaar op [uefi](https://uefi.org/node/735). De taal is ontworpen om stabiliteit en achterwaartse compatibiliteit te bieden, waardoor minder herschrijven of herbouwen van de applicatiestack nodig is.

## Specificaties AML-bestandsindeling

Een AML-bestand bestaat uit DSDT- en SSDT-tabellen. De AML-bytecode wordt gelezen en geparseerd vanaf het begin van elk van deze tabellen. Dit geeft informatie over de definities van apparaten en objecten in de ACPI-naamruimte. Met behulp van deze informatie kan de AML-interpreter een lijst genereren van alle apparaten die beschikbaar zijn in het systeem, en hun ondersteunde eigenschappen en functies.

### Voorbeeld ASL-code voor een DSDT

Een voorbeeld van ASL-code voor een DSDT is als volgt.

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

## Referenties

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

