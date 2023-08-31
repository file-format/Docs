{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML fájl - ACPI gépi nyelvi fájl",
  "description":"További információ az ACPI AML fájlformátumról és az API-król, amelyek AML fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Mi az AML fájl?

Az AML-fájl a hardvertulajdonságok konfigurálásához használt Advanced Configuration and Power Interface (ACPI) nyelvvel létrehozott rendszerfájl. Gépfüggetlen bájtkódot tartalmaz, amelyet a hardver konfigurálására használnak még olyan egyszerű műveletekhez is, mint például a számítógép leállítása. Az AML-fájlok utasításokat tartalmazhatnak attól függően, hogy milyen célból kívánják telepíteni őket a gépre. Az ACPI szabványok megvalósítása lehetővé teszi az energiagazdálkodási funkciók javítását, valamint egy robusztus interfészt az alaplapi eszközök, például a P55 alaplapok konfigurálásához.

## ACPI AML fájlformátum

Az AML-fájlok bináris fájlokként kerülnek mentésre bájtkóddal írt tartalommal rendelkező lemezre. Az ACPI szabvány fájlformátum-specifikációi elérhetők az [uefi](https://uefi.org/node/735) webhelyen. A nyelvet úgy tervezték, hogy stabilitást és visszamenőleges kompatibilitást kínáljon, kevesebb újraírást vagy újraépítést igényelve az alkalmazásveremben.

## Az AML fájlformátum specifikációi

Az AML fájl DSDT és SSDT táblákat tartalmaz. Az AML bájtkód beolvasása és elemzése az egyes táblák elejétől fogva történik. Ez információkat ad az eszközök és objektumok definícióiról az ACPI névtérben. Ezen információk felhasználásával az AML értelmező létrehozhat egy listát a rendszerben elérhető összes eszközről, valamint azok támogatott tulajdonságairól és funkcióiról.

### Példa ASL-kódra DSDT-hez

Egy példa a DSDT ASL-kódjára a következő.

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

## Hivatkozások

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

