{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "файл", "розширення", "формат файлу", "C++", "Мова програмування" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - файл вихідного коду C++",
  "description":"Дізнайтеся про формат файлу CPP та API, які можуть створювати та відкривати файли CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл C++?

Файли з розширенням CPP є файлами вихідного коду програм, написаних мовою програмування C++. Один проект C++ може містити більше одного файлу CPP як вихідний код програми. Такий проект складається з різних типів файлів, з яких файли CPP відомі як файли реалізації, оскільки вони містять усі визначення методів, оголошених у файлі заголовка (.h). Проект C++ у цілому призводить до виконуваної програми, коли її компілюють як ціле.

## Структура файлу CPP

Структура файлу CPP проста порівняно з файлами заголовків. Основна мета такого файлу реалізації полягає в тому, щоб відокремити інтерфейс від реалізації. Це призводить до оголошення всіх функцій-членів у файлі заголовка та їхніх деталей у файлі CPP. Файл реалізації CPP можна використовувати як простий файл для написання програми або як реалізацію класу.

### Незалежне впровадження

Файл CPP при використанні як незалежної програми може містити всі реалізації всередині нього без вимоги оголошення методів у файлі заголовка. Така реалізація складається з усіх методів, визначених у файлі реалізації, де запис програми регулюється основним методом, який приймає необов’язкові дані користувача як аргументи. Він також може містити будь-які бібліотеки зі стандартної бібліотеки C++ для використання будь-якими оголошеними методами у файлі.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Реалізація класу

В об’єктно-орієнтованому програмуванні (ООП) файл CPP використовується як визначення класу. У такому випадку всі члени даних класу та функції-члени оголошуються всередині файлу заголовка. Кожен заголовний файл, у свою чергу, також може мати посилання на стандартні методи бібліотеки. Файл визначення класу CPP посилається на файл заголовка в операторі включення на початку файлу. Здебільшого розробники програмного забезпечення додають коментарі на початку такого файлу реалізації класу, які надають інформацію про фактичний вміст файлу, відомості про автора та дату впровадження. У таких випадках файли реалізації заголовків повинні мати однакові імена. Нижче наведено приклад такого файлу заголовка та реалізації.

### Файл заголовка

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### Файл реалізації CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Список літератури

* [Реалізація класу - Вікіпедія](https://en.wikipedia.org/wiki/Class_implementation_file)
