{
  "date" : "2019-12-13",
  "keywords" :["WAV", "файл", "разширение", "формат", "файлов формат за обмен на аудио", "музика"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Научете за WAV файловия формат и API, които могат да създават и отварят WAV файлове.",
  "title" :"WAV - Формат на аудио файл с вълнова форма",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Какво е WAV файл?

WAV, известен като WAVE (Waveform Audio File Format), е подмножество от спецификацията на Microsoft Resource Interchange File Format (RIFF) за съхраняване на цифрови аудио файлове. Форматът не прилага никаква компресия към битовия поток и съхранява аудиозаписите с различни честоти на дискретизация и битрейт. Той е бил и е един от стандартните формати за аудио компактдискове. Wave файловете са с по-голям размер в сравнение с новите аудио файлови формати като [MP3](/bg/audio/mp3/), който използва компресия със загуби, за да намали размера на файла, като същевременно поддържа същото качество на звука. Въпреки това WAV файловете могат да бъдат компресирани с помощта на кодеци на Audio Compression Manager (ACM). Налични са няколко API и приложения, които могат да конвертират WAV файлове в други популярни аудио файлови формати.

**Знаеше ли?**
Можете да станете сътрудник на FileFormat.com, за да поддържате общността на файловите формати в крак с вашите открития. Ако трябва да споделите нещо относно WAV или аудио файловите формати, можете да публикувате констатациите си в секцията [Новини за аудио файловия формат](https://news.fileformat.com/t/audio), за да могат хората да бъдат информирани.

## WAV файлов формат ##

Файловият формат WAVE, който е подмножество на спецификацията RIFF на Microsoft, започва с заглавка на файла, последвана от последователност от части от данни. WAVE файлът има единична "WAVE" част, която се състои от две под-части:

* част "fmt" - определя формата на данните
* част "данни" - съдържа действителните примерни данни

### Заглавка на WAV файл ###

Заглавката на WAV (RIFF) файл е с дължина 44 байта и има следния формат:


|Позиции|Примерна стойност|Описание
---|---|---|
|1 - 4|"RIFF"|Маркира файла като риф файл. Всеки знак е с дължина 1 байт.
|5 - 8|Размер на файла (цяло число)|Размер на целия файл - 8 байта, в байтове (32-битово цяло число). Обикновено трябва да попълните това след създаването.
|9 -12|"WAVE"|Заглавка на тип файл. За нашите цели винаги е равно на "WAVE".
|13-16|"fmt "|Маркер за формат на парче. Включва крайна нула
|17-20|16|Дължина на данните за формат, както е посочено по-горе
|21-22|1|Тип формат (1 е PCM) - 2 байта цяло число
|23-24|2|Брой канали - 2 байта цяло число
|25-28|44100|Скорост на дискретизация - 32 байта цяло число. Общите стойности са 44100 (CD), 48000 (DAT). Честота на дискретизация = Брой проби в секунда или херц.
|29-32|176400|(Честота на дискретизация * BitsPerSample * Канали) / 8.
|33-34|4|(BitsPerSample * Канали) / 8.1 - 8 бита моно2 - 8 бита стерео/16 бита моно4 - 16 бита стерео
|35-36|16|Битове на проба
|37-40|"данни"|заглавка на парче "данни". Маркира началото на секцията с данни.
|41-44|Размер на файла (данни)|Размер на секцията с данни.
|По-горе са дадени примерни стойности за 16-битов стерео източник.

## Препратки ##

* [WAV - от Wikipedia](https://en.wikipedia.org/wiki/WAV)
