{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "файл", "розширення", "формат", "audio", "smaf", "mmf extension", "mmf files", "mobile music file", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Дізнайтеся про формат файлу MMF та API, які можуть створювати та відкривати файли MMF.",
  "title" :"MMF - формат мобільного музичного файлу",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Що таке файл MMF?

MMF — це розширення файлу, пов’язане з файлом SMAF. MMF означає мобільний музичний файл, тоді як SMAF означає синтетичний музичний формат мобільної програми. Файли MMF у смартфоні містять системні мелодії дзвінка, звук, а також можуть містити графіку та текст. MMF також містить три типи параметрів приладу, включаючи FM, PCM і Stream PCM. Ці формати файлів сумісні з системною платформою Windows. Файли MMF класифікуються як файли даних. Зазвичай Microsoft Mail підтримує файли MMF. Файл із суфіксом MMF можна скопіювати на будь-який мобільний пристрій або системну платформу.

Крім того, ці файли набагато менші за розміром порівняно зі стандартними файлами формату MIDI. Файли [WAV](/uk/audio/wav/) і [MID](/uk/audio/mid/) можна конвертувати у формат MMF, яким потім можна ділитися та розповсюджувати як аудіовміст. Ці файли можна отримати електронною поштою безпосередньо на телефони та ПК.


## Коротка історія формату файлів MMF

Yamaha розробила інструменти SMAF у вигляді звукових файлів, щоб смартфони могли зберігати більшу кількість унікальних мелодій. Yamaha представила SMAF з виробництвом звукових мікросхем LSI MA-1, MA-2, MA-3, MA-5 і MA-7. Усі ці формати стали досить звичними серед мобільних телефонів на ринку Східної Азії на початку 2000 року.

На міжнародному рівні формат MMF дозволив Samsung. За допомогою формату MMF компанія Samsung змогла створити широкий спектр поліфонічних мелодій для використання в смартфонах Samsung.

Yamaha хотіла зробити формат ще більш популярним, тому в офіційних файлах Yamaha SMAF опубліковано більше інструментів, сумісних із цим форматом. Завдяки цьому користувачі тепер можуть легко відтворювати файли MMF на своїх комп’ютерах.


## Специфікації формату файлу MMF ##

Файли MMF класифікуються за розділами даних. Для опису кожного сегмента використовується префіксна структура навколо 8-байт.
4-байтова мітка включає CNTI, OPDA, MSTR, MTR і ATR. Розмір даних плюс 8 байт — це розмір блоку; розмір усього файлу обчислюється шляхом підсумовування розмірів усіх фрагментів. Якщо файл не пошкоджено, сумарний розмір файлу має збігатися з розміром основного заголовка.

### Заголовок ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Ось приклад файлу MMF:

![](../mmf.png)

## Список літератури

* [MMF – Вікіпедія](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)
