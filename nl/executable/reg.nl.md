{
  "date" : "2021-08-02",
  "keywords" :[ "reg file", "reg file format", "wat is een reg file", "file", "reg example", "reg file extension","extension", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over REG-bestandsindelingen en API's die REG-bestanden kunnen maken en openen.",
  "title" :"REG - Windows-registerbestand",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Wat is een REG-bestand?
Een REG-bestand is gewoon een tekstbestand met de extensie .reg. Deze bestanden worden meestal gemaakt door typische sleutels uit het register te exporteren. Deze bestanden kunnen ook worden gebruikt als back-up van het register (met name deze stap is belangrijk voordat u wijzigingen aanbrengt!). U kunt zien dat sommigen ze beschikbaar hebben gemaakt als downloadbare bestanden op dezelfde sites die u laten zien hoe u een registerhack uitvoert. Een REG-bestand is handig om handmatige wijzigingen in het register aan te brengen en die wijzigingen te exporteren. Ruim het bestand een beetje op en deel het vervolgens met anderen.

## REG-bestandsindeling
De REG-bestandsindeling is ontworpen voor het exporteren en importeren van delen van het Windows-register met behulp van een op INI gebaseerde syntaxis. Het Windows-register is een relationele of hiërarchische database die de lage instellingen voor het Microsoft Windows-besturingssysteem en andere toepassingen die het Windows-register gebruiken, bewaart. Als alternatief kunnen we zeggen dat het register of Windows-register bestaat uit informatie, opties, instellingen en andere waarden voor programma's en hardware die op alle versies van Microsoft Windows-besturingssystemen zijn geïnstalleerd.
### Syntaxis van REG-bestand
Hier zijn enkele belangrijke elementen als onderdeel van een REG-bestandssyntaxis:
- **RegistryEditorVersion**: bijv. "Windows Registry Editor versie 5.00" voor Windows 2000, Windows XP en Windows Server 2003.
- **Blanke regel**: identificeert het begin van een nieuw registerpad.
- **RegistryPathx**: het pad van de subsleutel die de eerste waarde bevat die u importeert.
- **DataItemNamex**: de naam van het gegevensitem dat u wilt importeren.
- **DataTypex**: het gegevenstype voor de registerwaarde.

Sleutels worden opgeslagen in .reg-bestanden met behulp van de volgende syntaxis:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
U kunt de standaardwaarde van een sleutel bewerken door "@" te gebruiken in plaats van "Waardenaam":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Voorbeeld
Hier is een voorbeeld van een REG-bestand:
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

## Referenties

* [Windows-register- door Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Subsleutels en waarden in het register toevoegen, wijzigen of verwijderen met behulp van een .reg-bestand](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
