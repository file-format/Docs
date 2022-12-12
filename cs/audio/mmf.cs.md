{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "soubor", "přípona", "formát", "audio", "smaf", "přípona mmf", "soubory mmf", "mobilní hudební soubor", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru MMF a rozhraních API, která mohou vytvářet a otevírat soubory MMF.",
  "title" :"MMF - Mobile Music File Format",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Co je soubor MMF?

MMF je přípona souboru přidružená k souboru SMAF. MMF je zkratka pro Mobile Music File, zatímco SMAF je zkratka pro syntetický hudební formát Mobile Application Format. Soubory MMF v chytrém telefonu obsahují systémové vyzváněcí tóny, zvuk a mohou také obsahovat grafiku a textový displej. MMF dále obsahuje tři typy parametrů nástroje včetně FM, PCM a Stream PCM. Tyto formáty souborů jsou kompatibilní se systémovou platformou Windows. Soubory MMF jsou kategorizovány jako datové soubory. Microsoft Mail obvykle podporuje soubory MMF. Soubor s příponou MMF lze zkopírovat do libovolného mobilního zařízení nebo systémové platformy.

Navíc jsou tyto soubory mnohem menší ve srovnání se soubory standardního formátu MIDI. Soubory [WAV](/cs/audio/wav/) a [MID](/cs/audio/mid/) lze převést do formátu MMF, který pak lze sdílet a distribuovat jako zvukový obsah. Tyto soubory lze přijímat e-mailem přímo do telefonů a PC.


## Stručná historie formátu souborů MMF

Yamaha vyvinula nástroje SMAF jako zvukové soubory, takže chytré telefony mohou uložit větší počet jedinečných vyzváněcích tónů. Yamaha představila SMAF s výrobou svých zvukových čipů MA-1, MA-2, MA-3, MA-5 a MA-7 LSI. Všechny tyto formáty se na začátku roku 2000 staly mezi mobilními telefony na východoasijském trhu docela známé.

Na mezinárodní úrovni byl formát MMF schválen společností Samsung. S pomocí formátu MMF byl Samsung schopen navrhnout širokou škálu polyfonních vyzváněcích tónů pro použití v chytrých telefonech Samsung.

Yamaha chtěla tento formát učinit ještě populárnějším, a tak na oficiálních souborech Yamaha SMAF zveřejnila více nástrojů kompatibilních s tímto formátem. Díky tomu mohou nyní uživatelé snadno přehrávat soubory MMF na svých počítačích.


## Specifikace formátu souboru MMF ##

Soubory MMF jsou kategorizovány do datových sekcí. K popisu každého segmentu se používá struktura s předponou kolem 8 bajtů.
Čtyřbajtový štítek zahrnuje CNTI, OPDA, MSTR, MTR a ATR. Velikost dat plus 8 bajtů je velikost bloku; velikost celého souboru se vypočítá sečtením velikostí všech částí. Pokud soubor nebyl poškozen, měla by být celková velikost souboru stejná jako velikost primárního záhlaví.

### Záhlaví ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Zde je příklad souboru MMF:

![](../mmf.png)

## Reference

* [MMF – z Wikipedie](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

