{
  "date": "2021-08-02",
  "keywords": [
"reg fails",
"reg faila formāts",
"kas ir reg fails",
"failu",
"reg piemērs",
"reg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par REG faila formātu un API, kas var izveidot un atvērt REG failus.",
  "title": "REG — Windows reģistra fails",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-lvg"
}
},
  "lastmod": "2021-08-02"
}

## Kas ir REG fails?

REG fails ir vienkārši teksta fails ar paplašinājumu .reg. Šie faili parasti tiek izveidoti, eksportējot tipiskās atslēgas no reģistra. Šos failus var izmantot arī kā reģistra dublējumu (īpaši šī darbība ir svarīga pirms izmaiņu veikšanas!). Varat redzēt, ka daži tos padarīja pieejamus kā lejupielādējamus failus tajās pašās vietnēs, kurās parādīts, kā veikt reģistra uzlaušanu. REG fails ir noderīgs, veicot manuālas izmaiņas reģistrā un eksportējot šīs izmaiņas. Vienkārši nedaudz iztīriet failu un pēc tam kopīgojiet to ar citiem.

## REG faila formāts

REG faila formāts bija paredzēts Windows reģistra daļu eksportēšanai un importēšanai, izmantojot uz INI balstītu sintaksi. Windows reģistrs ir relāciju vai hierarhiska datu bāze, kurā tiek saglabāti zema līmeņa iestatījumi operētājsistēmai Microsoft Windows un citām lietojumprogrammām, kas izmanto Windows reģistru. Mēs varam teikt, ka reģistrs vai Windows reģistrs sastāv no informācijas, opcijām, iestatījumiem un citām vērtībām programmām un aparatūrai, kas instalēta visās Microsoft Windows operētājsistēmu versijās.

### REG faila sintakse
Šeit ir daži galvenie elementi kā daļa no REG faila sintakses:
- **RegistryEditorVersion**: piemēram, Windows Registry Editor Version 5.00 operētājsistēmai Windows 2000, Windows XP un Windows Server 2003.
- **Tukša rindiņa**: norāda jauna reģistra ceļa sākumu.
- **RegistryPathx**: apakšatslēgas ceļš, kurā ir pirmā importējamā vērtība.
- **DataItemNamex**: tā datu vienuma nosaukums, kuru vēlaties importēt.
- **DataTypex**: reģistra vērtības datu tips.

Atslēgas tiek saglabātas .reg failos, izmantojot šādu sintaksi:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Varat rediģēt atslēgas noklusējuma vērtību, izmantojot @, nevis Vērtības nosaukumu.
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Piemērs

Šeit ir REG faila piemērs
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

## Atsauces

* [Windows reģistrs — Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)

* [Kā pievienot, modificēt vai dzēst reģistra apakšatslēgas un vērtības, izmantojot .reg failu](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


