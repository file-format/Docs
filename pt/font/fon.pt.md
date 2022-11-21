{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo fon", "formato de arquivo fon", "o que é um arquivo fon", "arquivo", "exemplo fon", "extensão do arquivo fon", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Arquivo de biblioteca de fontes",
  "description":"Saiba mais sobre o formato de arquivo FON e APIs que podem criar e abrir arquivos FON.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## O que é um arquivo FON?

Um arquivo com extensão .fon é uma biblioteca de fontes do Microsoft Windows 3.x que, na verdade, é um arquivo executável, mas renomeado para .fon. É uma coleção de arquivos [.fnt](/pt/font/fnt/) em si e os aplicativos fazem referência a ele enquanto acessam a fonte do sistema. É por isso que ele atua como um arquivo de recurso. Ele pode ser aberto no sistema operacional Windows usando o aplicativo Microsoft Windows Font View.

## Formato de arquivo FON

Um arquivo FON contém recursos de fonte e tem o formato de arquivo Resource (.res). O formato de arquivo .res especifica o cabeçalho do arquivo, bem como as especificações da seção de dados. Um .fnt também é um arquivo de dados de recurso incluído em um arquivo de recurso. Os arquivos FON têm formato de arquivo binário e têm tipo MIME application/octet-stream.

Os recursos de fonte, ao contrário de outros tipos de recursos, não são adicionados aos recursos de um aplicativo. Em vez disso, eles são adicionados aos arquivos EXE e renomeados para arquivos .fon, resultando em arquivos de biblioteca em vez de aplicativos. Várias fontes individuais constituem componentes de um grupo de fontes em que cada grupo segue uma estrutura de grupo de recursos. Os recursos de fonte usam essas estruturas de grupo de recursos. O cabeçalho do grupo contém todas as informações necessárias para acessar uma fonte específica do grupo. Um recurso de componente de fonte tem o formato a seguir.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/pt/font/fnt/) file)
```
Um único arquivo de recurso .rc pode ter declarações de recursos mistas. Os grupos de fontes podem estar em qualquer lugar no arquivo de recursos e não precisam ser contíguos. É obrigatório para os programas que criam arquivos .RES adicionar entrada manual de FONDIR. A seguir está a estrutura do cabeçalho do grupo.

```
[Cabeçalho de recurso normal (tipo = 7)]

WORD NumberOfFonts; // Número total no arquivo .RES
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fonteOrdinal;
struct FontDirEntry {
WORD dfVersão;
DWORD dfSize;
char dfCopyright[60];
PALAVRA dfType;
WORD dfPontos;
WORD dfVertRes;
WORD dfHorizRes;
PALAVRA dfAscensão;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItálico;
BYTE dfUnderline;
BYTE dfStrikeOut;
PALAVRA dfPeso;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixAltura;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDispositivo;
DWORD dfFace;
DWORD dfReservado;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

