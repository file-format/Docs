
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - файл байтового коду ActionScript",
  "description":"Дізнайтеся про формат файлу ABC із прикладом і API, які можуть створювати та відкривати файли ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Що таке файл ABC?

Файл із розширенням .abc — це файл байтового коду ActionScript, створений компілятором Flash у результаті компіляції файлів сценаріїв ActionScript. Байт-код, що міститься у файлі ABC, виконується віртуальною машиною ActionScript (AVM і AVM2). Байт-код містить постійні дані, інструкції з набору інструкцій AVM2 і різні види метаданих. Коли файл ABC завантажується в AVM або AVM2, він проходить перевірку. Якщо він не відповідає огляду AVM2, він відхиляється. Файли ABC можна відкривати в Adobe Flash Player, який давно припинено.

## Формат файлу ABC – Додаткова інформація

Файли ABC зберігаються на диску у двійковому форматі, який читають віртуальні машини AVM або AVM2. Його внутрішня файлова структура представляє блок виконуваного коду з усіма його постійними даними, дескрипторами типів, кодом і метаданими.

## Структура файлу ABC

Структура файлу ABC показана нижче.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Поля файлу ABC

|Назва поля|Опис|
---|---|
|minor_version, major_version|Значення major_version і minor_version є номерами основної та другорядної версій формату abcFile.|
|constant_pool|Constant_pool — це структура змінної довжини, що складається з цілих чисел, подвійних чисел, рядків, просторів імен, наборів просторів імен і мультиімен.|
|method_count, method|Значення method_count — це кількість записів у масиві методів. Кожен запис у масиві методів є структурою method_info змінної довжини.|
|metadata_count, metadata|Значення metadata_count — це кількість записів у масиві метаданих. Кожен запис метаданих є metadata_infostructure, яка відображає ім’я на набір рядкових значень. |
|class_count, екземпляр, клас|Значення class_count — це кількість записів у екземплярі та масивах класів. |
|script_count, script|Значення script_count — це кількість записів у масиві сценаріїв. Кожен запис сценарію є структурою script_info, яка визначає характеристики окремого сценарію в цьому файлі. |
|method_body_count, method_body|Значення method_body_count — це кількість записів у масиві method_body. Кожен method_bodyentry складається зі структури method_body_info змінної довжини, яка містить інструкції для окремого методу або функції.|

## Список літератури

* [Надійний ABC (байт-код ActionScript) [Dis-]Ассемблер - Github](https://github.com/CyberShadow/RABCDAsm)

