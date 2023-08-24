{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo PCX - Archivo de imagen de mapa de bits de pincel",
  "description":"Obtenga información sobre el formato de archivo PCX y las API que pueden crear y abrir archivos PCX",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## ¿Qué es un archivo PCX?

Un archivo PCX, un archivo Picture Exchange, es un formato de archivo de imagen de trama que se usó como formato de archivo nativo para la aplicación PC Paintbrush. Fue desarrollado por ZSoft Corporation, EE. UU. para plataformas DOS y Windows y fue adoptado como el principal formato de archivo de imágenes antes de la llegada de [BMP](/es/image/bmp/), [JPEG](/es/image/jpeg/) y [ PNG](/es/image/png/) formatos de archivo. Los archivos PCX tienen un tamaño más pequeño ya que se comprimen con la codificación RLE. Se utiliza en el archivo de varias páginas [DCX](/es/image/dcx/) que se utiliza principalmente para crear archivos de fax digital.

## Formato de archivo PCX

Los archivos PCX se guardan en el disco en formato de archivo binario. La estructura de formato de archivo interno sigue el orden de bytes little endian y tiene las siguientes tres secciones:

**`Encabezado PCX`**: un encabezado PCX tiene una longitud de 128 bytes. Contiene un identificador, un número de versión, dimensiones de la imagen, 16 colores de paleta, número de planos de color y profundidad de bits de cada plano, y un valor para el método de compresión.

El encabezado PCX es como se muestra a continuación con una referencia de la Enciclopedia de formatos de archivo de gráficos (2ª ed.).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`Image Data`**: los datos de imagen PCX siguen justo después del encabezado. Los datos de la imagen pueden comprimirse según la configuración de campo en el encabezado. El almacenamiento de datos en el archivo PCX depende del número de planos de color especificados. Los datos de imagen se organizan en filas. En el caso de varios planos, estos se almacenan por plano dentro de la fila en disposición secuencial de datos rojos, verdes y azules. Este patrón se repite para cada línea en el plano.

## Referencias

* [PCX - Por Wikipedia](https://en.wikipedia.org/wiki/PCX)

