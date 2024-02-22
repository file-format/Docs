{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Дізнайтеся про формат файлу AC та API, які можуть створювати та відкривати файли ACCDB.",
  "title" : "Формат файлу AC – файл сценарію Autoconf",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-uk",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Що таке файл AC?

Файл AC — це файл сценарію Autoconf. **Autoconf** — це розширюваний пакет макросів M4, які створюють сценарії оболонки для автоматичного налаштування пакетів вихідного коду програмного забезпечення. Ці сценарії можуть адаптувати пакунки до багатьох видів UNIX-подібних систем без ручного втручання користувача. Autoconf створює сценарій конфігурації для пакета з файлу шаблону, який перераховує функції операційної системи, які може використовувати пакет, у формі викликів макросу M4.

Producing configuration scripts using Autoconf requires GNU M4. Ви повинні інсталювати GNU M4 (принаймні версію 1.4.6, хоча рекомендується 1.4.13 або пізніша версія) перед налаштуванням Autoconf, щоб сценарій налаштування Autoconf міг знайти його. Конфігураційні сценарії, створені Autoconf, є самодостатніми, тому їх користувачам не потрібно мати Autoconf (або GNU M4).

## Як відкрити файл AC?

AC означає автоматичне налаштування. Це сценарій, згенерований GNU Autoconf, який дозволяє адаптувати вихідний код програмного забезпечення до різних Posix-подібних систем шляхом перевірки необхідних функцій у пакеті. Сценарій називається файлом AC.

## Основні компоненти Autotools

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools — це набір пов’язаних пакетів, які при спільному використанні усувають багато труднощів, пов’язаних зі створенням портативного програмного забезпечення. Ці інструменти разом із кількома відносно простими вхідними файлами, що надаються вихідним потоком, використовуються для створення системи збірки для пакета.

**Базовий огляд того, як поєднуються основні компоненти autotools.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

У простому налаштуванні:

- Програма `autoconf` створює сценарій налаштування з `configure.in` або `configure.ac`.
- Програма `automake` створює Makefile.in з Makefile.am.
- Сценарій `configure` запускається для створення одного або кількох файлів Makefile з файлів Makefile.in.
- Програма `make` використовує Makefile для компіляції програми.

## Список літератури
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [Основи Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



