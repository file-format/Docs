{
  "date" : "2019-10-11",
  "keywords" :[ "j2c файл", "j2c файлов формат", "какво е j2c файл", "файл", "j2c пример", "j2c файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Научете за файловия формат J2C и API, които могат да създават и отварят J2C файлове.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Какво е J2C файл?

Файл с разширение .j2c е вариант на JPEG файлов формат и е компресиран с уейвлет компресия. Той има почти идентична система от маркери и сегменти с файловия формат JPEG 2000. Файловият формат J2C е както е дефиниран в част 1 на стойката за JPEG 2000, която поддържа компресия както със загуба, така и без загуба. Кодовият поток JPEG 2000 е проектиран да бъде вграден в [JP2](/bg/image/jp2/) или друг файлов формат, въпреки че може да се появи във файл сам. J2C файл може да се отвори с помощта на Adobe Photoshop 2020, Adobe Illustrator 2020 и Corel Paintshop Pro.

## J2C файлов формат

Файловият формат J2C е същият като този на JPEG 2000, който често се записва като .jp2 и .jpc. Това кара J2C файловете да следват същия подход на кодиране на метаданни в XML формат, където стандартът 12234-1 се използва като референция между Exif таговете и XML компонентите. Той е допълнително подобрен чрез разширение JPEG 2000 част-2, което комбинира механизма за анимация и конфигурациите на кодовия поток в едно изображение. Такива файлове с разширен файлов формат се записват като [.jpx](/bg/image/jpx/).

### Оформление на JPEG2000 файл

JPEG2000 поддържа различни приложения, базирани на съответствието за разширени файлови формати. Въпреки че най-простият тип може да съдържа едно изображение, по-сложните типове могат да включват поредица от изображения, подредени едно върху друго или последователно базирани на времето.

#### JP2 кутия
Това е градивният елемент от най-високо ниво на файловия формат JP2 и съдържа полета за тип и дължина в заглавката и секция с данни. Най-забележителният тип кутия е кутията за непрекъснат кодов поток. Тази кутия съхранява в своя раздел с данни кодовия поток JPEG2000.

#### JPEG2000 CodeStream

JPEG2000 CodeStream е поредица от байтове, която е необходима за декодиране на компресираното изображение JPEG2000. В случай че файлът няма нищо друго освен този кодов поток, той се нарича необработен файл с кодов поток. Обикновено JPEG кодовият поток е прилагането на алгоритъм за компресия JPEG2000 върху изображение, въпреки че това не е единственият начин.

#### Части от плочки ####

JPEG2000 кодирано изображение е колекция от единици данни, наречени пакети. Тези пакети се поддържат в кодовия поток вътре в групи пакети, наречени части от плочки. Преди да кодира изображение, енкодерът разделя изображението на правоъгълна мрежа от блокове, наречени плочки, където всяка плочка се кодира отделно, независимо от другите плочки.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 файлов формат" >}}

## J2C компресия
JPEG 2000 използва технология за уейвлет компресия, което го прави бърз въз основа на факта, че сравнително малко пиксели се показват в какъвто и прозорец или прозорец, който зрителят показва изображението. Това може да се подчертае от факта, че само няколко мегабайта пиксели ще се появят на екрана за изображения с много голям размер (в гигабайти). Това помага за бързото извличане и изобразяване само на онази част от данните за изображението, която е необходима за попълване на пикселите на дисплея. Това също изисква високоскоростна технология за декомпресия, за да се ускори механизмът за извличане на изображения за създаване на необходимите изображения в движение.

J2C се възползва от бързата декомпресия и извлича само необходимата информация за пикселни данни, за да изобрази част от видимите изображения бързо на екраните. J2C е предназначен основно за преглед на данни, а не за тяхното редактиране.

## J2C идентификация
JPEG 2000 файловете имат сигнатурни байтове „FF 4F FF 51“.

### Типове Mime
Регистрираните Mime типове за JPEG 2000 файлове включват:
* изображение/j2c
* изображение/jpx
* изображение/jpm
* видео/mj2

## Подобрения спрямо стандарта JPEG
Подобренията спрямо стандарта JPEG включват:
* Превъзходна производителност на компресия
* Представяне с множество разделителни способности
* Прогресивно предаване по пиксел и точност на разделителната способност
* Избор на компресия без загуба или със загуба
* Устойчивост на грешки, Гъвкав файлов формат
* Поддръжка на висок динамичен диапазон
* Пространствена информация за страничен канал

## Препратки ##
* [Таубман, Дейвид; Марцелин, Майкъл (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)
