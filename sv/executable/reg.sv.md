{
  "date" : "2021-08-02",
  "keywords" :[ "reg fil", "reg filformat", "vad är en reg fil", "fil", "reg exempel", "reg filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om REG-filformat och API:er som kan skapa och öppna REG-filer.",
  "title" :"REG - Windows-registerfil",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Vad är REG fil?
En REG-fil är helt enkelt en textfil med filtillägget .reg. Dessa filer skapas vanligtvis genom att exportera typiska nycklar från registret. Dessa filer kan också användas som en säkerhetskopia av registret (särskilt detta steg är viktigt innan du gör ändringar!). Du kan se att vissa gjorde dem tillgängliga som nedladdningsbara filer på samma webbplatser som visar hur du utför ett registerhack. En REG-fil är användbar för att göra manuella ändringar i registret och exportera dessa ändringar. Rensa bara upp filen lite och dela den sedan med andra.

## REG filformat
REG-filformatet utformades för att exportera och importera delar av Windows-registret med en INI-baserad syntax. Windows-registret är en relations- eller hierarkisk databas som håller lågnivåinställningarna för Microsoft Windows-operativsystemet och andra applikationer som använder Windows-registret. Alternativt kan vi säga att registret eller Windows-registret består av information, alternativ, inställningar och andra värden för program och hårdvara installerade på alla versioner av Microsoft Windows-operativsystem.
### Syntax för REG-fil
Här är några nyckelelement som en del av en REG-filsyntax:
- **RegistryEditorVersion**: T.ex. "Windows Registry Editor Version 5.00" för Windows 2000, Windows XP och Windows Server 2003.
- **Tom rad**: Identifierar början på en ny registersökväg.
- **RegistryPathx**: Sökvägen till undernyckeln som innehåller det första värdet du importerar.
- **DataItemNamex**: Namnet på dataobjektet som du vill importera.
- **DataTypex**: Datatypen för registervärdet.

Nycklar lagras i .reg-filer med följande syntax:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Du kan redigera standardvärdet för en nyckel genom att använda "@" istället för "Värdenamn":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Exempel
Här är ett exempel på REG-fil
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

## Referenser

* [Windows Registry- av Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Hur man lägger till, ändrar eller tar bort registerundernycklar och värden genom att använda en .reg-fil](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- register-undernycklar-och-värden-genom-användning-en-reg-fil-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


