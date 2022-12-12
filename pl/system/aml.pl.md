{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik AML - plik języka maszynowego ACPI",
  "description":"Poznaj format pliku ACPI AML i interfejsy API, które mogą tworzyć i otwierać pliki AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Czym jest plik AML?

Plik AML to plik systemowy utworzony za pomocą języka Advanced Configuration and Power Interface (ACPI) używanego do konfigurowania właściwości sprzętu. Zawiera niezależny od maszyny kod bajtowy, który jest używany do konfigurowania sprzętu nawet w przypadku prostych operacji, takich jak wyłączanie komputera. Pliki AML mogą zawierać instrukcje w zależności od celu, w jakim mają być instalowane na komputerze. Wdrożenie standardów ACPI pozwala rozszerzyć funkcjonalność zarządzania zasilaniem i rozbudować interfejs do konfiguracji urządzeń płyt głównych, takich jak płyty główne P55.

## Format pliku ACPI AML

Pliki AML są zapisywane jako pliki binarne na dysku z zawartością zapisaną w kodzie bajtowym. Specyfikacje formatu plików standardu ACPI są dostępne na stronie [uefi](https://uefi.org/node/735). Język został zaprojektowany tak, aby oferować stabilność i kompatybilność wsteczną, wymagając mniej ponownego pisania lub przebudowy stosu aplikacji.

## Specyfikacje formatu pliku AML

Plik AML składa się z tabel DSDT i SSDT. Kod bajtowy AML jest odczytywany i analizowany od początku każdej z tych tabel. Daje to informacje o definicjach urządzeń i obiektów w przestrzeni nazw ACPI. Na podstawie tych informacji interpreter AML może wygenerować listę wszystkich urządzeń dostępnych w systemie wraz z ich obsługiwanymi właściwościami i funkcjami.

### Przykładowy kod ASL dla DSDT

Przykład kodu ASL dla DSDT jest następujący.

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

## Bibliografia

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

