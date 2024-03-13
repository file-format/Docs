{
   "date":"2023-10-11",
   "keywords":[
"mtl",
"mtl faylı",
"mtl obj material şablon kitabxana faylı",
"mtl faylını necə açmaq olar",
"fayl",
"mtl fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"MTL Fayl Format - OBJ Material Şablon Kitabxana Faylı",
   "description":"MTL OBJ Material Şablon Kitabxanası fayl formatı və MTL faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl-az",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## MTL faylı nədir?

**Material Şablon Kitabxanası** üçün qısaldılmış MTL faylı 3D kompüter qrafikası və modelləşdirmədə istifadə olunan köməkçi fayl formatıdır. O, tez-tez 3D modelləri və onlarla əlaqəli materialları və fakturaları saxlamaq üçün ümumi format olan **Wavefront OBJ fayl formatı** ilə əlaqələndirilir.

## MTL fayl formatı

**MTL fayl formatı** 3D kompüter qrafikası ilə əlaqələndirilir və tez-tez OBJ (Wavefront .obj) fayl formatı ilə birlikdə istifadə olunur. OBJ faylları 3D həndəsəsini, MTL faylları isə əlaqəli OBJ faylları üçün material xüsusiyyətlərini müəyyənləşdirir.

MTL faylının sadə bir nümunəsidir:

```
newmtl MaterialName
Ka 0.6 0.6 0.6    # Ambient color
Kd 0.8 0.8 0.8    # Diffuse color
Ks 1.0 1.0 1.0    # Specular color
Ns 100            # Shininess
d  1.0            # Dissolve (transparency)
map_Kd texture.jpg  # Diffuse texture map
```

Bu misalda:

- `Ka` mühit rəngini təmsil edir.
- `Kd` diffuz rəngi təmsil edir.
- `Ks` spekulyar rəngi təmsil edir.
- `Ns` parlaqlığı təmsil edir.
- `d` həlli (şəffaflığı) ifadə edir.
- `map_Kd` diffuz faktura xəritəsini təyin edir.

Bu material xassələri müvafiq OBJ faylında müəyyən edilmiş 3D modelin müxtəlif hissələrinə tətbiq oluna bilər.

**MTL faylı isteğe bağlıdır və OBJ faylları əlaqəli MTL faylları olmadan istifadə edilə bilər**. Bununla belə, MTL fayllarından istifadə səthin xüsusiyyətlərini və teksturalarını təyin etməklə 3D modellərin daha ətraflı və real şəkildə göstərilməsinə imkan verir.

## Material Şablon Kitabxanası

MTL faylları haqqında vacib məlumatlar:

1.  **Material Tərifləri**: .mtl faylı müvafiq OBJ faylında 3D obyektlərə tətbiq olunan materiallar üçün tərifləri ehtiva edir. Hər bir material tərifi rəng, parlaqlıq, şəffaflıq və faktura xəritələri kimi müxtəlif xüsusiyyətləri müəyyən edir.
    
2.  **Mətn Əsaslı Format**: .mtl faylları adətən düz mətn fayllarıdır, yəni mətn redaktoru ilə asanlıqla redaktə edilə bilər. Hər bir maddi tərif ifadələr toplusundan ibarətdir və bu ifadələr materialın atributlarını müəyyən edir.
    
3.  **Texture Xəritəçəkmə**: .mtl faylının əsas funksiyalarından biri fakturaların (şəkil fayllarının) 3D modelin səthlərinə necə uyğunlaşdırıldığını müəyyən etməkdir. O, faktura faylının yolunu və onun necə bükülməli və ya modelə tətbiq edilməli olduğunu müəyyən edir.
    
4.  **Misal MTL İfadələri**: Budur, .mtl faylında tapa biləcəyiniz bəzi nümunə ifadələri:
    
- `newmtl MaterialName`: Bu, MaterialName adı ilə yeni materialı müəyyən edir.
- `Ka rgb`: Materialın mühit rəngi, RGB dəyərlərində göstərilmişdir.
- `Kd rgb`: RGB dəyərlərində göstərilən materialın diffuz rəngi.
- `Ks rgb`: RGB dəyərlərində göstərilən materialın spekulyar rəngi.
- `Ns dəyəri`: Materialın parlaqlığı və ya eksponenti.
- `map_Kd texturefile.jpg`: Material üçün diffuz faktura xəritəsini təyin edir.
5.  **Birdən çox Material**: OBJ faylı birdən çox materiala istinad edə bilər və hər bir material .mtl faylı daxilində müəyyən edilir. Bu, müxtəlif hissələrə tətbiq olunan müxtəlif materiallarla mürəkkəb 3D modellər yaratmağa imkan verir.
    
6.  **Uyğunluq**: .mtl faylları 3D modelləşdirmə proqramı və göstərmə mühərrikləri tərəfindən geniş şəkildə dəstəklənir, bu da 3D modelləri və onların materiallarını müxtəlif proqram tətbiqləri arasında ötürməyə imkan verir.

## MTL faylını necə açmaq olar?

MTL faylı mətn əsaslı fayllardır, ona görə də onlar daxil olmaqla istənilən mətn redaktoru ilə açıla bilər

- Notepad (Windows)
- Notepad++ (Windows)
- Visual Studio Kodu
- Möhtəşəm Mətn
- Atom
- TextEdit (macOS)

MTL fayllarını açan və ya istinad edən proqramlar daxildir

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

## İstinadlar
* [Wavefront .obj faylı](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


