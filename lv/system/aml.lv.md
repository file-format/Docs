{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML fails — ACPI mašīnas valodas fails",
  "description":"Uzziniet par ACPI AML faila formātu un API, kas var izveidot un atvērt AML failus.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml-lv",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Kas ir AML fails?

AML fails ir sistēmas fails, kas izveidots ar Advanced Configuration and Power Interface (ACPI) valodu, ko izmanto aparatūras rekvizītu konfigurēšanai. Tajā ir no mašīnas neatkarīgs baita kods, ko izmanto, lai konfigurētu aparatūru pat vienkāršām darbībām, piemēram, datora izslēgšanai. AML failos var būt instrukcijas atkarībā no mērķa, kādam tie ir jāinstalē iekārtā. ACPI standartu ieviešana ļauj uzlabot enerģijas pārvaldības funkcionalitāti un spēcīgu saskarni mātesplates ierīču, piemēram, P55 mātesplates, konfigurēšanai.

## ACPI AML faila formāts

AML faili tiek saglabāti kā bināri faili diskā ar saturu, kas ierakstīts baitu kodā. ACPI standarta faila formāta specifikācijas ir pieejamas vietnē [uefi](https://uefi.org/). Valoda ir izstrādāta tā, lai nodrošinātu stabilitāti un atpakaļejošu saderību, kas prasa mazāk pārrakstīšanas vai lietojumprogrammu steka pārveidošanas.

## AML faila formāta specifikācijas

AML fails sastāv no DSDT un SSDT tabulām. AML baita kods tiek lasīts un parsēts no katras šīs tabulas sākuma. Tas sniedz informāciju par ierīču un objektu definīcijām ACPI nosaukumvietā. Izmantojot šo informāciju, AML tulks var izveidot visu sistēmā pieejamo ierīču sarakstu, kā arī to atbalstītās īpašības un funkcijas.

### DSDT ASL koda piemērs

ASL koda piemērs DSDT ir šāds.

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

## Atsauces

* [ACPI AML](https://wiki.osdev.org/AML)

* [DSDT](https://wiki.osdev.org/DSDT)

* [SSDT](https://wiki.osdev.org/SSDT)


