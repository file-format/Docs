{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу PET - файл пакета встановлення Puppy Linux",
  "description":"Дізнайтеся про формат файлу PET та API, які можуть створювати та відкривати файли PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Що таке PET-файл Linux?

PET-файл — це файл інсталяційного пакета програми, створений і використаний із варіантом операційної системи Linux PuppyLinux. Він створюється як стиснутий файл [TGZ](/uk/compression/tgz/), який зменшує розмір файлу стисненого архіву. Цілісність формату файлу PET забезпечується контрольною сумою md5sum, яка додається в кінець файлу для перевірки на віддаленому кінці. Файли PET можна розпакувати за допомогою стандартного екстрактора файлів TGZ і WinRAR. Файли PET замінили старі файли встановлення пакета [PUP](/uk/compression/pup/).

## Формат файлу PET

Файли PET зберігаються на диску як стиснені архіви у двійковому форматі. Однак деталі внутрішнього формату файлу PET невідомі. Подібно до файлів встановлення пакетів [.exe](/uk/executable/exe/) і [.msi](/uk/executable/msi/), PET-файли запускають установку під час їх виконання.

## Список літератури

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Індекс PET-пакетів PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

