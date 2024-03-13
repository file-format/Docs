{
  "date": "2021-04-23",
  "keywords": [
"konfiqurasiya faylı",
"konfiqurasiya faylları",
"konfiqurasiya faylı formatı",
"uzadılması",
"format",
"git konfiqurasiya faylı",
"Linux-da konfiqurasiya faylları",
"konfiqurasiya faylı nədir",
"Konfiqurasiya faylı php",
"ssh konfiqurasiya faylı nümunəsi",
"aws konfiqurasiya faylı nümunəsi",
"python config file example"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "CONFIG - Konfiqurasiya faylı",
  "description": "CONFIG nümunəsi və CONFIG faylları yarada və aça bilən API ilə CONFIG fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "CONFIG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-confi-azg"
}
},
  "lastmod": "2021-04-23"
}

## CONFIG faylı nədir?
CONFIG faylı konfiqurasiya faylı kimi tanınır; bir neçə kompüter proqramı üçün parametrləri və əsas parametrləri konfiqurasiya etmək üçün istifadə olunur. Bəzi proqramlar işə salındıqda yalnız **konfiqurasiya fayllarını** oxuyur. Digərləri vaxtaşırı dəyişikliklər üçün konfiqurasiya fayllarını yoxlayır.

## CONFIG fayl formatı
**CONFIG Fayl formatı** server prosesləri, proqram proqramları və əməliyyat sistemi parametrləri üçün istifadə olunur. Proqramçı müəyyən müddətdən sonra konfiqurasiya fayllarını təkrar-təkrar oxumaq və dəyişiklikləri cari prosesə tətbiq etmək üçün proqrama göstəriş vermək üçün kod yaza bilər. CONFIG fayl sysntax üçün qəti standartlar və ya güclü konvensiyalar yoxdur. Məsələn, Microsoft-un Web.config faylı [XML](/web/xml/) əsaslı teq dəstlərindən ibarət olan CONFIG fayl formatına aiddir; Microsoft Visual Studio və ya hər hansı digər mətn redaktoru ilə redaktə edilə bilər.

## Konfiqurasiya fayllarına nümunələr:
Konfiqurasiya faylları heç bir qaydalara, standartlara və ya konvensiyalara əməl etməklə yaradılmadığından, bu fayllar müxtəlif formatlardan istifadə etməklə yazılmış ola bilər. .config faylı XML, [JSON](/web/json/) və ya hər hansı digər formata əsaslana bilər. Aşağıda tanınmış əməliyyat sistemləri və proqram təminatı üçün konfiqurasiya fayllarının nümunələri verilmişdir:

### Linux-da konfiqurasiya faylları
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Kateqoriya|Nümunə| Şərhlər|
---|---|---|
|Fayllara giriş|/etc/host.conf|Şəbəkə domeni serverinə host adlarını necə axtarmaq lazım olduğunu bildirir.|
|Yükləmə və giriş/çıxış|/etc/rc.d/rc.local|Rəsmi deyil. rc, rc.sysinit və ya /etc/inittab.|-dan çağırıla bilər
|Fayl sistemi|/etc/mtools.conf|DOS tipli fayl sistemində bütün əməliyyatlar (mkdir, surət, format və s.) üçün konfiqurasiya.|
|Sistem administrasiyası|/etc/shells|Sistemdə mövcud olan mümkün qabıqların” siyahısını saxlayır.|
|Networking|/etc/gated.conf|Gated üçün konfiqurasiya. Yalnız qapılı demon tərəfindən istifadə olunur.|
|Sistem əmrləri|/etc/logrotate.conf|Dinamik Bağlayıcı üçün konfiqurasiya.|
|Daemons|/etc/httpd.conf|Apache, Veb server üçün konfiqurasiya faylı. Bu fayl adətən /etc.|-də olmur
|İstifadəçi proqramları| /etc/lynx.cfg| Proksi parametrləri|
### AWS CONFIG fayl nümunəsi
Tez-tez istifadə olunan konfiqurasiya parametrləri və etimadnamələri AWS CLI tərəfindən saxlanılan CONFIG fayllarında yadda saxlanıla bilər. CONFIG faylı aşağıdakı formatdan istifadə edən açıq mətn faylı olmalıdır:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG fayl nümunəsi
OpenSSH müştəri tərəfi konfiqurasiya faylı CONFIG adlanır və o, .ssh qovluğunda saxlanılır. SSH CONFIG faylı aşağıdakı strukturdan ibarətdir:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG fayl nümunəsi
Python CONFIG faylı belə görünə bilər:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## İstinadlar

 * [Linux konfiqurasiya fayllarının başa düşülməsi](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Python-da konfiqurasiya faylları](https://martin-thoma.com/configuration-files-in-python/)

