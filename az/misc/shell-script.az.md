{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell skripti - Onu Ubuntu və Linux-da necə işə salmaq olar",
  "description":"Shell Script-in nə olduğunu və onu Ubuntu və Linux-da necə işlətəcəyini öyrənin",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-az",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Shell Script nədir?

Shell skriptləri düz mətn faylında bir sıra əmrlərin yazılmasını əhatə edir, tez-tez **Shell Script** kimi istinad edilir. Bu skriptlər əmr xətti tərcüməçisi olan qabıq tərəfindən yerinə yetirilir. Ən çox yayılmış qabıqlara daxildir

1. Bash (Bourne Again SHell)
2. Zsh (Z Shell)
3. Balıq.

Shell skriptləri sadə bir laynerdən mürəkkəb proqramlara qədər dəyişə bilər və onlar faylların manipulyasiyası, sistemin idarə edilməsi və təkrarlanan tapşırıqların avtomatlaşdırılması kimi müxtəlif tapşırıqları yerinə yetirmək üçün istifadə olunur.

## Shell Scripting üstünlükləri:

1.  **Avtomatlaşdırma:** Shell skriptləri istifadəçilərə təkrarlanan tapşırıqları avtomatlaşdırmağa imkan verir, vaxta qənaət edir və insan xətası şansını azaldır.
    
2.  **Fərdiləşdirmə:** İstifadəçilər yüksək dərəcədə fərdiləşdirmə təmin edərək, onların xüsusi ehtiyaclarına uyğunlaşdırılmış skriptlər yarada bilərlər.
    
3.  **Batch Processing:** Shell skriptləri çoxlu əmrlərin ardıcıllıqla yerinə yetirilməli olduğu toplu emal tapşırıqlarını idarə etmək üçün əladır.
    
4.  **Sistem İdarəetməsi:** Shell skriptləri adətən ehtiyat nüsxələri çıxarmaq, jurnalın fırlanması və proqram təminatının quraşdırılması kimi sistem idarəetmə tapşırıqları üçün istifadə olunur.

## Sadə Shell Skriptinin Yazılması:

Gəlin salamlama mesajını çap edən əsas qabıq skripti yaradaq. Mətn redaktorunu açın və `greeting.sh` adlı fayl yaradın. Aşağıdakı sətirləri əlavə edin:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Terminalda aşağıdakı əmri işlətməklə faylı yadda saxlayın və icra edilə bilən hala gətirin:

```
chmod +x greeting.sh
```

İndi skripti icra edə bilərsiniz:

```
./greeting.sh
```

Çıxış belə olmalıdır:

```
Hello, welcome to the world of shell scripting!
```

## Ubuntu və Linux-da Shell Skriptlərinin işlədilməsi:

İndi biz **Ubuntu və Linux-da .sh faylını necə işlətməyi** müzakirə edəcəyik.

1.  **Skripti icra edilə bilən edin:** Qabıq skriptini işə salmazdan əvvəl onun icra edilə bilən olduğundan əmin olun. Daha əvvəl göstərildiyi kimi chmod əmrindən istifadə edin.
    
2.  **Skript Kataloquna gedin:** Terminal açın və shell skriptinizi ehtiva edən kataloqa getmək üçün `cd` əmrindən istifadə edin.
    
3.  **Skripti işə salın:** Terminalda `./scriptname.sh` yazaraq skripti icra edin, skript adını skriptinizin əsl adı ilə əvəz edin.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Bash Komandasından istifadə:** Əgər skriptiniz `#!/bin/bash` (**shebang** kimi tanınır) ilə başlayırsa, siz onu `bash` əmrindən istifadə etməklə də işlədə bilərsiniz.

```
bash greeting.sh
```

## Shell Script-də $@ nə deməkdir?

Shell skriptində `$@` skriptə ötürülən bütün əmr xətti arqumentlərini təmsil edir. Tez-tez arqumentlərin siyahısına ayrı-ayrı obyektlər kimi istinad etmək üçün istifadə olunur. `$@` kimi qoşa dırnaq içərisində istifadə edildikdə, boşluqları və xüsusi simvolları nəzərə alaraq fərdi arqumentləri qoruyur.

Qısa izahat budur:

- `$@`: Skript və ya funksiyaya ötürülən bütün mövqe parametrlərini (arqumentləri) təmsil edir. Hər bir arqument ayrı söz kimi qəbul edilir.
    
- `$@`: İki dırnaqla işarələndikdə, ayrı-ayrı arqumentlərdə boşluqlara və ya xüsusi simvollara icazə verməklə arqumentlərin ayrılmasını qoruyur.
    

Təsvir etmək üçün sadə bir nümunə:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Bu skripti arqumentlərlə işlətdiyiniz zaman, məsələn:

```
bash example.sh arg1 "argument 2" arg3
```

Bu çıxış edəcək:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Gördüyünüz kimi, `$@` bütün arqumentləri təmsil edir və `$@` fərdi arqumentləri, hətta boşluqlardan ibarət olsa belə, saxlayır.

