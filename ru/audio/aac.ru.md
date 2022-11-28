{
  "date" : "2019-12-13",
  "keywords" :[ "AAC", "файл", "расширение", "формат", "кодирование звука", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Узнайте о формате файла AAC и API-интерфейсах, которые могут создавать и открывать файлы AAC.",
  "title" :"AAC — файл расширенного кодирования звука",
  "linktitle" : "AAC",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-03-03"
}

## .AAC вариант №

AAC (Advanced Audio Coding) относится к стандарту цифрового кодирования звука, который представляет аудиофайлы на основе сжатия звука с потерями. Он был запущен как преемник файлового формата **[MP3](/ru/audio/mp3/)** с учетом того, что стороны столкнулись с проблемами реализации новых идей в процессе кодирования, основанных на развитии методов сжатия данных. AAC обеспечивает лучшее качество звука по сравнению с MP3 при той же скорости передачи данных. Он был определен в MPEG-2 Part 7 (ISO/IEC 13818-7) и в обновленной форме в MPEG-4 Part 3 (ISO/IEC 14496-3).

Формат AAC был принят в качестве формата мультимедиа по умолчанию на YouTube, iPhone, iPod, iPad, Apple iTunes и некоторых других платформах. Доступно несколько приложений и API для преобразования формата файла AAC в другие форматы, такие как MP3, WMA, M4A, **[WAV](/ru/audio/wav/)** и другие.

### Краткая история файла AAC

Формат файла AAC представляет собой расширенную версию MP3 с некоторыми улучшениями. Внесенный несколькими компаниями, включая Институт Фраунгофера (Fraunhofer IIS - разработчики MP3), Nokia, Dolby, AT&T и Sony, формат был объявлен международным стандартом группой экспертов по движущимся изображениям (MPEG) в апреле 1997 года. Позже, в 1999 году, MPEG-2 Part 7 был обновлен и включен в семейство стандартов MPEG-4. Он был известен как MPEG-4 Part 3, обозначенный как ISO/IEC 14496-3: 1999 или MPEG-4 Audio.

## Спецификации формата файла AAC

Спецификации формата файла AAC обеспечивают большую гибкость при разработке кодека, чем MP3, что приводит к более параллельным стратегиям кодирования и эффективному сжатию. Этот формат был выбран рядом аппаратных платформ из-за его улучшений по сравнению с MP3 с точки зрения обеспечения поддержки большего количества параметров даже при меньшей скорости передачи данных. Спецификации формата файла AAC доступны как [MPEG-2, часть 7] (https://www.iso.org/standard/43345.html) и [MPEG-4, часть 3] (https://www.iso.org). /standard/53943.html) (бесплатная загрузка). В формате используются следующие типы носителей:

* аудио/ААС
* аудио/аацп
* аудио/3gpp
* аудио/3gpp2
* аудио/mp4
* аудио/mp4a-латм
* аудио/mpeg4-универсальный

## AAC против MP3 - Улучшения ##

Основные различия между AAC и MP3 с точки зрения улучшений заключаются в следующем:

* AAC поддерживает более широкий диапазон каналов (до 48) и частот дискретизации (от 8 кГц до 96 кГц)
* AAC имеет лучшие частоты кодирования выше 16 кГц
* AAC имеет более широкие пределы изменения частотно-временного разрешения банка фильтров, что привело к улучшенному кодированию переходных процессов и стационарных частей аудиосигнала.
* Более эффективный и простой банк фильтров: гибридный банк фильтров был заменен стандартным MDCT (модифицированным дискретным косинусным преобразованием).
* Поддерживается повышенная эффективность сжатия с помощью Temporal Noise Shaping (TNS), коэффициентов предсказания MDCT-времени (долговременное предсказание), параметрического стереозвука, перцепционного замещения шума, репликации спектральной полосы (SBR).
* более гибкое совместное стерео (можно использовать разные методы в разных частотных диапазонах);

## Использованная литература ##

* [AAC — Википедия] (https://en.wikipedia.org/wiki/Advanced_Audio_Coding)
