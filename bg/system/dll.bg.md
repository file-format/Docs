{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "разширение", "файл", "формат", "система", "Библиотека с динамични връзки", "настройки", "програми", "компютър", "приложение" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - библиотека с динамични връзки",
  "description":"Научете за DLL файловия формат и API, които могат да създават и отварят DLL файлове.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Какво е DLL файл? ##

DLL файл или Dynamic Link Library е вид изпълним файл. Това е един от най-често срещаните разширения на вашето устройство и обикновено се съхранява в папката System32 на вашия Windows. Файлът с разширение DLL е разработен от Microsoft и се използва широко от тях. Има висока потребителска оценка за популярност. DLL работи като рафт, който съдържа *драйверите/процедурите/функциите/свойствата*, които са проектирани и приложени за програма/приложение от сървъра на Windows. Единичен DLL файл може също да се споделя между различни Windows програми. Тези файлове с разширения са жизненоважни за безпроблемната работа на Windows програмите на вашето устройство, тъй като те са отговорни за активирането и изпълнението на различни функции на програмата, като писане и четене на файлове, свързване с други устройства, които са външни за вашата настройка.
Тези файлове обаче могат да бъдат отворени само на устройство, което поддържа всяка версия на Windows (windows 7/windows 10/и т.н.) и следователно не могат да бъдат отворени директно на устройство, което поддържа Mac OS. (Ако искате да отворите DLL файл на Mac OS, различни външни приложения могат да ви помогнат да ги отворите.)


## DLL файлов формат ##

DLL файлът е разработен от Microsoft и има разширението ".dll", което представлява типа. Той е бил неразделна част от сървъра на Windows 1.0 и извън него. Това е тип двоичен файл и се поддържа от всички версии на Microsoft Windows. Този тип файл е създаден като средство за създаване на споделена библиотечна система в програмите на Windows, за да позволи отделни и независими редакции или промени в програмните библиотеки без необходимост от повторно свързване на програмите.


## DLL пример ##

Примерен код за входна точка на DLL може да бъде намерен по-долу:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Референция ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)