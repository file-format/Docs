{
  "date": "2019-10-11",
  "keywords": [
"yaml",
".yaml",
"yaml faylı nədir",
"yaml faylını necə açmaq olar",
"uzadılması",
"fayl",
"yaml faylı",
"yaml fayl formatı",
".yaml uzadılması",
"yaml vs json",
"YAML fayl nümunəsi",
"docker yaml fayl nümunəsi"
],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "description": " YAML faylı yarada və aça bilən YAML fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "YAML fayl formatı",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yam-azl"
}
},
  "lastmod": "2021-05-05"
}

## YAML faylı nədir? ##

**YAML faylı** Unicode əsaslı verilənlərin seriyalaşdırma dili olan YAML (YAML İşarələmə Dili) dilindən ibarətdir; konfiqurasiya faylları, internet mesajlaşması, obyekt davamlılığı və s. üçün istifadə olunur. YAML öz faylları üçün .yaml uzantısından istifadə edir. Onun sintaksisi konkret proqramlaşdırma dilindən müstəqildir. Əsasən, YAML insanların qarşılıqlı əlaqəsi və müasir proqramlaşdırma dilləri ilə yaxşı işləmək üçün nəzərdə tutulmuşdur. İxtiyari yerli məlumat strukturlarının serializasiyasına dəstək YAML fayllarının oxunaqlılığını artırdı, lakin bu, təhlil və fayl yaratma prosesini bir qədər çətinləşdirdi.

## Qısa tarix ##

YAML ilk dəfə 2001-ci ildə təklif edilmiş və Clark Evans, Ingy döt Net və Oren Ben-Kiki tərəfindən hazırlanmışdır. YAML ilk olaraq işarələmə dili kimi məqsədini göstərmək üçün Yenə başqa İşarələmə Dili mənasını verirdi. Daha sonra məqsədini məlumat yönümlü olaraq göstərmək üçün YAML Aint Markup Language olaraq dəyişdirildi.


## YAML fayl formatı ##

YAML faylı aşağıdakı məlumat növlərindən ibarətdir

- **Skalar**: Skalarlar Sətirlər, Tam ədədlər, Booleanlar və s. kimi dəyərlərdir.
- **Ardıcıllıq**: Ardıcıllıqlar tire (-) ilə başlayan hər bir elementi olan siyahılardır. Siyahılar da yuvalana bilər.
- **Mappings**: Xəritəçəkmə düymələri dəyərlərlə siyahıya salmaq imkanı verir.

### Sintaksis ###

- **Boşluq**: Boşluq girintisi yuva və ümumi quruluşu göstərmək üçün istifadə olunur.

```yaml
adı: John Smith
əlaqə:
ev: 1012355532
ofis: 5002586256
ünvan:
küçə: |
123 Tornado Xiyabanı
Suite 16
Şəhər: East Centerville
dövlət: KS
```

- **Şərhlər**: Şərhlər # işarəsi ilə başlayır.

```yaml
# Bu YAML şərhidir
```

- **Siyahılar**: Defis (-) hər bir üzvü ayrı sətirdə siyahı üzvlərini göstərmək üçün istifadə olunur. Siyahı üzvləri həmçinin kvadrat mötərizə ([...]) içərisində vergül (,) ilə ayrılmış üzvlər daxil edilə bilər.

```yaml
  - "A"
  - "B"
  - "C"
```

```yaml
[A, B, C]
```

- **Assosiativ massiv**: Assosiativ massiv qıvrımlı mötərizələr ({...}) ilə əhatə olunub. Düymələr və dəyərlər iki nöqtə (:) ilə ayrılır və hər bir cüt vergül (,) ilə ayrılır.

```yaml
{ad: John Smith, yaş: 20}
```

- **Stringlər**: Sətir qoşa dırnaq () və ya tək dırnaq (') ilə və ya olmadan yazıla bilər.

```yaml
Nümunə sətir
"Nümunə sətir"
Nümunə sətri
```

- **Skalar Blok məzmunu**: Skalar məzmun aşağıdakılardan istifadə etməklə blok notasiyası ilə yazıla bilər:
  - "**|**: Bütün canlı fasilələr əhəmiyyətlidir."
  - "**>>**: Hər sətir fasiləsi boşluğa qatlanır. O, hər bir sətir üçün aparıcı boşluğu aradan qaldırır."

```yaml
məlumat: |
YAML
(YAML İşarələmə Dili Deyil)
verilənlərin seriyalaşdırılması dilidir
```

```yaml
məlumat: ?
YAML (YAML İşarələmə Dili Deyil)
verilənlərin seriyalaşdırılması dilidir
```

- **Birdən çox Sənəd**: Birdən çox sənədlər bir axında üç tire (---) ilə ayrılır. Defis sənədin başlanğıcını göstərir. Direktivləri sənəd məzmunundan ayırmaq üçün də defislərdən istifadə olunur. Sənədin sonu üç nöqtə (...) ilə göstərilir.

```yaml
  ---
Sənəd 1
  ---
Sənəd 2
...
```

- **Növ**: Dəyərin növünü təyin etmək üçün ikiqat nida işarələri (!!) istifadə olunur.

```yaml
a: !!float 123
b: !!küç 123
```

- **Tag**: Qeydə teq təyin etmək üçün ampersand (&) və həmin node istinad etmək üçün ulduz işarəsi (*) istifadə olunur.

```yaml
adı: John Smith
faktura: &id01
küçə: |
123 Tornado Xiyabanı
Suite 16
Şəhər: East Centerville
dövlət: KS

Göndərmə: *id01
```

- **Direktivlər**: YAML sənədləri axındakı direktivlərdən əvvəl ola bilər. Direktivlər faiz işarəsi (%) ilə başlayır, ardınca ad və sonra parametrlər boşluqlarla ayrılır.

```yaml
%YAML 1.2
  ---
Sənədin məzmunu
```
## YAML fayl nümunəsi
Burada siz aşağıda **docker yaml fayl nümunəsini** görə bilərsiniz:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Əsasən, həm JSON, həm də YAML insan tərəfindən oxuna bilən məlumat mübadiləsi formatını təmin etmək üçün hazırlanmışdır. YAML JSON formatının super dəsti kimi həyata keçirilir. Bu o deməkdir ki, biz YAML analizatorundan istifadə edərək JSON-u təhlil edə bilərik. Baxmayaraq ki, bu nəzəriyyənin praktiki tətbiqi bir az çətin olsa da. Buna görə də, YAML və JSON arasındakı bəzi əsas fərqlər aşağıda verilmişdir:

|YAML| JSON|
---|---|
|Seriallaşdırılmış məlumatların təhlili üçün mürəkkəb və vaxt aparan proses |Daha sadə dizaynı ilə JSON seriyalı verilənlərini tez və asanlıqla təhlil edin|
|Daha az icma dəstəyi| Daha böyük icma dəstəyi və populyarlıq|
|Şərhləri dəstəkləyir| Şərhləri dəstəkləmir|
|Digər məlumat obyektlərinə istinaddan istifadə etmək bacarığı| Mürəkkəb strukturları obyekt istinadları ilə seriallaşdırmaq mümkün deyil|
|İyerarxiya qoşa boşluq simvollarından istifadə etməklə işarələnir. Tab simvollarına icazə verilmir|Obyektlər və Massivlər mötərizədə və mötərizədə işarələnir.|
|String dırnaqları isteğe bağlıdır, lakin o, tək və qoşa dırnaqları dəstəkləyir.|Sətrlər cüt dırnaq içərisində olmalıdır.|
|Kök node etibarlı məlumat növlərindən hər hansı biri ola bilər|Kök node ya massiv, ya da obyekt olmalıdır.|


## İstinadlar ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

