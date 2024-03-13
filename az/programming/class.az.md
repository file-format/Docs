{
  "date": "2019-10-11",
  "keywords": [
"sinif",
".sinif",
"sinif faylı nədir",
"sinif faylını necə açmaq olar",
"uzadılması",
"fayl",
"sinif faylı",
"sinif fayl formatı",
".class genişləndirilməsi",
"java-da sinif faylı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Class - Java Class Fayl Format",
  "description": "Class fayl formatı və Class faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-azs"
}
},
  "lastmod": "2020-09-10"
}

## Class faylı nədir?

Java-da **Sinif faylı**, əslində Java Virtual Maşın (JVM) tərəfindən icra edilən [.java](/programming/java/) sinifinin tərtib edilmiş çıxışıdır. Sinif faylları ayrı-ayrılıqda icra oluna bilər, həmçinin digər paket faylları ilə birlikdə paket kimi [JAR](/programming/jar/) faylının bir hissəsi ola bilər. Bunlar komanda xətti interfeysindən **`javac`** əmrindən istifadə etməklə yaradıla bilər. [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) və NetBeans kimi bəzi Java İDE-ləri layihənin Java fayllarından .class çıxış faylları yaratmağı təmin edir.

## Sinif fayl formatı

Java sinif faylı JVM tərəfindən idarə olunacaq ara kod olan bayt kodundan ibarətdir. Sinif faylı 8 bitlik bayt axınından ibarətdir və çoxbaytlı məlumat elementləri həmişə böyük-endian qaydasında saxlanılır.

### ClassFile Strukturu

Sinif fayl strukturu aşağıda göstərildiyi kimidir.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
harada:

* u1 = işarəsiz bir baytlıq kəmiyyət

* u2 = işarəsiz iki baytlıq kəmiyyət

* u4 = işarəsiz dörd baytlıq kəmiyyət


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `sehrli` - Sehrli element sinif fayl formatını müəyyən edən sehrli nömrəni təmin edir; 0xCAFEBABE dəyərinə malikdir.

* `kiçik_versiya`, `əsas_versiya` - Kiçik_versiya və əsas_versiya elementlərinin dəyərləri bu sinif faylının kiçik və əsas versiya nömrələridir.

* `constant_pool_count` - daimi_pool_count elementinin dəyəri sabit_hovuz cədvəlindəki girişlərin sayına üstəgəl birə bərabərdir. Sabit_pool indeksi uzun və ikiqat tipli sabitlər istisna olmaqla, sıfırdan böyük və daimi_hovuz_sayından kiçik olduqda etibarlı sayılır.

* `constant_pool[]` - Constant_pool müxtəlif sətir sabitlərini, sinif və interfeys adlarını, sahə adlarını və ClassFile strukturunda və onun alt strukturlarında istinad edilən digər sabitləri təmsil edən strukturlar cədvəlidir (§4.4). Hər bir daimi_pool cədvəli girişinin formatı onun ilk "teq" baytı ilə göstərilir.

* `access_flags` - access_flags elementinin dəyəri bu sinif və ya interfeysin giriş icazələrini və xassələrini göstərmək üçün istifadə edilən bayraqların maskasıdır.

* `bu_sinif` - this_class elementinin dəyəri daimi_hovuz cədvəlində etibarlı indeks olmalıdır.

* `super_sinif` - Sinif üçün super_sinif elementinin dəyəri ya sıfır olmalıdır, ya da daimi_pool cədvəlində etibarlı indeks olmalıdır.

* `interfaces_count` - interfaces_count elementinin dəyəri bu sinif və ya interfeys tipli birbaşa super interfeyslərin sayını verir.

* `interfeyslər[]` - İnterfeyslər massivindəki hər bir dəyər daimi_pool cədvəlində etibarlı indeks olmalıdır.

* `fields_count` - fields_count elementinin dəyəri sahələr cədvəlindəki field_info strukturlarının sayını verir.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `metods_count` - Methods_count elementinin dəyəri metodlar cədvəlində metod_info strukturlarının sayını verir.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `atributların_sayması` - atributların_sayı elementinin dəyəri bu sinfin atributlar cədvəlində atributların sayını (§4.7) verir.

* `atributlar[]` - Atributlar cədvəlinin hər bir dəyəri atribut_info strukturu olmalıdır.





## İstinadlar

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

