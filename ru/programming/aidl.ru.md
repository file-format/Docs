{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл AIDL — языковой файл определения интерфейса Android",
  "description":"Узнайте, что такое формат файла AIDL, с примерами и API-интерфейсами, которые могут создавать и открывать файлы AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .AIDL вариант №

Файл AIDL (язык определения интерфейса Android) позволяет разработчикам Android устанавливать связь между различными приложениями. На основе интерфейса программирования и клиент, и служба соглашаются взаимодействовать с помощью межпроцессного взаимодействия (IPC). Файл AIDL содержит исходный код [Java](/ru/programming/java/) для определения этих интерфейсов и контрактов для связи между приложениями.

Вы можете открывать файлы AIDL с помощью Google Android Studio или любого текстового редактора, такого как Microsoft Notepad и Notepad++.

## Формат файла AIDL — дополнительная информация

AIDL — это текстовые файлы, содержащие интерфейсы для связи между приложениями. ОС Android не позволяет одному процессу получать доступ к памяти другого процесса. Это приводит к тому, что процессы разбивают свои объекты на примитивы для понимания базовой операционной системы и устанавливают процесс коммуникационных структур для разработчика.

### Какие типы данных поддерживает AIDL?

AIDL по умолчанию поддерживает следующие типы данных.

* Все примитивные типы языка программирования Java (такие как int, long, char, boolean и т. д.)
* Нить
* последовательность символов
* Список
* Карта

## Пример файла AIDL

Ниже приведен пример файла AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## использованная литература

* [Язык определения интерфейса Android (AIDL)] (https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

