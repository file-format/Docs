{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP fájl - Windows Heap Dump File Format",
  "description":"További információ a HDMP fájlformátumról és az API-król, amelyek HDMP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Mi az a HDMP fájl?

A HDMP fájl egy tömörítetlen memóriakép, amikor egy alkalmazás vagy program hiba miatt összeomlik. Csak a Windows XP/Vista hozta létre, és kiíratást tartalmaz az alkalmazás állapotáról, amikor az összeomlott. Mivel nincsenek tömörítve, a HDMP fájlok több helyet foglalnak el a lemezen, mint a jelentéskészítés céljából tömörített Minidump [MDMP](/hu/system/mdmp/) fájlok.

A HDMP-fájlok **megnyitására** vagy elemzésére használható alkalmazások közé tartozik a Microsoft Visual Studio a Windows rendszerhez készült hibakereső eszközökkel.

## HDMP fájlformátum

A HDMP-fájlok bináris fájlokként kerülnek a lemezre, és nem nyújtanak semmilyen előnyt, ha megfelelő alkalmazások nélkül nyitják meg őket. Ezek a hiba bekövetkeztekor rögzített releváns rendszeradatokat tartalmazzák.

### A HDMP és MDMP fájlformátumok közötti különbség

A HDMP tömörítetlen memóriaképfájlok. Ezzel szemben az MDMP mini dump fájlok, amelyeket tömörítenek a fájlméret csökkentése érdekében, és elküldik a Microsoftnak a probléma jelentésére.

## Hivatkozási szám

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

