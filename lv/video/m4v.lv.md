{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"failu",
"pagarinājumu",
"formātā",
"MPEG-4",
"Digitālo tiesību pārvaldība",
"DRM",
"Apple",
"video"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "Uzziniet par M4V faila formātu un API, kas var izveidot un atvērt M4V failus.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-lvv"
}
},
  "lastmod": "2019-09-14"
}

## Kas ir M4V fails?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V izmanto H.264 video un **[AAC](/audio/aac/)** un Dolby Digital audio kodēšanai un dekodēšanai.

## M4V faila struktūra ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V, kas definēts pēc apakštipa, kam jābūt M4V_”. Papildu gabalu tipi ir iepriekš definēti paraksti: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide , load, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt, ssrc,  PICT. Atkārtojot gabalus, līdz tiek atklāts nezināms veids, mēs veidojam M4V failu.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. Nobīdē 32 (hex: 20) atrodas otrā daļa, kuras izmērs ir 30 322 (hex: 00 00 76 72, big-endian, pirmais zemākais baits) un tips **moov** (hex: 6D 6F 6F 76). Nākamā daļa atrodas nobīdē 32+30,322#30,354 (hex: 00 00 76 92), un tās izmērs ir 8 (hex: 00 00 00 08) un veids ir **free** (hex: 66 72 65 65).
### M4V izmantotie kodeki ###

#### Video Codec H.264 ####

H.264 ir video saspiešanas standarts, kas pārvērš digitālo video formātā, kas prasa mazāk vietas, kad nepieciešama pārraide vai uzglabāšana. M4V video saspiešanai izmanto H.264. Tās pielietojums svārstās no DVD, TV, videokonferencēm un video straumēšanas internetā. H.264 sastāv no divām galvenajām daļām: Encoder — kas saspiež video, dekodētājs — kas atspiež saspiesto video atpakaļ. Tālāk esošajā attēlā kodēšanas un dekodēšanas procesi ir izcelti, un citi procesi ir ietverti H.264 standartā.

##### Video kodēšanas un dekodēšanas process H.264 #####

Saspiestai H.264 bitu straumei video kodētājs veic prognozēšanas, pārveidošanas un kodēšanas procesu. Tajā pašā laikā dekodētājs veic apgriezto dekodēšanas, apgrieztās pārveidošanas un rekonstrukcijas procesu, lai atjaunotu video failu. H.264 aizņem uz pusi mazāku izmēru nekā MPEG.

#### Audio kodeks ####

Advanced Audio Coding (AAC) ir audio kodeks, kas paredzēts digitālā audio saspiešanai ar zudumiem, un tiek izmantots M4V konteinerā. AAC ir [MP3](/audio/mp3/) formāta pēctecis un nodrošina labāku kvalitāti nekā MP3 ar tādu pašu bitu pārraides ātrumu. AAC formāts saspiešanas procesa laikā izmet daļu informācijas, kas ir mazāk svarīga. AAC ir mainīga bitu ātruma (VBR) uz blokiem balstīts kodeks, kurā katrs bloks dekodē līdz 1024 laika domēna paraugiem.

### Atsauces ###

* [Wikipedia — M4V](https://en.wikipedia.org/wiki/M4V)

* [Wikipedia — MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


