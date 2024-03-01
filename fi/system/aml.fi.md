{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AML-tiedosto - ACPI-konekielitiedosto",
  "description":"Opi ACPI AML -tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata AML-tiedostoja.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml-fi",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Mikä on AML-tiedosto?

AML-tiedosto on järjestelmätiedosto, joka on luotu Advanced Configuration and Power Interface (ACPI) -kielellä, jota käytetään laitteiston ominaisuuksien määrittämiseen. Se sisältää koneesta riippumattoman tavukoodin, jota käytetään laitteiston määrittämiseen jopa yksinkertaisia toimintoja, kuten tietokoneen sammuttamista, varten. AML-tiedostot voivat sisältää ohjeita riippuen siitä, mihin tarkoitukseen ne asennetaan koneelle. ACPI-standardien käyttöönoton avulla voit parantaa virranhallintatoimintoja ja vankan käyttöliittymän emolevylaitteiden, kuten P55-emolevyjen, määrittämiseen.

## ACPI AML -tiedostomuoto

AML-tiedostot tallennetaan binääritiedostoina levylle, jonka sisältö on kirjoitettu tavukoodilla. ACPI-standardin tiedostomuotomääritykset ovat saatavilla osoitteessa {{HYPERLINKKI}}. Kieli on suunniteltu tarjoamaan vakautta ja taaksepäin yhteensopivuutta, mikä vaatii vähemmän sovelluspinon uudelleenkirjoittamista tai -muodostuksia.

## AML-tiedostomuodon tekniset tiedot

AML-tiedosto koostuu DSDT- ja SSDT-taulukoista. AML-tavukoodi luetaan ja jäsennetään jokaisen taulukon alusta alkaen. Tämä antaa tietoja laitteiden ja objektien määritelmistä ACPI-nimiavaruudessa. Näiden tietojen avulla AML-tulkki voi luoda luettelon kaikista järjestelmässä olevista laitteista ja niiden tuetuista ominaisuuksista ja toiminnoista.

### Esimerkki ASL-koodista DSDT:lle

Esimerkki ASL-koodista DSDT:lle on seuraava.

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

## Viitteet

* [ACPI AML](https://wiki.osdev.org/AML)

* [DSDT](https://wiki.osdev.org/DSDT)

* [SSDT](https://wiki.osdev.org/SSDT)


