
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC – файл с байтов код на ActionScript",
  "description":"Научете какво е ABC файлов формат с пример и API, които могат да създават и отварят ABC файлове.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Какво е ABC файл?

Файл с разширение .abc е файл с байтов код на ActionScript, създаден от Flash компилатор в резултат на компилиране на файловете със скриптове на ActionScript. Байтовият код, съдържащ се във файла ABC, се изпълнява от виртуалната машина на ActionScript (AVM и AVM2). Байтовият код се състои от постоянни данни, инструкции от набора инструкции AVM2 и различни видове метаданни. Когато ABC файл се зареди в AVM или AVM2, той се подлага на проверка. Ако не отговаря на общия преглед на AVM2, той се отхвърля. ABC файловете могат да се отварят в Adobe Flash Player, който отдавна е спрян.

## ABC файлов формат - повече информация

ABC файловете се записват на диск в двоичен файлов формат, който може да се чете от AVM или AVM2 виртуални машини. Неговата вътрешна файлова структура представлява изпълним кодов блок с всички негови постоянни данни, типови дескриптори, код и метаданни.

## ABC файлова структура

Файловата структура на ABC е както е показано по-долу.

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

### ABC файлови полета

|Име на поле|Описание|
---|---|
|minor_version, major_version|Стойностите на major_version и minor_version са номерата на основната и второстепенната версия на формата abcFile.|
|constant_pool|Constant_pool е структура с променлива дължина, съставена от цели числа, двойни числа, низове, пространства от имена, набори от пространства от имена и мултиимена.|
|method_count, method|Стойността наmethod_count е броят на записите в масива на метода. Всеки запис в масива на метода е структура с променлива дължина method_info.|
|metadata_count, metadata|Стойността на metadata_count е броят на записите в масива с метаданни. Всеки запис на метаданни е metadata_infostructure, който преобразува име в набор от низови стойности. |
|class_count, instance, class|Стойността на class_count е броят на записите в екземпляра и класовите масиви. |
|script_count, script|Стойността на script_count е броят на записите в масива на скрипта. Всеки запис на скрипт е структура script_info, която дефинира характеристиките на един скрипт в този файл. |
|method_body_count, method_body|Стойността на method_body_count е броят на записите в масива method_body. Всеки method_bodyentry се състои от структура с променлива дължина method_body_info, която съдържа инструкциите за отделен метод или функция.|

## Препратки

* [Силен ABC (ActionScript байт код) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

