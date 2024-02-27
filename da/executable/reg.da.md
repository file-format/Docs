{
  "date": "2021-08-02",
  "keywords": [
"reg fil",
"reg filformat",
"hvad er en reg fil",
"fil",
"reg eksempel",
"reg filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om REG-filformat og API'er, der kan oprette og åbne REG-filer.",
  "title": "REG - Windows Registry File",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-dag"
}
},
  "lastmod": "2021-08-02"
}

## Hvad er REG fil?

En REG-fil er simpelthen en tekstfil med filtypenavnet .reg. Disse filer oprettes normalt ved at eksportere typiske nøgler fra registreringsdatabasen. Disse filer kan også bruges som backup af registreringsdatabasen (Specielt dette trin er vigtigt, før du foretager ændringer!). Du kan se, at nogle gjorde dem tilgængelige som downloadbare filer på de samme websteder, der viser dig, hvordan du udfører et registreringshack. En REG-fil er nyttig til at foretage manuelle ændringer i registreringsdatabasen og eksportere disse ændringer. Bare ryd lidt op i filen og del den derefter med andre.

## REG filformat

REG-filformatet blev designet til at eksportere og importere dele af Windows-registreringsdatabasen ved hjælp af en INI-baseret syntaks. Windows-registreringsdatabasen er en relationel eller hierarkisk database, der holder lavniveauindstillingerne for Microsoft Windows-operativsystemet og andre applikationer, der bruger Windows-registreringsdatabasen. Alternativt kan vi sige, at registreringsdatabasen eller Windows-registreringsdatabasen består af information, muligheder, indstillinger og andre værdier for programmer og hardware installeret på alle versioner af Microsoft Windows-operativsystemer.

### Syntaks for REG-fil
Her er nogle nøgleelementer som en del af en REG-filsyntaks:
- **RegistryEditorVersion**: F.eks. Windows Registry Editor Version 5.00 til Windows 2000, Windows XP og Windows Server 2003.
- **Blank linje**: Identificerer starten på en ny registreringssti.
- **RegistryPathx**: Stien til den undernøgle, der indeholder den første værdi, du importerer.
- **DataItemNamex**: Navnet på det dataelement, du vil importere.
- **DataTypex**: Datatypen for registreringsdatabasen værdi.

Nøgler gemmes i .reg-filer ved hjælp af følgende syntaks:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Du kan redigere standardværdien for en nøgle ved at bruge @ i stedet for Værdinavn:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Eksempel

Her er et eksempel på REG-fil
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

## Referencer

* [Windows Registry- af Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)

* [Sådan tilføjer, ændrer eller sletter du registreringsundernøgler og -værdier ved hjælp af en .reg-fil](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- registreringsdatabasenøgler-og-værdier-ved-bruge-en-reg-fil-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


