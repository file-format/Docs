{
  "date" : "2021-04-08",
  "keywords" :[ "оар файл", "оар файл формат", "какво е оар файл", "файл", "оар пример", "оар файл разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR – архивен файлов формат на OpenSimulator",
  "description":"Научете за OAR файловия формат и API, които могат да създават и отварят OAR файлове.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Какво е OAR файл?

Файл с разширение .oar е архивен файл, използван от приложението OpenSimulator, което е сървър за 3D приложения с отворен код за създаване на виртуална среда, достъпна за множество потребители по мрежата. Файловият формат OAR предоставя необходимите данни за активите, необходими за пълното зареждане на терена, текстурите на обекти и инвентара на различна система. OpenSimulator също има незадължителна хипермрежа, която позволява на потребителите да посещават други инсталации на OpenSimulator в мрежата. OAR файловете имат интернет MIME тип application/oar и съдържат един или повече архивирани файлове.


## OAR файлов формат

OAR са двоични файлове, които се съхраняват в компресиран архивен файлов формат. Най-новата версия на файловия формат OAR е [версия 1.0](http://opensimulator.org/wiki/OAR_Format_1.0), която има големи промени от предишната си [версия 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). Най-новата версия поддържа съхраняване на множество региони в един OAR и не е обратно съвместима с версии на OpenSimulator преди 0.7.5. OAR файлът е gzipped tar файл (tar.gz) в оригиналния Unix tar формат (не USTAR).

## Пример за региони на OAR
AOR файловете могат да съдържат множество региони. Структурата на архива е както следва (този пример съдържа 4 региона):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

Архивният контролен файл съдържа основен номер на версия за определяне на съвместимост с бъдещи промени на формата. Наличието на активи във формат OAR се обозначава от булевия елемент<assets_included> . Информацията за включените региони се съдържа в манифест, който присъства в контролния файл. Пример за Archive.xml е както следва.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Препратки

* [OAR Format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

