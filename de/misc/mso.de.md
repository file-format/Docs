{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office-Makroreferenzdatei",
  "description":"Erfahren Sie mehr über MSO-Dateien und APIs, die MSO-Dateien erstellen und öffnen können.",
  "linktitle" :"MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Was ist eine MSO-Datei?

Eine MSO-Datei ist ein Datencontainer-Dateiformat, das erstellt wird, wenn eine HTML-Nachricht mit Microsoft Outlook gesendet wird. Dies geschieht hauptsächlich bei Microsoft Office 2000-Anwendungen. In den meisten Fällen wird die E-Mail-Nachricht mit dem Dateinamen **Oledata.mso** angehängt. Der E-Mail-Empfänger kann beim Öffnen einer solchen E-Mail die Datei korrekt anzeigen, auch wenn er nicht dieselbe Software installiert hat. MSO-Dateien beziehen sich auf [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Microsoft MSO-Dateiformat

MSO-Dateien werden im Microsoft Compound Document File Format (MCDF) gespeichert, das auch als Object Linking and Embedding (OLE) oder Component Object Model (COM) strukturiertes Speicher-Compound-Dateiimplementierungs-Binärdateiformat bekannt ist.

### Struktur des MSO-Dateiformats

Die interne Dateiformatstruktur des MSO-Dateiformats ist in den [Strukturen](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) Abschnitt der MCDF-Dokumentation. Die Dateizuordnungstabelle (FAT) verwaltet die Sektorzuordnung und die Sektorketten. Es enthält ein Array von 32-Bit-Sektornummern. Jeder Index im Array stellt eine Sektornummer dar, während sein Wert den nächsten Sektor in der Kette oder einen speziellen Wert darstellt.

## Verweise

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

