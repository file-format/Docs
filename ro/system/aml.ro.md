{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier AML - Fișier ACPI Machine Language",
  "description":"Aflați despre formatul de fișier ACPI AML și despre API-urile care pot crea și deschide fișiere AML.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Ce este un fișier AML?

Un fișier AML este un fișier de sistem creat cu limbajul Advanced Configuration and Power Interface (ACPI) utilizat pentru configurarea proprietăților hardware. Conține un cod octet independent de mașină, care este utilizat pentru a configura hardware-ul chiar și pentru operațiuni simple, cum ar fi închiderea unui computer. Fișierele AML pot conține instrucțiuni în funcție de scopul pentru care urmează să fie instalate pe mașină. Implementarea standardelor ACPI vă permite să îmbunătățiți funcționalitatea de gestionare a energiei și o interfață robustă pentru configurarea dispozitivelor plăcii de bază, cum ar fi plăcile de bază P55.

## Format de fișier ACPI AML

Fișierele AML sunt salvate ca fișiere binare pe disc cu conținut scris în cod octet. Specificațiile de format de fișier ale standardului ACPI sunt disponibile pe [uefi](https://uefi.org/). Limbajul a fost conceput pentru a oferi stabilitate și compatibilitate inversă, necesitând mai puține rescrieri sau reconstruiri ale stivei de aplicații.

## Specificații privind formatul fișierului AML

Un fișier AML constă din tabele DSDT și SSDT. Codul octet AML este citit și analizat de la începutul fiecăruia dintre aceste tabele. Acesta oferă informații despre definițiile dispozitivelor și obiectelor din spațiul de nume ACPI. Folosind aceste informații, interpretul AML poate genera o listă cu toate dispozitivele disponibile în sistem și proprietățile și funcțiile lor acceptate.

### Exemplu de cod ASL pentru un DSDT

Un exemplu de cod ASL pentru un DSDT este următorul.

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

## Referințe

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

