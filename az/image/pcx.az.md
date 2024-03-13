{
  "date": "2022-03-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCX Fayl Format - Paintbrush Bitmap Image File",
  "description": "PCX faylları yarada və aça bilən PCX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "PCX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-pc-azx"
}
},
  "lastmod": "2022-03-16"
}

## PCX faylı nədir?

PCX faylı, Picture Exchange faylı, PC Paintbrush tətbiqi üçün yerli fayl formatı kimi istifadə edilən rastr şəkil fayl formatıdır. O, ZSoft Corporation, ABŞ tərəfindən DOS və Windows platformaları üçün hazırlanmışdır və [BMP](/image/bmp/), [JPEG](/image/jpeg/) və [PNG](/image/png/) fayl formatları gəlməmişdən əvvəl əsas təsvir fayl formatı kimi qəbul edilmişdir. PCX faylları RLE kodlaşdırması ilə sıxıldığı üçün daha kiçik ölçülüdür. O, əsasən rəqəmsal faks faylları yaratmaq üçün istifadə edilən çox səhifəli [DCX](/image/dcx/) faylında istifadə olunur.

## PCX fayl formatı

PCX faylları ikili fayl formatında diskdə saxlanılır. Daxili fayl formatı strukturu kiçik endian bayt sıralamasını izləyir və aşağıdakı üç bölmədən ibarətdir:

**`PCX Header`** - PCX Başlığı 128 bayt uzunluğundadır. O, identifikator, versiya nömrəsi, şəkil ölçüləri, 16 palitra rəngi, nömrə rəng təyyarələri və hər bir təyyarənin bit dərinliyi və sıxılma metodu üçün dəyərdən ibarətdir.

PCX Başlığı Qrafik Fayl Formatları Ensiklopediyasından (2-ci nəşr) istinadla aşağıda göstərildiyi kimidir.
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

**`Şəkil Məlumatı`** - PCX təsvir məlumatları başlıqdan dərhal sonra gəlir. Şəkil məlumatları başlıqdakı sahə parametrlərindən asılı olaraq sıxıla bilər. PCX faylında məlumatların saxlanması göstərilən rəng müstəvilərinin sayından asılıdır. Şəkil məlumatları cərgələrdə təşkil edilir. Bir neçə təyyarə olduqda, bunlar qırmızı, yaşıl və mavi məlumatların ardıcıl düzülüşündə cərgə daxilində təyyarə ilə saxlanılır. Bu nümunə təyyarədəki hər bir xətt üçün təkrarlanır.

## İstinadlar

* [PCX - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/PCX)


