{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - файл вихідного коду Matlab",
  "description":"Дізнайтеся про файл вихідного коду Matlab .m та API, які можуть створювати та відкривати файли MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - файли вихідного коду Matlab

## Що таке файл M (Matlab)?

Файл із розширенням .m — це файл вихідного коду, який використовується Matlab, платформою для програмування та числових обчислень, яка використовується для аналізу, розробки алгоритмів і імітаційного моделювання. Як і інші формати файлів програмування, файл M містить вихідний код, який виконує команди Matlab для побудови графіків, запуску моделювання та інших математичних операцій. Одна симуляція Matlab може охоплювати кілька таких файлів .m, які можуть класифікувати програму в сценаріях, класах, функціях або оголошеннях. Файли Matlab M можна відкрити будь-яким текстовим редактором.

## Формат файлу Matlab M – більше інформації

Файли Matlab .m — це текстові файли, які містять програмний код мовою програмування Matlab. Їх можна відкривати та редагувати в будь-якому текстовому редакторі, а також зберігати для виконання в програмному забезпеченні Matlab. Сам Matlab містить Live Editor, який використовується для створення сценаріїв, які є комбінацією коду, виводу та форматованого тексту.

### Функціональні файли Matlab

Як і в інших мовах програмування, ви можете створити файл .m, який містить лише визначення функції, яка виконує лише конкретне завдання. Такі файли також зберігаються з розширенням .m і реалізують функції, пов’язані лише з цією функцією.

### Приклад файлу .M

Нижче наведено приклад функціонального файлу Matlab, який обчислює час, необхідний для падіння об’єкта з висоти h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Щоб викликати цю функцію з редактора Matlab або з іншого файлу .m, можна використати наступний код.
```C++
TimeToGround(100)
```

## Список літератури

* [Matlab – підтримувані формати файлів](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Використання Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - файл реалізації Objective-C

## Що таке файл M (Objective-C)?

Файл M також називають файлом реалізації, який містить вихідний код класу, написаний мовою Objective-C, мовою програмування, яка використовується для написання програмних програм для OS X та iOS. Objective-C є основною мовою програмування, яка використовується основними API Apple, Cocoa і Cocoa Touch, для цих платформ. Один програмний додаток, розроблений цією мовою, може містити кілька файлів .m, що містять реалізацію класів програми. Їх можна відкрити за допомогою Apple XCode, jEdit та інших поширених текстових редакторів.

## Формат файлу Objective-C M – більше інформації

Файли M записуються у форматі звичайного тексту з використанням синтаксису програмування Objective-C. Кожен метод класу має бути визначений з усім необхідним кодом у цих файлах реалізації. Ці M-файли реалізації можуть імпортувати один або кілька файлів заголовків .h відповідно до вимог. Інструкція імпорту повідомляє компілятору, де знайти файл заголовка, який належить до цього файлу реалізації. Інструкція імпорту записується наступним чином.

```C++
#import "network.h"
```

Потім кожна реалізація файлу M починається з директиви @implementation, за якою йде ім’я файлу класу реалізації. Далі слідує реалізація всіх методів, оголошених у файлі заголовка.

### Приклад формату файлу M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Список літератури
* [Про Objective C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Посібник Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

