
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл APKS - Архів набору APK",
  "description":"Дізнайтеся, що таке файл APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Що таке файл APKS?

Файл із розширенням .apks — це архівний файл, який є колекцією файлів **APK** пакета Android. Кожен окремий файл APK у файлі APKS створюється з урахуванням різних аспектів пристроїв. До них належать архітектура, мова, щільність екрана та інші функції пристрою. Файли APKS генеруються за допомогою **bundletool**. Він використовується для створення Android App Bundle і перетворення пакету додатків у різні файли APK для розгортання на пристроях.

## Формат файлу APKS – Додаткова інформація

Файли APKS зберігаються як стиснуті файли у форматі [ZIP](/uk/compression/zip/).

## Як створити файл APKS?

Коли Android App Bundle (AAB) буде готовий, його поведінку в магазині Google Play можна перевірити для розгортання на пристрої. З цією метою файли APKS можна створити з файлів AAB і встановити на тестових пристроях за допомогою [bundletool] від Google (https://developer.android.com/tools/bundletool). Він надає інструменти командного рядка для створення файлу архіву APKS з файлів APK за допомогою наступної команди.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Щоб розгорнути файли APK на пристрої, файл APKS можна підписати за допомогою інформації про підпис пристрою, як описано нижче.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Список літератури

* [bundletool - командний рядок](https://developer.android.com/tools/bundletool)

