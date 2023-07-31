{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO – Microsoft Office Macro Reference File",
  "description":"További információ az MSO-fájlokról és az MSO-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Mi az MSO fájl?

Az MSO-fájl egy adattároló fájlformátum, amely akkor jön létre, amikor HTML-üzenetet küld a Microsoft Outlook használatával. Ez leginkább a Microsoft Office 2000 alkalmazásokkal történik. Az esetek többségében az e-mail üzenet **Oledata.mso** fájlnévvel van csatolva. Az e-mail címzettje, amikor megnyit egy ilyen e-mailt, akkor is helyesen tekintheti meg a fájlt, ha nem ugyanaz a szoftver van telepítve. Az MSO-fájlok a [Microsoft Compound Document File Format (MCDF)]-re hivatkoznak (https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Microsoft MSO fájlformátum

Az MSO-fájlok mentése Microsoft összetett dokumentumfájl-formátumban (MCDF) történik, amelyet Object Linking and Embedding (OLE) vagy Component Object Model (COM) strukturált tárolási összetett fájlmegvalósítási bináris fájlformátumként is ismernek.

### MSO fájlformátum szerkezete

Az MSO-fájlformátum belső fájlformátum-struktúrája jól meghatározott a [Struktúrák](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) szakasza az MCDF dokumentációjában. A File Allocation Table (FAT) kezeli a szektorok elosztását és a szektorláncokat. 32 bites szektorszámok tömbjét tartalmazza. A tömb minden indexe egy szektorszámot jelöl, míg az értéke a lánc következő szektorát vagy egy speciális értéket képvisel.

## Hivatkozások

* [COM Structured Storage](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

