{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "fișier", "extensie", "format", "format fișier de schimb audio", "muzică"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul de fișier WMA și despre API-urile care pot crea și deschide fișiere WMA.",
  "title" :"WMA – fișier audio Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Ce este un fișier WMA?

Un fișier cu extensia .wma reprezintă un fișier audio care este salvat în formatul Advanced Systems Format (ASF). ASF este formatul proprietar al Microsoft, care conține fluxuri de biți codificate de Windows Media Audio 9. Pe lângă conținutul audio, un fișier WMA conține și obiecte de metadate, cum ar fi titlul, albumul, artistul și genul piesei. Fișierele WMA sunt utilizate în principal pentru transmiterea în flux pe web, similar fișierelor [.mp3](/ro/audio/mp3/).

## Format de fișier WMA

Un fișier WMA este format de fișier binar și este conținut în formatul de fișier ASF. Specifică codificarea metadatelor despre fișier similar cu etichetele ID3 utilizate de fișierele MP3. Codecul WMA este utilizat de către Microsoft în formatul său de fișier interoperabil protejat (PIFF) din 2008. Cu toate acestea, nu a fost declarat ca codec audio standardizat de standardele industriale aferente, cum ar fi DECE UltraViolet și MPEG-DASH.

### Date specifice tipului WMA

Informațiile specifice tipului pentru codecul Windows Media Audio sunt stocate în următorul format ca parte a Datelor specifice tipului din obiectul Proprietăți flux.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Referințe

* [Prezentare generală ASF - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

