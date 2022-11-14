{
  "date" : "2020-08-20",
  "keywords" :[ "file fon", "formato file fon", "cos'è un file fon", "file", "esempio fon", "estensione file fon", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - File della libreria dei caratteri",
  "description":"Scopri il formato di file FON e le API che possono creare e aprire file FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Che cos'è un file FON?

Un file con estensione .fon è una libreria di caratteri Microsoft Windows 3.x che è effettivamente un file eseguibile ma rinominato in .fon. È una raccolta di file [.fnt](/it/font/fnt/) in sé e le applicazioni vi fanno riferimento durante l'accesso ai font di sistema. Ecco perché agisce come un file di risorse. Può essere aperto su sistema operativo Windows utilizzando l'applicazione Microsoft Windows Font View.

## Formato file FON

Un file FON contiene risorse di font e ha il formato di file Resource (.res). Il formato del file .res specifica l'intestazione del file e le specifiche della sezione dati. Un .fnt è anche un file di dati di risorse incluso in un file di risorse. I file FON hanno un formato di file binario e hanno un tipo MIME application/octet-stream.

Le risorse dei caratteri, a differenza di altri tipi di risorse, non vengono aggiunte alle risorse di un'applicazione. Vengono invece aggiunti ai file EXE e rinominati in file .fon, risultando in file di libreria anziché in applicazioni. Più caratteri individuali costituiscono componenti di un gruppo di caratteri in cui ogni gruppo segue una struttura di gruppi di risorse. Le risorse dei caratteri utilizzano queste strutture di gruppi di risorse. L'intestazione del gruppo contiene tutte le informazioni necessarie per accedere a un carattere specifico del gruppo. Una risorsa componente carattere ha il formato seguente.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/it/font/fnt/) file)
```
Un singolo file di risorse .rc può avere dichiarazioni di risorse miste. I gruppi di caratteri possono trovarsi in qualsiasi punto del file di risorse e non devono essere contigui. È necessario che i programmi che creano file .RES aggiungano l'immissione manuale di FONTDIR. Di seguito è riportata la struttura dell'intestazione del gruppo.

```
[Intestazione risorsa normale (tipo = 7)]

WORD Numero di caratteri; // Numero totale nel file .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPunti;
WORD dfVertRes;
WORD dfHorizRes;
PAROLA dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE df Corsivo;
BYTE dfSottolinea;
BYTE dfStrikeOut;
PAROLA dfPeso;
BYTE dfCharSet;
PAROLA dfPixWidth;
PAROLA dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
PAROLA dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfRiservato;
char szDeviceName[];
char szNomeFace[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

