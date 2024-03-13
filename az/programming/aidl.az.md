{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL Faylı - Android İnterfeys Tərifi Dil Faylı",
  "description":"AIDL faylları yarada və aça bilən nümunə və API-lərlə AIDL fayl formatının nə olduğunu öyrənin.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl-az",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## AIDL faylı nədir?

AIDL (Android Interface Definition Language) faylı Android tərtibatçılarına müxtəlif proqramlar arasında əlaqə yaratmağa imkan verir. Proqramlaşdırma interfeysinə əsaslanaraq, həm müştəri, həm də xidmət proseslərarası ünsiyyətdən (IPC) istifadə etməklə əlaqə saxlamağa razılaşır. AIDL faylı bu interfeysləri və tətbiqlər arasında əlaqə üçün müqavilələri müəyyən etmək üçün [Java](/programming/java/) mənbə kodunu ehtiva edir.

AIDL fayllarını Google Android Studio və ya Microsoft Notepad və Notepad++ kimi hər hansı mətn redaktoru ilə aça bilərsiniz.

## AIDL Fayl Format - Ətraflı Məlumat

AIDL proqramlar arasında ünsiyyət üçün interfeysləri ehtiva edən mətn fayllarıdır. Android OS bir prosesin digər prosesin yaddaşına daxil olmasına icazə vermir. Bu, prosesləri əsas əməliyyat sistemini başa düşmək üçün obyektlərini primitivlərə bölməyə və tərtibatçı üçün kommunikasiya strukturları prosesini qurmağa gətirib çıxarır.

### AIDL hansı Məlumat Növlərini dəstəkləyir?

AIDL standart olaraq aşağıdakı məlumat növlərini dəstəkləyir.

 * Java proqramlaşdırma dilində bütün primitiv tiplər (məsələn, int, long, char, boolean və s.)
 * Simli
 * CharSequence
 * Siyahı
 * Xəritə

## AIDL fayl nümunəsi

Aşağıda bir nümunə AIDL faylı verilmişdir.

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
## İstinadlar

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

