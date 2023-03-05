{
  "date" : "2021-08-02",
  "keywords" :[ "reg-Datei", "reg-Dateiformat", "was ist eine reg-Datei", "Datei", "reg-Beispiel", "reg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das REG-Dateiformat und APIs, die REG-Dateien erstellen und öffnen können.",
  "title" :"REG - Windows-Registrierungsdatei",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Was ist eine REG-Datei?
Eine REG-Datei ist einfach eine Textdatei mit der Erweiterung .reg. Diese Dateien werden normalerweise erstellt, indem typische Schlüssel aus der Registrierung exportiert werden. Diese Dateien können auch als Backup der Registrierung verwendet werden (besonders dieser Schritt ist wichtig, bevor Sie Änderungen vornehmen!). Sie können sehen, dass einige sie als herunterladbare Dateien auf denselben Websites zur Verfügung gestellt haben, die Ihnen zeigen, wie Sie einen Registrierungs-Hack durchführen. Eine REG-Datei ist nützlich, um manuelle Änderungen an der Registrierung vorzunehmen und diese Änderungen zu exportieren. Räumen Sie die Datei einfach ein wenig auf und teilen Sie sie dann mit anderen.

## REG-Dateiformat
Das REG-Dateiformat wurde zum Exportieren und Importieren von Teilen der Windows-Registrierung mithilfe einer INI-basierten Syntax entwickelt. Die Windows-Registrierung ist eine relationale oder hierarchische Datenbank, die die Low-Level-Einstellungen für das Microsoft Windows-Betriebssystem und andere Anwendungen enthält, die die Windows-Registrierung verwenden. Alternativ können wir sagen, dass die Registrierung oder Windows-Registrierung aus Informationen, Optionen, Einstellungen und anderen Werten für Programme und Hardware besteht, die auf allen Versionen von Microsoft Windows-Betriebssystemen installiert sind.
### Syntax der REG-Datei
Hier sind einige Schlüsselelemente als Teil einer REG-Dateisyntax:
- **RegistryEditorVersion**: zB "Windows Registry Editor Version 5.00" für Windows 2000, Windows XP und Windows Server 2003.
- **Leerzeile**: Kennzeichnet den Beginn eines neuen Registrierungspfades.
- **RegistryPathx**: Der Pfad des Unterschlüssels, der den ersten Wert enthält, den Sie importieren.
- **DataItemNamex**: Der Name des Datenelements, das Sie importieren möchten.
- **DataTypex**: Der Datentyp für den Registrierungswert.

Schlüssel werden in REG-Dateien mit der folgenden Syntax gespeichert:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Sie können den Standardwert eines Schlüssels bearbeiten, indem Sie "@" anstelle von "Wertname" verwenden:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Beispiel
Hier ist ein Beispiel für eine REG-Datei
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

## Verweise

* [Windows-Registrierung – von Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Hinzufügen, Ändern oder Löschen von Registrierungsunterschlüsseln und -werten mithilfe einer .reg-Datei](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete-registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)
