
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC — файл байт-кода ActionScript",
  "description":"Узнайте, что такое формат файла ABC, с примерами и API, которые могут создавать и открывать файлы ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## .ABC вариант №

Файл с расширением .abc представляет собой файл байт-кода ActionScript, созданный компилятором Flash в результате компиляции файлов сценариев ActionScript. Байт-код, содержащийся в файле ABC, выполняется виртуальной машиной ActionScript (AVM и AVM2). Байт-код состоит из постоянных данных, инструкций из набора инструкций AVM2 и различных видов метаданных. Когда файл ABC загружается в AVM или AVM2, он проходит проверку. Если он не соответствует Обзору AVM2, он отклоняется. Файлы ABC можно открывать в Adobe Flash Player, поддержка которого давно прекращена.

## Формат файла ABC — дополнительная информация

Файлы ABC сохраняются на диск в двоичном формате, который может быть прочитан виртуальными машинами AVM или AVM2. Его внутренняя файловая структура представляет собой исполняемый блок кода со всеми его постоянными данными, дескрипторами типов, кодом и метаданными.

## Структура файла ABC

Структура файла ABC показана ниже.

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

### Поля файла ABC

|Имя поля|Описание|
---|---|
|minor_version, major_version|Значения major_version и minor_version представляют собой основной и дополнительный номера версий формата abcFile.|
|constant_pool|constant_pool — это структура переменной длины, состоящая из целых чисел, двойных чисел, строк, пространств имен, наборов пространств имен и множественных имен.|
|method_count, method|Значение method_count — это количество записей в массиве методов. Каждая запись в массиве методов представляет собой структуру переменной длины method_info.|
|metadata_count, metadata|Значение metadata_count — это количество записей в массиве метаданных. Каждая запись метаданных представляет собой структуру metadata_info, которая сопоставляет имя с набором строковых значений. |
|class_count, instance, class|Значение class_count — это количество записей в экземплярах и массивах классов. |
|script_count, script|Значением script_count является количество записей в массиве скриптов. Каждая запись скрипта представляет собой структуру script_info, которая определяет характеристики отдельного скрипта в этом файле. |
|method_body_count, method_body|Значение method_body_count равно количеству записей в массиве method_body. Каждый method_bodyentry состоит из структуры method_body_info переменной длины, которая содержит инструкции для отдельного метода или функции.|

## использованная литература

* [Надежный ABC (байт-код ActionScript) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

