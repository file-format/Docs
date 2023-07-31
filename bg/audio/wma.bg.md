{
  "date" : "2021-02-20",
  "keywords" :["WMA", "файл", "разширение", "формат", "файлов формат за обмен на аудио", "музика"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за WMA файловия формат и API, които могат да създават и отварят WMA файлове.",
  "title" :"WMA - Windows Media Audio File",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Какво е WMA файл?

Файл с разширение .wma представлява аудио файл, който е записан във формат Advanced Systems Format (ASF). ASF е патентован формат на Microsoft, който съдържа потоци от битове, кодирани от Windows Media Audio 9. В допълнение към аудио съдържанието, WMA файлът съдържа и обекти с метаданни като заглавие, албум, изпълнител и жанр на песента. WMA файловете се използват предимно за поточно предаване през мрежата, подобно на [.mp3](/bg/audio/mp3/) файлове.

## WMA файлов формат

WMA файлът е двоичен файлов формат и се съдържа във файловия формат ASF. Той определя кодирането на метаданните за файла, подобно на ID3 таговете, използвани от MP3 файловете. Кодекът WMA се използва от Microsoft в неговия защитен оперативно съвместим файлов формат (PIFF) от 2008 г. Въпреки това, той не е деклариран като стандартизиран аудио кодек от свързаните индустриални стандарти като DECE UltraViolet и MPEG-DASH.

### Специфични данни за типа WMA

Специфичната за типа информация за Windows Media Audio кодека се съхранява в следния формат като част от специфичните за типа данни на обекта на свойствата на потока.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Препратки

* [Общ преглед на ASF - Microsoft](https://learn.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format)

