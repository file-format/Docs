{
  "date": "2019-10-11",
  "keywords": [
"obj faylı",
"obj fayl formatı",
"obj faylı nədir",
"fayl",
"obj nümunəsi",
"obj fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBJ fayl formatı",
  "description": "OBJ fayl formatı və OBJ fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OBJ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-ob-azj"
}
},
  "lastmod": "2019-09-10"
}

## OBJ faylı nədir?

**OBJ** faylları həndəsi obyektləri müəyyən etmək və saxlamaq üçün Wavefront-un Advanced Visualizer tətbiqi tərəfindən istifadə olunur. Həndəsi məlumatların geri və irəli ötürülməsi OBJ faylları vasitəsilə mümkün olur. Nöqtələr, xətlər, faktura təpələri, üzlər və sərbəst formalı həndəsə (əyrilər və səthlər) kimi həm çoxbucaqlı həndəsə OBJ formatı tərəfindən dəstəklənir. Bu format animasiya və ya işıq və səhnələrin mövqeyi ilə bağlı məlumatları dəstəkləmir.

OBJ faylı adətən CAD (Kompüter Dəstəkli Dizayn) tərəfindən yaradılan 3D modelləşdirmə prosesinin son məhsuludur. Təpələri saxlamaq üçün standart qayda üz normallarının açıq şəkildə bəyan edilməsindən qaçınmaqla saat əqrəbinin əksinədir. OBJ faylları şərh xəttində miqyas məlumatlarını elan etsə də, OBJ koordinatları üçün heç bir vahid elan edilməmişdir.

## 3D OBJ Formatının tarixi

Wavefront Technologies created OBJ file format for its Advanced Visualizer application to store geometric objects and 3D data. Its version 2.11 is superseded by a newly documented version 3. Fayl formatı açıqdır və digər satıcılar tərəfindən 3D qrafika tətbiqi üçün tətbiq edilmişdir. Wavefront Technologies bu fayl formatını açıq mənbə və neytral saxladı.

## OBJ fayl formatı

3D obyektlərdə səth həndəsəsinin kodlaşdırılması OBJ fayl formatının çox yaxşı yerinə yetirdiyi çətin bir işdir. Bu format olduqca çox yönlüdür, çünki səth həndəsəsini kodlaşdırmaq üçün bir sıra seçimlər təklif edir. Aşağıda öz üstünlükləri və çatışmazlıqları olan üç icazə verilən format var:

### Çoxbucaqlı üzlərlə mozaika

OBJ fayl formatı istifadəçiyə sadə və ya mürəkkəb həndəsi fiqurlardan istifadə edərək 3D model səthini cızmaqda kömək edir. Modelin səth həndəsəsinin kodlaşdırılması üçün fayl hər çoxbucaqlının təpələrini və normallarını saxlayır. Mozaika modelin qabalığını artırsa da, faylın ölçüsü ilə onun çap keyfiyyəti arasında düzgün balansı tapmaq lazımdır.

### Sərbəst forma əyrisi

OBJ fayl formatı istifadəçi tərəfindən müəyyən edilmiş sərbəst formalı səth əyrilərinə modelin səthinin həndəsəsini təyin etməyə imkan verir. Sərbəst formalı əyrilər çoxbucaqlı üzlərdən daha mürəkkəb olduğundan, az riyazi parametrlərlə əyri xətlər ən yaxşı şəkildə sərbəst forma əyriləri ilə müəyyən edilə bilər. Buna görə də, çoxbucaqlı mozaiklərlə müqayisədə daha az məlumatla, fayl ölçüsünü genişləndirmədən istənilən 3D modelin yüksək keyfiyyətli kodlaşdırılmasını yaratmaq üçün sərbəst forma əyriləri istifadə olunur.

### Sərbəst formalı səthlər

OBJ fayl formatı həmçinin sərbəst formada səth yamaqları ilə səth həndəsəsinin döşənməsini müəyyən edir. Bu cür sərbəst forma səth yamaları (NURBS) yük maşınının gövdəsi, vertolyotun qanadları və ya qayığın gövdəsi kimi sərt radial ölçüləri olmayan səthlər üçün çox uyğundur. Sərbəst formalı səthlərin istifadəsi çox faydalıdır, çünki onlar fayl ölçülərini daha yüksək dəqiqliklə daha kiçik saxlamaq üçün daha dəqiqdirlər. Bu səthlər aerokosmik və avtomobil sənayesinin vacib hissəsidir, burada aşağı dəqiqlik bağışlanmazdır.

Səthin həndəsəsini müəyyən etmək üçün aşağıdakı açar sözlər məlumat növünə görə sıralanır.


|Elementlər|Sərbəst formalı əyri/səth gövdəsi ifadələri|Sərbəst formalı əyri/səth atributları
---|---|---|
|p|Nöqtə|parm|Parametr qiymətləri|deg|Derece
|l|Xətt|trim|Xarici kəsmə döngəsi|bmat|Baza matrisi
|f|Üz|deşik|Daxili kəsmə ilgəsi|addım|Addım ölçüsü
|əyri|Əyri|scrv|Xüsusi əyri|cstype|Əyri və ya səth növü
|curv2|2D curve|sp|Xüsusi nöqtə|**Səthlərin birləşdirilməsi və qruplaşdırılması**
|surf|Səth|end|Son bəyanat|connect|connect
|**Atributları göstərin/göstərin**|g|Qrup adı
|bevel|Keyif interpolyasiyası|shadow_obj|Kölgə tökmə|s|Hamiləmə qrupu
|lod|Təfərrüat səviyyəsi|trace_obj|Şüa izləmə|mg|Birləşmə qrupu
|d_interp|İnterpolyasiyanı həll et|ctech|Əyri yaxınlaşma texnikası|o|Obyekt adı
|c_interp|Rəng interpolyasiyası|stech|Səthin yaxınlaşma texnikası|
|usemtl|Material adı|mtllib|Material kitabxanası|
|**Həndəsi təpələr**|
|v|Həndəsi təpələr|vn|Vertex normalları|
|vt|Tekstura təpələri|vp|Parametr fəzasının təpələri|

### Rəng və Tekstura

OBJ faylı rəng və faktura məlumatlarını Material Şablon Kitabxanası (MTL) adlı əlaqəli fayl formatında saxlamağa imkan verir. Çox rəngli həndəsi modellər bu iki faylı birlikdə istifadə edərək göstərir. MTL faylları ASCII əsaslıdır və Phong əks etdirmə modelindən istifadə edərək səthin işığı əks etdirən xüsusiyyətlərini təsvir etməklə kompüter göstərilməsini asanlaşdırır. Standart materialların mübadiləsi üçün ondan istifadə edən çoxlu sayda proqram təminatçısı tərəfindən qəbul edilmişdir. MTL formatı, spekulyar və paralaks xəritələr kimi ən son texnologiyalarda dəstək olmadığı üçün bir qədər köhnəlmişdir.

## İstinadlar

* [Wavefront .obj faylı](https://en.wikipedia.org/wiki/Wavefront_.obj_file)


