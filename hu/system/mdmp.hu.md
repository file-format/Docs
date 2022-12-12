{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP fájl - Windows Minidump fájlformátum",
  "description":"További információ az MDMP fájlformátumról és az MDMP-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Mi az MDMP fájl?

Az MDMP-fájl egy Microsoft Windows rendszeren futó alkalmazás memóriakiírása, amely akkor jön létre, amikor az alkalmazás rendellenesen bezárul vagy összeomlik. Információkat és adatkiíratásokat tartalmaz, amelyek segítségével meg lehet keresni az összeomlás okát. Az MDMP fájlok bármilyen platformon, például Java, C++, .NET és mások által létrehozott alkalmazásokban alkalmazhatók. Az MDMP mellett

Az MDMP fájlokat megnyitni képes alkalmazások közé tartozik a Microsoft Visual Studio Debugger.

## MDMP fájlformátum

Az MDMP-fájlok bináris fájlokként kerülnek a lemezre, és megnyithatók a Microsoft Visual Studio hibakeresővel. A következő információkat tartalmazza, amelyek segítenek azonosítani a baleset okát.

* A Stop üzenet részletei, paraméterei és egyéb adatok
* A betöltött illesztőprogramok listája
* Processzor kontextus (PRCB) azon processzorhoz, amely leállt
* Folyamatinformációk és kernelkörnyezet (EPROCESS) a leállt folyamathoz
* A leállt szál feldolgozási információi és kernelkörnyezete (ETHREAD).
* Kernel módú hívásverem a leállt szálhoz

Ez az információ segít kideríteni, mi történt, kijavítani a problémát, és megelőzni annak újbóli előfordulását.

### Minidump elemzése

A Windows memóriaképfájl létrehozásához lapozófájlra van szükség a rendszerindító köteten. A lapozófájl a rendszerindító köteten jön létre, és legalább 2 megabájt (MB) méretűnek kell lennie. A kiíratási fájl akkor jön létre, amikor egy alkalmazás összeomlik. Második probléma esetén egy második kis memóriakiíratási fájl jön létre, miközben az előző megmarad. A dump fájl neve különálló, hogy elkerülje a felülírást.

A Windows a %SystemRoot%\Minidump mappában tárolja az összes memóriakiíratási fájl listáját. Az MDMP-fájlokat úgy elemezheti, hogy futtatja őket a Visual Studio Debugger alkalmazásban az alábbi lépések szerint.

## Hogyan nyithatok meg MDMP fájlt a Visual Studióban?

A következő lépésekkel nyithat meg egy MDMP-fájlt a Visual Studio alkalmazásban.

* A Visual Studio Fájl menüjében válassza a Megnyitás | Összeomlás kiírása .
* Keresse meg a megnyitni kívánt dump fájlt.
* Válassza a Megnyitás lehetőséget.

## Referencia

* [A Windows által létrehozott kis memóriaképfájl olvasása összeomlás esetén](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -fájl)

