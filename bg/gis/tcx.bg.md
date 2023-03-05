{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TCX файлов формат – XML файл на център за обучение",
  "description":"Научете за файловия формат TCX и API, които могат да създават и отварят TCX файлове.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Какво е TCX файл?

TCX (Training Center XML) файл е формат за обмен на данни, използван за споделяне на данни между фитнес устройства. Той беше представен през 2008 г. с продукта на Garmin Training Center. Данни за тренировка, като пулс, каданс на бягане, каданс на велосипед, калории и време за обиколка, се съхраняват във формат [XML](/bg/web/xml/) във файла TCX. В допълнение, обобщените данни за тренировъчната писта също са включени в TCX файла. TCX файловете са подобни на [FIT](/bg/gis/fit/) файлове, които се създават със спортни носими устройства Garmin.

## TCX файлов формат - повече информация

TCX файловете се записват на диск като XML файлове, като всеки запис се записва като дейност. Дейността включва всички данни от тренировка като време, време на обиколка, Id, сърдечен ритъм, интензивност, каданс и информация за песента, която съдържа двойките позиции заедно с клеймото за време за тази шир-дълга позиция, подобно на [GPX](/bg/gis/gpx/) файлове.

### Версии на файлов формат TCX

Има две версии на този формат със собствени XML схеми, хоствани от Garmin. Следват няколко от тях:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX протокол за данни

Бърза версия на TCX XML формат е достъпна в Github като [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Препратки ##

* [Център за обучение XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

