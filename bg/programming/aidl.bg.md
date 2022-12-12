{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL файл – езиков файл за дефиниране на интерфейс на Android",
  "description":"Научете какво е AIDL файлов формат с пример и API, които могат да създават и отварят AIDL файлове.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Какво е AIDL файл?

AIDL (Android Interface Definition Language) файл позволява на разработчиците на Android да установяват комуникация между различни приложения. Въз основа на интерфейса за програмиране и клиентът, и услугата се съгласяват да комуникират чрез междупроцесна комуникация (IPC). AIDL файлът съдържа [Java](/bg/programming/java/) изходен код за дефиниране на тези интерфейси и договори за комуникация между приложения.

Можете да отваряте AIDL файлове с Google Android Studio или всеки текстов редактор като Microsoft Notepad и Notepad++.

## AIDL файлов формат - повече информация

AIDL са текстови файлове, които съдържат интерфейсите за комуникация между приложенията. Android OS не позволява на един процес да има достъп до паметта на друг процес. Това кара процесите да разделят своите обекти на примитиви за разбиране на основната операционна система и да установят процеса на комуникационни структури за разработчиците.

### Какви типове данни се поддържат от AIDL?

AIDL поддържа следните типове данни по подразбиране.

* Всички примитивни типове в езика за програмиране Java (като int, long, char, boolean и т.н.)
* Низ
* CharSequence
* Списък
* Карта

## Пример за AIDL файл

Следва примерен AIDL файл.

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
## Препратки

* [Език за дефиниране на интерфейс на Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

