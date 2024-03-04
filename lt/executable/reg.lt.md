{
  "date": "2021-08-02",
  "keywords": [
"reg failą",
"reg failo formatas",
"kas yra reg failas",
"failą",
"reg pavyzdys",
"reg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie REG failo formatą ir API, kurios gali kurti ir atidaryti REG failus.",
  "title": "REG – „Windows“ registro failas",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-ltg"
}
},
  "lastmod": "2021-08-02"
}

## Kas yra REG failas?

REG failas yra tiesiog tekstinis failas su plėtiniu .reg. Šie failai paprastai sukuriami eksportuojant tipinius raktus iš registro. Šie failai taip pat gali būti naudojami kaip atsarginė registro kopija (ypač šis veiksmas yra svarbus prieš atliekant pakeitimus!). Matote, kad kai kurie padarė juos prieinamus kaip atsisiunčiamus failus tose pačiose svetainėse, kuriose parodyta, kaip įsilaužti į registrą. REG failas yra naudingas atliekant rankinius registro pakeitimus ir eksportuojant tuos pakeitimus. Tiesiog šiek tiek išvalykite failą ir bendrinkite jį su kitais.

## REG failo formatas

REG failo formatas buvo skirtas eksportuoti ir importuoti Windows registro dalis naudojant INI sintaksę. Windows registras yra reliacinė arba hierarchinė duomenų bazė, kurioje saugomi žemo lygio Microsoft Windows operacinės sistemos ir kitų Windows registrą naudojančių programų parametrai. Galima sakyti, kad registrą arba Windows registrą sudaro informacija, parinktys, nustatymai ir kitos programos ir aparatinės įrangos, įdiegtos visose Microsoft Windows operacinių sistemų versijose, reikšmės.

### REG failo sintaksė
Štai keletas pagrindinių REG failo sintaksės elementų:
– **RegistryEditorVersion**: pvz., Windows Registry Editor Version 5.00, skirta Windows 2000, Windows XP ir Windows Server 2003.
- **Tuščia eilutė**: nurodo naujo registro kelio pradžią.
– **RegistryPathx**: dalinio rakto, kuriame yra pirmoji importuojama reikšmė, kelias.
– **DataItemNamex**: duomenų elemento, kurį norite importuoti, pavadinimas.
- **DataTypex**: registro reikšmės duomenų tipas.

Raktai saugomi .reg failuose naudojant šią sintaksę:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Galite redaguoti numatytąją rakto reikšmę naudodami @, o ne vertės pavadinimą:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Pavyzdys

Čia yra REG failo pavyzdys
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

## Nuorodos

* [Windows registras – Vikipedija](https://en.wikipedia.org/wiki/Windows_Registry)

* [Kaip pridėti, modifikuoti arba ištrinti dalinius registro raktus ir reikšmes naudojant .reg failą](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- Registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


