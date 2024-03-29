{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла BML — файл языка разметки компонентов",
  "description":"Узнайте о формате файла BML и API-интерфейсах, которые могут создавать и открывать файлы BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## .BML вариант №

Файл с расширением .bml представляет собой файл языка разметки компонентов, в котором хранятся классы Java для поддержки приложений Java. Это позволяет получить доступ к объектам и методам Java и не требует создания новых функций с использованием классов Java. Он определяет, как компоненты связаны друг с другом для выполнения полезных задач. BML был разработан IBM alphaWorks для описания взаимосвязей между структурами и компонентами. Файлы BML можно открывать и просматривать с помощью любого текстового редактора, такого как веб-браузеры, Microsoft Notepad и Notepad++.

## Формат файла BML

Веб-сайт IBM alphaworks предоставил две реализации BML. Первая реализация представляет собой интерпретатор, который «проигрывает» сценарий BML для создания желаемой иерархии компонентов. Вторая реализация представляет собой компилятор, который компилирует любой сценарий BML в код Java без отражения. Это выгодно в том смысле, что позволяет зафиксировать межкомпонентную структуру приложения с помощью языка, разработанного для этой конкретной цели, с дополнительной возможностью компилировать его в «обычный» код Java.

## BML-теги

Ниже приводится объяснение некоторых тегов, используемых в языке BML:

###<bean> ярлык:

<bean>элемент используется для создания новых бинов или для поиска бинов по имени.<bean> тег имеет формат:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
"id" в теге связан с реестром объектов для JavaBean.

###<string> ярлык

Существует два способа использования строкового тега:

1. Чтобы создать непустую строку:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Чтобы создать пустую строку:

```
<string/>
```
## использованная литература

* [Объектно-ориентированный обмен сообщениями с XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Физический язык разметки](http://web.mit.edu/mecheng/pml/standards.htm)


