{
  "date" : "2020-08-20",
  "keywords" :[ "archivo eot", "formato de archivo eot", "qué es un archivo eot", "archivo", "ejemplo de eot", "extensión de archivo eot", "extensión", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Formato de archivo de fuente TrueType",
  "description":"Obtenga más información sobre el formato de archivo EOT y las API para crear y abrir archivos EOT",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## ¿Qué es un archivo EOT?

Un archivo con extensión .eot es una fuente OpenType que está incrustada en un documento. Estos se utilizan principalmente en archivos web, como una página web. Fue creado por Microsoft y es compatible con los productos de Microsoft, incluido el archivo de presentación de PowerPoint [.pps](/es/presentation/pps). El archivo no es de uso principal y es una especie de documento que acompaña al documento principal o página web. Al igual que las fuentes OTF, EOT admite contornos Postscript y TrueType para los glifos. Los archivos EOT son de menor tamaño debido a que se comprimen con compresión LZ. EOT utiliza una herramienta de Microsoft para crear una fuente a partir de fuentes TTF/OTF existentes.

## Breve historia

La fuente EOT se envió al W3C en 2007 como parte de CSS3, pero debido a sus requisitos de instalación permanente en un sistema remoto, se convirtió en el motivo de su rechazo. Se volvió a enviar en marzo de 2008, pero W3C finalmente eligió [Web Font Format](/es/font/woff/) (WOFF), que estaba estandarizado en ese momento.

## Formato de archivo EOT

Los detalles del formato de archivo EOT se pueden encontrar en [página de envío W3](https://www.w3.org/Submission/EOT/#FileFormat) y elabora la estructura utilizada por este formato de fuente. El EOT consta de una única estructura EMBEDDEDFONT que proporciona suficiente información básica sobre el nombre de la fuente y los caracteres admitidos. El empaquetado de esta información permite a los Agentes de Usuario evitar desempaquetar, descomprimir o instalar la fuente si ya está presente en la máquina.

### Estructura del FONDO INTEGRADO
La estructura EMBEDDEDFONT ha pasado por tres revisiones, con la adición de datos adicionales al final de la estructura con cada revisión. La última revisión de la estructura EMBEDDEDFONT se muestra a continuación.

|Tipo de datos|Nombre de entrada|Descripción|
---|---|---|
|unsigned long|EOTSize|Longitud total de la estructura en bytes (incluidos datos de cadena y fuente)|
|unsigned long|FontDataSize|Longitud de la fuente OpenType (FontData) en bytes|
|unsigned long|Version|Número de versión de este formato - 0x00020002|
|unsigned long|Banderas|Banderas de procesamiento|
|byte[10]|FontPANOSE|El valor PANOSE para esta fuente: consulte http://www.microsoft.com/typography/otspec/os2.htm#pan|
|byte|Charset|En Windows, esto se deriva de TEXTMETRIC.tmCharSet. Este valor especifica el conjunto de caracteres de la fuente. DEFAULT_CHARSET (0x01) indica que no hay preferencia. - Consulte https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Cursiva|Si el bit para CURSIVA está establecido en OS/2.fsSelection, el valor será 0x01 - Consulte http://www.microsoft.com/typography/otspec/os2.htm#fss|
|unsigned long|Peso|El valor de peso de esta fuente: consulte http://www.microsoft.com/typography/otspec/os2.htm#wtc|
|unsigned short|fsType|Indicadores de tipo que brindan información sobre permisos de incrustación: consulte http://www.microsoft.com/typography/otspec/os2.htm#fst|
|Corto sin firmar|MagicNumber|Número mágico para archivo EOT - 0x504C. Se utiliza para comprobar si hay corrupción de datos.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (bits 0-31) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (bits 32-63) - Ver http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (bits 64-95) - Ver http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (bits 96-127) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#ur|
|unsigned long|CodePageRange1|CodePageRange1 (bits 0-31) - Consulte http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (bits 32-63): consulte http://www.microsoft.com/typography/otspec/os2.htm#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - Ver https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reservado1|Reservado - debe ser 0|
|unsigned long|Reservado2|Reservado - debe ser 0|
|unsigned long|Reservado3|Reservado - debe ser 0|
|unsigned long|Reservado4|Reservado - debe ser 0|
|corto sin firmar|Padding1|Relleno para mantener la alineación larga. El valor de relleno siempre debe establecerse en 0x0000.|
|corto sin firmar|FamilyNameSize|Número de bytes utilizados por la matriz FamilyName|
|byte|FamilyName[FamilyNameSize]|Matriz de caracteres UTF-16 con la longitud de bytes de FamilyNameSize. Esta es la cadena de la familia de fuentes en idioma inglés que se encuentra en la tabla de nombres de la fuente (ID de nombre = 1). Consulte https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|El valor de relleno siempre debe establecerse en 0x0000.|
|sin signo corto|StyleNameSize|Número de bytes utilizados por StyleName|
|byte|StyleName[StyleNameSize]|Matriz de caracteres UTF-16 de la longitud de StyleNameSize bytes. Esta es la cadena de subfamilia de fuentes en idioma inglés que se encuentra en la tabla de nombres de la fuente (ID de nombre = 2). Consulte https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|El valor de relleno siempre debe establecerse en 0x0000.|
|corto sin firmar|VersionNameSize|Número de bytes utilizados por VersionName|
|bytes|VersionName[VersionNameSize]|Matriz de caracteres UTF-16 de la longitud de VersionNameSize bytes. Esta es la cadena de la versión en inglés que se encuentra en la tabla de nombres de la fuente (ID de nombre = 5). Consulte https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|El valor de relleno siempre debe establecerse en 0x0000.|
|sin signo corto|FullNameSize|Número de bytes utilizados por FullName|
|byte|FullName[FullNameSize]|Matriz de caracteres UTF-16 con la longitud de bytes FullNameSize. Esta es la cadena de nombre completo en inglés que se encuentra en la tabla de nombres de la fuente (ID de nombre = 4). Consulte https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|El valor de relleno siempre debe establecerse en 0x0000.|
|sin signo corto|RootStringSize|Número de bytes utilizados por la matriz RootString|
|byte|RootString[RootStringSize]|Matriz de caracteres UTF-16 con la longitud de bytes de RootStringSize.|
|unsigned long|RootStringCheckSum|valor de RootString CheckSum. Consulte el algoritmo para procesar RootStringChecksum a continuación.|
|unsigned long|EUDCCodePage|Valor de página de códigos necesario para la compatibilidad con fuentes EUDC.|
|unsigned short|Padding6|El valor de relleno siempre debe establecerse en 0x0000.|
|unsigned short|SignatureSize|Número de bytes utilizados por la matriz Signature. Actualmente reservado y debe establecerse en 0x0000.|
|byte|Firma[Tamaño de firma]|Actualmente reservado. Si SignatureSize es 0x0000, esta matriz no tiene longitud.|
|unsigned long|EUDCFlags|Indicadores de procesamiento para la fuente EUDC. Los valores típicos pueden ser TTEMBED_XORENCRYPTDATA y TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|Número de bytes utilizados por la matriz Signature.|
|byte|EUDCFontData[EUDCFontSize]|Número de bytes utilizados para los datos de fuente EUDC. Si EUDCFontSize es 0x00000000, esta matriz no tiene longitud.|
|byte|FontData[FontDataSize]|Los datos de fuente para este archivo EOT. Los datos pueden comprimirse o cifrarse con XOR según lo indiquen las banderas de procesamiento.|

## Referencias

* [Formato de archivo EOT](https://www.w3.org/Submission/EOT/)
* [OpenType integrado](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Incrustación de fuentes](https://en.wikipedia.org/wiki/Font_embedding)

