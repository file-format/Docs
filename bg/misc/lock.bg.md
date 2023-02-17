{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлов формат LOCK – Какво е файл за заключване?",
  "description":"Научете повече за файловия формат LOCK и неговите .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Какво е LOCK файл?

**LOCK** файл е преименуван файл, който се използва от приложения и операционни системи за маркиране на файл или някое устройство като заключено. Това казва на други приложения да не използват файла, освен ако не е свободен от приложението, което го използва. В повечето случаи тези заключващи файлове са празни, но в други случаи може да съдържат информация, свързана със заключването, като свойства и настройки.

Понякога .lock файлът се използва от .NET Framework на Microsoft за създаване на **заключени** копия на файл с база данни. В такъв случай копие на файла с база данни ще се отвори с разширение .lock. Това не позволява на потребителя да прави промени във файла, докато той се използва от друг потребител.

## LOCK файлов формат - повече информация

LOCK файл се създава от всяко приложение и неговият файлов формат е специфичен за приложението. Тези файлове за заключване могат да бъдат записани както в текстов, така и в двоичен файлов формат.

Наличието на заключващи файлове предотвратява едновременен достъп на ресурс до множество файлове, които се опитват да получат достъп до този ресурс. Създава се копие на оригиналния файл с разширение .lock към името му. Това казва на други приложения да имат достъп само за четене до файла. Например resource.dat ще стане resource.data.lock.

За езика за програмиране Ruby може да попаднете на файла **gemfile.lock**. Това е мястото, където Bundler съхранява точните версии, които са инсталирани. По този начин, когато проект/библиотека се премести на друга машина, работещият пакет ще търси Gemfile за точната подходяща версия.

## Заключване на файл в Linux

Linux поддържа два типа заключвания на файлове: препоръчителни заключвания и задължителни заключвания.

* **Advisory Locks**: Тип заключване, което не се прилага. В този случай участващите процеси си сътрудничат помежду си, изрично придобивайки ключалки. Ако това не е възможно, препоръчителните заключвания се игнорират.

* **Задължителни заключвания**: В случай на задължително заключване, операционната система налага заключването на файла, като не позволява на други процеси да четат или записват файла. Това не изисква никакво сътрудничество между процесите.

задължителното заключване не изисква никакво сътрудничество между участващите процеси. След като се активира задължително заключване на файл, операционната система не позволява на други процеси да четат или записват файла.

## Препратки

* [GemFile и Gemfile.lock в Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Заключване в Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)
