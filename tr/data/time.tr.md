{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME Dosyası - .time dosyası nedir? Dosyanın Linux'ta oluşturulduğu zaman",
  "description" : "TIME dosyası hakkında bilgi edinin ve dosyanın Linux'ta oluşturulduğu zamanı öğrenin",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-tr",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## TIME dosyası nedir?

TIME dosya formatı, kullanıcıların hayatlarını kaydetmelerine, organize etmelerine ve paylaşmalarına yardımcı olan LIGHT adlı bir web sistemi tarafından kullanıldı. Temel olarak, bir gönderi koleksiyonunu saklıyordu ve sistem içindeki kullanıcının yaşam sayfasındaki bir klasörü temsil ediyordu.

## Linux'ta Bir Dosyanın Ne Zaman Oluşturulduğunu Nasıl Öğrenirim?

Linux'ta bir dosyanın ne zaman oluşturulduğunu öğrenmek için 'stat' komutunu kullanabilirsiniz. Bunu nasıl yapabileceğiniz aşağıda açıklanmıştır:

Bir terminal açın ve aşağıdaki komutu yazın:

```
stat <file_path>
```

 Değiştir<file_path> ` ilgilendiğiniz dosyanın yolu ile birlikte. Örneğin:

```
stat /path/to/your/file.txt
```

Bu komut, dosya hakkında, oluşturulma zamanı da dahil olmak üzere çeşitli bilgileri görüntüler. Doğum veya Dosya: ile başlayan satırı arayın. Doğum zamanı, dosyanın dosya sisteminde ne zaman oluşturulduğunu gösterir.

İşte çıktının nasıl görünebileceğine dair bir örnek:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Bu örnekte Doğum zamanı, dosyanın ne zaman oluşturulduğunu gösterir.

