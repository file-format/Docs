{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo CR3 - arquivo de imagem Canon Raw 3",
  "description":"Saiba mais sobre o formato de arquivo CR3 e APIs que podem criar e abrir arquivos CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## O que é um arquivo CR3?

Um arquivo CR3 é um formato de arquivo de imagem Canon RAW criado por câmeras digitais Canon selecionadas. Foi introduzido pela Canon para substituir o formato de arquivo CR2 e é usado por alguns dos dispositivos digitais da Canon. Os arquivos CR3 armazenam os dados de imagem sem perdas originais não processados capturados pela câmera. O uso dessas imagens brutas fornece imagens de alta qualidade e permite muito espaço para edição aos fotógrafos. Além dos dados da imagem principal, os arquivos CR3 também armazenam informações de metadados sobre a imagem.

## Formato de arquivo CR3

Os arquivos CR3 são armazenados em disco como arquivo binário no formato de arquivo de mídia ISO Base (ISO/IEC 14496-12) e também inclui [tags Canon] (https://exiftool.org/TagNames/Canon.html#uuid) personalizadas. Ele também inclui o [codec Canon 'crx'](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) que é uma mistura de JPEG-LS (Rice-Golomb + RLE codificação) e JPEG-2000 (LeGall 5/3 DWT + quantificação).

## Tags personalizadas CR3

Os arquivos CR3 contêm tags personalizadas para diferentes propósitos. Algumas dessas tags são as seguintes.

|ID da etiqueta| Nome da etiqueta| Gravável |Valores / Notas|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP Tags|
|'CMT1' |IFD0| - |--> EXIF Tags|
|'CMT2' |ExifIFD| - |--> EXIF Tags|
|'CMT3' |MakerNoteCanon| - |--> Etiquetas Canon|
|'CMT4' |GPSInfo| - |--> Etiquetas GPS|
|'CNCV' |Versão do Compressor| não| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tags|
|'THMB' |Imagem de miniatura| não| |

## Referências

* [Formato de arquivo CR2](http://lclevy.free.fr/cr2/)
* [Tags Canon](https://exiftool.org/TagNames/Canon.html#uuid)

