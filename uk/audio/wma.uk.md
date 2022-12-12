{
  "date" : "2021-02-20",
  "keywords" :[ "WMA", "файл", "розширення", "формат", "формат файлу для обміну аудіо", "музика"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу WMA та API, які можуть створювати та відкривати файли WMA.",
  "title" :"WMA - аудіофайл Windows Media",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-20"
}

## Що таке файл WMA?

Файл із розширенням .wma — це аудіофайл, збережений у форматі Advanced Systems Format (ASF). ASF — це власний формат Microsoft, який містить бітові потоки, закодовані за допомогою Windows Media Audio 9. Окрім аудіовмісту, файл WMA також містить такі об’єкти метаданих, як назва, альбом, виконавець і жанр доріжки. Файли WMA в основному використовуються для потокового передавання через Інтернет, подібно до файлів [.mp3](/uk/audio/mp3/).

## Формат файлу WMA

Файл WMA є двійковим форматом і міститься у форматі файлу ASF. Він визначає кодування метаданих про файл, подібне до тегів ID3, які використовуються файлами MP3. Кодек WMA використовується корпорацією Майкрософт у форматі файлів із захищеним взаємодію (PIFF) з 2008 року. Однак він не був оголошений як стандартизований аудіокодек відповідними галузевими стандартами, такими як DECE UltraViolet і MPEG-DASH.

### Специфічні дані типу WMA

Специфічна для типу інформація кодека Windows Media Audio зберігається в такому форматі як частина специфічних для типу даних об’єкта властивостей потоку.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## Список літератури

* [Огляд ASF – Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)

