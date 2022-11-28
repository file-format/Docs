{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла PET — файл установочного пакета Puppy Linux",
  "description":"Узнайте о формате файла PET и API, которые могут создавать и открывать файлы PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
"идентификатор":"сжатие-питомец",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Что такое файл Linux PET?

Файл PET представляет собой файл пакета установки приложения, созданный и используемый с вариантом операционной системы Linux PuppyLinux. Он создается в виде сжатого файла [TGZ](/ru/compression/tgz/), что уменьшает размер файла сжатого архива. Целостность формата файла PET обеспечивается контрольной суммой md5sum, которая добавляется в конец файла для проверки на удаленном конце. Файлы PET можно извлечь с помощью стандартного экстрактора файлов TGZ и WinRAR. Файлы PET заменили старые установочные файлы пакета [PUP](/ru/compression/pup/).

## Формат файла ПЭТ

Файлы PET сохраняются на диск в виде сжатых архивов в двоичном формате. Однако детали внутреннего формата файла PET неизвестны. Подобно файлам установки пакетов [.exe](/ru/executable/exe/) и [.msi](/ru/executable/msi/), файлы PET запускают установку при запуске.

## использованная литература

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Указатель пакетов PuppyLinux PET] (https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)
