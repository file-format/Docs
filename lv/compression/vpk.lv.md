{
  "date": "2022-03-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VPK fails — PlayStation Vita lietojumprogrammu pakotnes faila formāts",
  "description": "Uzziniet par VPK faila formātu un API, kas var izveidot un atvērt VPK failus.",
  "linktitle": "VPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-vp-lvk"
}
},
  "lastmod": "2022-03-01"
}

## Kas ir VPK fails?

Fails ar paplašinājumu .vpk ir saspiests arhīva pakotnes fails, kas tiek izmantots, lai instalētu trešās puses programmas Sony PlayStation Vita spēļu konsolē. Šos failus var instalēt tikai HENkaku jailbreak Vita PlayStation, kas ļāva PS Vita un PSTV izmantot pielāgotu lietotāja izveidotu saturu. VPK arhīva failā ir viss saturs, kas veido spēli, tostarp attēli, piemēram, [PNG](/image/png/) faili, iestatījumu faili, piemēram, [.bin](/disc-and-media/bin/), un visas konfigurācijas faila formātā [XML](/web/xml/).

## VPK faila formāts

VPK faili tiek saglabāti diskā kā standarta saspiesti [ZIP](/compression/zip/) arhīvi. Tajos var būt vairākas mapes un citi saistīti faili, kas paredzēti trešās puses lietotnēm, kas jāinstalē Vita Gaming Console. Lai skatītu VPK pakotnes faila saturu, pārdēvējiet tā paplašinājumu no .vpu uz .zip un izņemiet saturu, izmantojot standarta dekompresijas utilītas, piemēram, WinZip vai WinRAR.

Valvesoftware ir detalizēta informācija par [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format), uz kuru var atsaukties no izstrādātāja viedokļa.

## Kā instalēt VPK failus?

VPK failus var instalēt no komandrindas utilīta VPK.exe. Operētājsistēmā Windows failus var nomest failā vpk.exe, kas atgriež \*.vpk, kurā ir visi iepakotie faili. Alternatīvi komandrindas rīku var izmantot šādi.

### Izveidojiet VPK un pievienojiet failus

```
vpk <dirname>
```

### Izvelciet VPK failus

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK skatītājs

 * [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Atsauces

* [VPK faila formāts](https://developer.valvesoftware.com/wiki/VPK_File_Format)

* [VPK faili](https://developer.valvesoftware.com/wiki/VPK)


