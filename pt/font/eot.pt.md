{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo eot", "formato de arquivo eot", "o que é um arquivo eot", "arquivo", "exemplo eot", "extensão de arquivo eot", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Formato de arquivo de fonte TrueType",
  "description":"Saiba mais sobre o formato de arquivo EOT e APIs para criar e abrir arquivos EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## O que é um arquivo EOT?

Um arquivo com extensão .eot é uma fonte OpenType incorporada em um documento. Eles são usados principalmente em arquivos da Web, como uma página da Web. Ele foi criado pela Microsoft e é suportado pelos produtos da Microsoft, incluindo o arquivo de apresentação do PowerPoint [.pps](/pt/presentation/pps). O arquivo não é de uso principal e é uma espécie de documento que acompanha o documento principal ou a página da web. Semelhante às fontes OTF, a EOT suporta contornos Postscript e TrueType para os glifos. Os arquivos EOT são menores em tamanho porque são compactados usando a compactação LZ. A EOT usa uma ferramenta da Microsoft para criar uma fonte a partir de fontes TTF/OTF existentes.

## Breve história

A fonte EOT foi submetida ao W3C em 2007 como parte do CSS3, mas devido aos seus requisitos de estar permanentemente instalada em sistema remoto tornou-se o motivo de sua rejeição. Foi reenviado em março de 2008, mas o W3C finalmente escolheu [Web Font Format](/pt/font/woff/) (WOFF), que foi padronizado na época.

## Formato de arquivo EOT

Os detalhes do formato do arquivo EOT podem ser encontrados na [página de envio do W3](https://www.w3.org/Submission/EOT/#FileFormat) e elabora a estrutura usada por esse formato de fonte. O EOT consiste em uma única estrutura EMBEDDEDFONT que fornece informações básicas suficientes sobre o nome da fonte e os caracteres suportados. O empacotamento dessas informações permite que os Agentes do Usuário evitem descompactar, descompactar ou instalar a fonte se ela já estiver presente na máquina.

### Estrutura da FONTE EMBEDDED
A estrutura EMBEDDEDFONT passou por três revisões, com adição de dados adicionais ao final da estrutura a cada revisão. A última revisão da estrutura EMBEDDEDFONT é mostrada abaixo.

|Tipo de dados|Nome da entrada|Descrição|
---|---|---|
|unsigned long|EOTSize|Comprimento total da estrutura em bytes (incluindo dados de string e fonte)|
|unsigned long|FontDataSize|Comprimento da fonte OpenType (FontData) em bytes|
|unsigned long|Versão|Número da versão deste formato - 0x00020002|
|unsigned long|Flags|Processing Flags|
|byte[10]|FontPANOSE|O valor PANOSE para esta fonte - Consulte http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|No Windows isso é derivado de TEXTMETRIC.tmCharSet. Este valor especifica o conjunto de caracteres da fonte. DEFAULT_CHARSET (0x01) indica nenhuma preferência. - Consulte https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Se o bit para ITALIC estiver definido em OS/2.fsSelection, o valor será 0x01 - Consulte http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Weight|O valor do peso para esta fonte - Consulte http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Tipo sinalizadores que fornecem informações sobre permissões de incorporação - Consulte http://www.microsoft.com/typography/otspec/os2.htm#fst|
|unsigned short|MagicNumber|Número mágico para arquivo EOT - 0x504C. Usado para verificar se há corrupção de dados.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bits 0-31) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bits 64-95) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bits 0-31) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bits 32-63) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Consulte https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserved1|Reserved - deve ser 0|
|unsigned long|Reserved2|Reservado - deve ser 0|
|unsigned long|Reserved3|Reserved - deve ser 0|
|unsigned long|Reserved4|Reserved - deve ser 0|
|unsigned short|Padding1|Padding para manter o alinhamento longo. O valor de preenchimento sempre deve ser definido como 0x0000.|
|unsigned short|FamilyNameSize|Número de bytes usados pelo array FamilyName|
|byte|FamilyName[FamilyNameSize]|Matriz de caracteres UTF-16 com o comprimento de bytes FamilyNameSize. Esta é a cadeia de caracteres da família de fontes do idioma inglês encontrada na tabela de nomes da fonte (ID do nome = 1) - Consulte http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding2|O valor de preenchimento deve sempre ser definido como 0x0000.|
|unsigned short|StyleNameSize|Número de bytes usados pelo StyleName|
|byte|StyleName[StyleNameSize]|Matriz de caracteres UTF-16 com o comprimento de bytes StyleNameSize. Esta é a cadeia de caracteres da subfamília de fontes do idioma inglês encontrada na tabela de nomes da fonte (ID do nome = 2) - Consulte http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding3|O valor de preenchimento deve sempre ser definido como 0x0000.|
|unsigned short|VersionNameSize|Número de bytes usados pelo VersionName|
|bytes|VersionName[VersionNameSize]|Matriz de caracteres UTF-16 com o comprimento de bytes VersionNameSize. Esta é a string da versão do idioma inglês encontrada na tabela de nomes da fonte (ID do nome = 5) - Consulte http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding4|O valor de preenchimento deve sempre ser definido como 0x0000.|
|unsigned short|FullNameSize|Número de bytes usados pelo FullName|
|byte|FullName[FullNameSize]|Matriz de caracteres UTF-16 com o comprimento de bytes FullNameSize. Esta é a cadeia de caracteres de nome completo do idioma inglês encontrada na tabela de nomes da fonte (ID do nome = 4) - Consulte http://www.microsoft.com/typography/otspec/name.htm|
|unsigned short|Padding5|O valor de preenchimento deve sempre ser definido como 0x0000.|
|unsigned short|RootStringSize|Número de bytes usados pelo array RootString|
|byte|RootString[RootStringSize]|Matriz de caracteres UTF-16 com o comprimento de bytes RootStringSize.|
|unsigned long|RootStringCheckSum|Valor de RootString CheckSum. Veja algoritmo para processar RootStringChecksum abaixo.|
|unsigned long|EUDCCodePage|Valor de página de código necessário para suporte de fonte EUDC.|
|unsigned short|Padding6|O valor de preenchimento deve sempre ser definido como 0x0000.|
|unsigned short|SignatureSize|Número de bytes usados pelo array Signature. Atualmente reservado e deve ser definido como 0x0000.|
|byte|Assinatura[SignatureSize]|Atualmente reservado. Se o SignatureSize for 0x0000, não há comprimento para esta matriz.|
|unsigned long|EUDCFlags|Processando sinalizadores para a fonte EUDC. Os valores típicos podem ser TTEMBED_XORENCRYPTDATA e TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Número de bytes usados pelo array Signature.|
|byte|EUDCFontData[EUDCFontSize]|Número de bytes usados para os dados de fonte EUDC. Se o EUDCFontSize for 0x00000000, não há comprimento para esta matriz.|
|byte|FontData[FontDataSize]|Os dados da fonte para este arquivo EOT. Os dados podem ser compactados ou criptografados por XOR conforme indicado pelos sinalizadores de processamento.|

## Referências

* [Formato de arquivo EOT](https://www.w3.org/Submission/EOT/)
* [OpenType incorporado](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Font Embedding](https://en.wikipedia.org/wiki/Font_embedding)

