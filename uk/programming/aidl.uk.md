{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл AIDL – файл мови визначення інтерфейсу Android",
  "description":"Дізнайтеся про формат файлу AIDL із прикладом і API, які можуть створювати та відкривати файли AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Що таке файл AIDL?

Файл AIDL (мова визначення інтерфейсу Android) дозволяє розробникам Android встановлювати зв’язок між різними програмами. На основі інтерфейсу програмування і клієнт, і служба погоджуються спілкуватися за допомогою міжпроцесного зв’язку (IPC). Файл AIDL містить вихідний код [Java](/uk/programming/java/) для визначення цих інтерфейсів і контрактів для зв’язку між програмами.

Ви можете відкривати файли AIDL за допомогою Google Android Studio або будь-якого текстового редактора, наприклад Microsoft Notepad і Notepad++.

## Формат файлу AIDL - Додаткова інформація

AIDL — це текстові файли, які містять інтерфейси для зв’язку між програмами. ОС Android не дозволяє одному процесу отримувати доступ до пам’яті іншого процесу. Це призводить до того, що процеси розділяють свої об’єкти на примітиви для розуміння базової операційної системи та встановлення процесу комунікаційних структур для розробника.

### Які типи даних підтримує AIDL?

AIDL за замовчуванням підтримує такі типи даних.

* Усі примітивні типи в мові програмування Java (такі як int, long, char, boolean тощо)
* Рядок
* CharSequence
* Список
* Карта

## Приклад файлу AIDL

Нижче наведено приклад файлу AIDL.

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
## Список літератури

* [Мова визначення інтерфейсу Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

