{
  "date": "2021-08-02",
  "keywords": [
"reg tiedosto",
"reg tiedostomuoto",
"mikä on reg-tiedosto",
"tiedosto",
"reg esimerkki",
"reg tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi REG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata REG-tiedostoja.",
  "title": "REG - Windowsin rekisteritiedosto",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-fig"
}
},
  "lastmod": "2021-08-02"
}

## Mikä on REG-tiedosto?

REG-tiedosto on yksinkertaisesti tekstitiedosto, jonka tunniste on .reg. Nämä tiedostot luodaan yleensä viemällä tyypillisiä avaimia rekisteristä. Näitä tiedostoja voidaan käyttää myös rekisterin varmuuskopiona (etenkin tämä vaihe on tärkeä ennen muutosten tekemistä!). Voit nähdä, että jotkut asettivat ne saataville ladattavina tiedostoina samoilla sivustoilla, jotka osoittavat, kuinka voit suorittaa rekisterihakkeroinnin. REG-tiedosto on hyödyllinen manuaalisten muutosten tekemisessä rekisteriin ja muutosten viemiseen. Puhdista tiedosto hieman ja jaa se sitten muiden kanssa.

## REG-tiedostomuoto

REG-tiedostomuoto on suunniteltu Windows-rekisterin osien vientiin ja tuontiin käyttämällä INI-pohjaista syntaksia. Windowsin rekisteri on relaatio- tai hierarkkinen tietokanta, joka säilyttää matalan tason asetukset Microsoft Windows -käyttöjärjestelmälle ja muille Windows-rekisteriä käyttäville sovelluksille. Vaihtoehtoisesti voidaan sanoa, että rekisteri tai Windows-rekisteri koostuu tiedoista, vaihtoehdoista, asetuksista ja muista arvoista ohjelmille ja laitteistoille, jotka on asennettu kaikkiin Microsoft Windows -käyttöjärjestelmien versioihin.

### REG-tiedoston syntaksi
Tässä on joitain avainelementtejä osana REG-tiedoston syntaksia:
- **RegistryEditorVersion**: esim. Windows Registry Editor Version 5.00 Windows 2000:lle, Windows XP:lle ja Windows Server 2003:lle.
- **Tyhjä rivi**: Ilmaisee uuden rekisteripolun alun.
- **RegistryPathx**: Ensimmäisen tuotavan arvon sisältävän aliavaimen polku.
- **DataItemNamex**: Sen tietokohteen nimi, jonka haluat tuoda.
- **DataTypex**: Rekisteriarvon tietotyyppi.

Avaimet tallennetaan .reg-tiedostoihin käyttämällä seuraavaa syntaksia:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Voit muokata avaimen oletusarvoa käyttämällä @-merkkiä Arvon nimen sijaan:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Esimerkki

Tässä on esimerkki REG-tiedostosta
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Viitteet

* [Windows Registry - Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)

* [Rekisterin aliavaimien ja arvojen lisääminen, muokkaaminen tai poistaminen .reg-tiedoston avulla](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


