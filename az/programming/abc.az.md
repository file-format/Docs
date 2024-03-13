
{
  "date": "2021-12-14",
  "keywords": [
".abc faylı",
"uzadılması",
"format",
"ActionScript Bayt Kod Faylı",
".abc faylını necə açmaq olar",
"abc fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ABC - ActionScript Bayt Kod Faylı",
  "description": "ABC faylları yarada və aça bilən nümunə və API-lərlə ABC fayl formatının nə olduğunu öyrənin.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-azc"
}
},
  "lastmod": "2021-12-14"
}

## ABC faylı nədir?

.abc uzantılı fayl ActionScript skript fayllarının tərtibi nəticəsində Flash tərtibçisi tərəfindən yaradılmış ActionScript Bayt Kod Faylıdır. ABC faylında olan bayt kodu ActionScript Virtual Maşın (AVM və AVM2) tərəfindən yerinə yetirilir. Bayt kodu daimi verilənlərdən, AVM2 təlimat dəstindən olan təlimatlardan və müxtəlif növ metaməlumatlardan ibarətdir. ABC faylı AVM və ya AVM2-yə yükləndikdə, o, yoxlamadan keçir. AVM2 İcmalına uyğun gəlmirsə, rədd edilir. ABC faylları çoxdan dayandırılmış Adobe Flash Player-də açıla bilər.

## ABC Fayl Format - Ətraflı Məlumat

ABC faylları AVM və ya AVM2 virtual maşınları tərəfindən oxuna bilən ikili fayl formatında diskdə saxlanılır. Onun daxili fayl strukturu bütün daimi məlumatları, tip deskriptorları, kodu və metadata ilə icra edilə bilən kod blokunu təmsil edir.

## ABC fayl strukturu

ABC fayl strukturu aşağıda göstərildiyi kimidir.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC File Fields

|Sahənin Adı|Təsvir|
---|---|
|minor_version, major_version|Major_version və minor_version dəyərləri abcFile formatının əsas və kiçik versiya nömrələridir.|
|constant_pool|Constant_pool tam ədədlərdən, qoşalardan, sətirlərdən, ad boşluqlarından, ad məkanı dəstlərindən və çoxadlardan ibarət dəyişən uzunluqlu strukturdur.|
|metod_count, method|method_count dəyəri metod massivindəki qeydlərin sayıdır. Metod massivindəki hər bir giriş dəyişən uzunluqlu metod_info strukturudur.|
|metadata_count, metadata|Metadata_count dəyəri metadata massivindəki girişlərin sayıdır. Hər bir metadata girişi adı sətir dəyərlərinə uyğunlaşdıran metadata_infostructuredur. |
|class_count, instance, class|class_count dəyəri nümunə və sinif massivlərindəki girişlərin sayıdır. |
|script_count, script|script_count dəyəri skript massivindəki qeydlərin sayıdır. Hər bir skript girişi bu fayldakı tək skriptin xüsusiyyətlərini müəyyən edən script_info strukturudur. |
|method_body_count, method_body|metod_body_count dəyəri metod_bədən massivindəki qeydlərin sayıdır. Hər metod_bodyentry fərdi metod və ya funksiya üçün təlimatları ehtiva edən dəyişən uzunluqlu metod_body_info strukturundan ibarətdir.|

## İstinadlar

 * [Sağlam ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

