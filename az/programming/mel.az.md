{
  "date": "2019-10-11",
  "keywords": [
".mel",
"Maya daxil edilmiş dil",
"fayl",
"uzadılması",
"fayl formatı",
"Maya 3D",
"Proqramlaşdırma bələdçisi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MEL - Maya Gömülü Dil Fayl Formatı",
  "description": "MEL faylları yarada və aça bilən MEL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "MEL",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-me-azl"
}
},
  "lastmod": "2021-03-08"
}

## MEL faylı nədir?

.mel (Maya Embedded Language) uzantısına malik fayl Autodesk Maya tərəfindən qrafik interfeyslər yaratmaq üçün istifadə edilən skript dilidir. O, Maya qrafik interfeysinə əlavə olaraq icra edilə bilən skriptlərdən istifadə edərək qrafik elementlərin yaradılmasını avtomatlaşdırmağa imkan verir. MEL sizə proqramlaşdırmanı öyrənmədən qrafik interfeyslər yaratmağa imkan verir. Bu, təkrarlanan tapşırıqları sürətləndirən makrolar və xüsusi hərəkətlər yaratmaqla əldə edilir. Bu prosedurlar və skriptlər sizə fərdi modelləşdirmə, animasiyalar, dinamika və tapşırıqların göstərilməsini yaratmağa imkan verir. Autodesk Maya 2020 EML faylının məzmununu açmaq və baxmaq üçün istifadə edilə bilər.

## MEL Fayl Format - Ətraflı Məlumat

Proqramçı [reference manual](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) Maya'nın sənədlər bölməsində tərtibatçılar üçün əlçatandır. MEL şeylərə nail olmaq üçün UINX-ə bənzər qabıq skript əmrlərinə əsaslanır. Skriptə əsaslanan əmrlər onu adi və obyekt yönümlü proqramlaşdırmaya (OOP) aidiyyatsız edir, nəticədə məlumat strukturlarından, zəng funksiyalarından və ya digər dillərdə olduğu kimi OOP-dan istifadə edilmir.

MEL haqqında bəzi əsas məqamlar aşağıdakılardır.

`Şərhlər` - MEL-də hər bir ifadə blokun sonunda olsa belə, nöqtəli vergül (;) ilə bitməlidir.

`Dəyərlərin qaytarılması` - Dəyəri qaytaran ifadənin bildirilməsi dəyəri avtomatik olaraq MEL-də çap etmir. Bunun əvəzinə xətaya səbəb olur.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Yaratmaq, Redaktə etmək və Silmək üçün əmrlər` - Eyni əmr əşyalar yaratmaq, redaktə etmək və ya mövcud şeylər haqqında məlumatı sorğulamaq üçün istifadə olunur. Bununla belə, bayraq əmrin nə etdiyini (yaratmaq, redaktə etmək və ya sorğu etmək) idarə edir.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Funksiyadan Dəyəri qaytarın` - Funksiya sintaksisi avtomatik olaraq dəyəri qaytarır. Komanda sintaksisindən istifadə edərək qaytarılan dəyər əldə etmək üçün əmri əks dırnaqlara daxil etməlisiniz.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## İstinadlar

 * [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

