{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Kabuk betiği - Ubuntu ve Linux'ta nasıl çalıştırılır",
  "description":"Shell Script'in ne olduğunu ve Ubuntu ve Linux'ta nasıl çalıştırılacağını öğrenin",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-tr",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Kabuk Komut Dosyası Nedir?

Kabuk komut dosyası oluşturma, genellikle **Kabuk Komut Dosyası** olarak adlandırılan düz metin dosyasına bir dizi komut yazmayı içerir. Bu komut dosyaları, komut satırı yorumlayıcısı olan bir kabuk tarafından yürütülür. En yaygın kabuklar şunları içerir:

1. Bash (Bourne Again SHell)
2. Zsh (Z Kabuğu)
3. Balık.

Kabuk komut dosyaları basit tek satırlık programlardan karmaşık programlara kadar değişebilir ve dosya işleme, sistem yönetimi ve tekrarlanan görevlerin otomasyonu gibi çok çeşitli görevleri gerçekleştirmek için kullanılırlar.

## Shell Komut Dosyasının Faydaları:

1.  **Otomasyon:** Kabuk komut dosyaları, kullanıcıların tekrarlanan görevleri otomatikleştirmesine olanak tanıyarak zamandan tasarruf sağlar ve insan hatası olasılığını azaltır.
    
2.  **Özelleştirme:** Kullanıcılar, yüksek düzeyde özelleştirme sağlayan, kendi özel ihtiyaçlarına göre uyarlanmış komut dosyaları oluşturabilir.
    
3.  **Toplu İşleme:** Kabuk komut dosyaları, birden fazla komutun sırayla yürütülmesi gereken toplu işleme görevlerini gerçekleştirmek için mükemmeldir.
    
4.  **Sistem Yönetimi:** Kabuk komut dosyaları genellikle yedekleme, günlük döndürme ve yazılım yükleme gibi sistem yönetimi görevleri için kullanılır.

## Basit Bir Kabuk Betiği Yazmak:

Bir tebrik mesajı yazdıran temel bir kabuk komut dosyası oluşturalım. Bir metin düzenleyici açın ve greeting.sh adlı bir dosya oluşturun. Aşağıdaki satırları ekleyin:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Dosyayı kaydedin ve terminalde aşağıdaki komutu çalıştırarak yürütülebilir hale getirin:

```
chmod +x greeting.sh
```

Artık betiği çalıştırabilirsiniz:

```
./greeting.sh
```

Çıktı şöyle olmalıdır:

```
Hello, welcome to the world of shell scripting!
```

## Kabuk Komut Dosyalarını Ubuntu ve Linux'ta Çalıştırmak:

Şimdi **Ubuntu ve Linux'ta bir .sh dosyasının nasıl çalıştırılacağını** tartışacağız.

1.  **Komut Dosyasını Çalıştırılabilir Hale Getirin:** Bir kabuk komut dosyasını çalıştırmadan önce, çalıştırılabilir olduğundan emin olun. Daha önce gösterildiği gibi 'chmod' komutunu kullanın.
    
2.  **Komut Dosyası Dizinine gidin:** Bir terminal açın ve kabuk komut dosyanızı içeren dizine gitmek için cd komutunu kullanın.
    
3.  **Komut Dosyasını Çalıştırın:** Terminalde `./scriptname.sh` yazarak, scriptname yerine komut dosyanızın gerçek adını yazarak komut dosyasını çalıştırın.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Bash Komutunu Kullanma:** Komut dosyanız `#!/bin/bash` (**shebang** olarak bilinir) ile başlıyorsa, onu `bash` komutunu kullanarak da çalıştırabilirsiniz.

```
bash greeting.sh
```

## Shell Komut Dosyasında $@ ne anlama geliyor?

Kabuk komut dosyasında, `$@` komut dosyasına iletilen tüm komut satırı bağımsız değişkenlerini temsil eder. Genellikle bağımsız değişkenlerin listesine ayrı varlıklar olarak atıfta bulunmak için kullanılır. `$@` gibi çift tırnak içinde kullanıldığında, bireysel bağımsız değişkenleri korur, boşlukları ve özel karakterleri hesaba katar.

İşte kısa açıklama:

- `$@`: Komut dosyasına veya işleve iletilen tüm konumsal parametreleri (argümanları) temsil eder. Her argüman ayrı bir kelime olarak ele alınır.
    
- `$@`: Çift tırnak içine alındığında, bağımsız değişkenlerin içinde boşluklara veya özel karakterlere izin vererek bağımsız değişkenlerin ayrılmasını korur.
    

İşte açıklamak için basit bir örnek:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Bu betiği argümanlarla çalıştırdığınızda, örneğin:

```
bash example.sh arg1 "argument 2" arg3
```

Çıktısı olacaktır:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Gördüğünüz gibi, `$@` tüm bağımsız değişkenleri temsil eder ve `$@`, boşluk içerseler bile bağımsız bağımsız değişkenleri korur.

