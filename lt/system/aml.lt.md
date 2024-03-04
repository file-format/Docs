{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML failas – ACPI mašinos kalbos failas",
  "description":"Sužinokite apie ACPI AML failo formatą ir API, kurios gali kurti ir atidaryti AML failus.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml-lt",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Kas yra AML failas?

AML failas yra sistemos failas, sukurtas naudojant išplėstinės konfigūracijos ir maitinimo sąsajos (ACPI) kalbą, naudojamą aparatūros ypatybėms konfigūruoti. Jame yra nuo mašinos nepriklausomas baitų kodas, naudojamas aparatūrai konfigūruoti net atliekant paprastas operacijas, pvz., išjungti kompiuterį. AML failuose gali būti nurodymų, atsižvelgiant į tai, kokiu tikslu jis turi būti įdiegtas įrenginyje. Įdiegę ACPI standartus galite pagerinti energijos valdymo funkcionalumą ir tvirtą sąsają, skirtą pagrindinės plokštės įrenginiams, pvz., P55 pagrindinėms plokštėms, konfigūruoti.

## ACPI AML failo formatas

AML failai išsaugomi kaip dvejetainiai failai į diską, kurio turinys įrašytas baitų kodu. ACPI standarto failo formato specifikacijos pasiekiamos [uefi](https://uefi.org/). Kalba sukurta taip, kad būtų užtikrintas stabilumas ir atgalinis suderinamumas, todėl reikia mažiau perrašyti arba kurti programų paketą.

## AML failo formato specifikacijos

AML failą sudaro DSDT ir SSDT lentelės. AML baito kodas skaitomas ir analizuojamas nuo kiekvienos iš šių lentelių pradžios. Tai suteikia informacijos apie įrenginių ir objektų apibrėžimus ACPI vardų erdvėje. Naudodamas šią informaciją, AML vertėjas gali sugeneruoti visų sistemoje galimų įrenginių sąrašą ir jų palaikomas savybes bei funkcijas.

### DSDT ASL kodo pavyzdys

DSDT ASL kodo pavyzdys yra toks.

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

## Nuorodos

* [ACPI AML](https://wiki.osdev.org/AML)

* [DSDT](https://wiki.osdev.org/DSDT)

* [SSDT](https://wiki.osdev.org/SSDT)


