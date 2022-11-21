{
  "date" : "2022-02-17",
  "keywords" :["gpg dosyası", "gpg dosya biçimi", "gpg dosyası nedir", "dosya", "gpg örneği", "gpg dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPG Dosyası - GNU Privacy Guard Public Keyring Dosyası",
  "description":"GPG dosyası ve GPG dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## GPG dosyası nedir?

Bir GPG dosyası, GNU Privacy Guard (GnuPG) şifreleme programı tarafından kullanılan bir şifreleme/şifre çözme anahtarı dosyasıdır. GnuPC programının kendisi, RFC4880 olarak tanımlanan OpenPGP standardına dayanmaktadır ve PGP olarak da bilinir. GPG'nin modern işletim sisteminde başarılı kullanımının anahtarı, çok yönlü anahtar yönetim sistemidir. GPG'nin komut satırı yardımcı programı, diğer uygulamalarla kolayca entegre olmasını sağlar.

## GPG Dosya Biçimi

GPG dosyaları şifrelenmiş ikili dosyalar olarak kaydedilir ve elbette insanlar tarafından okunamazlar. Şifrelenmiş bir GPG dosyasının şifresini çözmek için aynı güvenli anahtarı kullanmanız gerekir. Bu dosyaların dahili dosya formatının bilinmemesinin nedeni de budur.

## Linux'ta GPG ile Dosyaları Şifreleyin ve Şifresini Çözün

GPG komut satırı yardımcı programı, Linux'ta dosyaları şifrelemek ve şifrelerini çözmek için kullanılabilir.

### Bir Dosyayı Şifreleme

Bir dosya, aşağıda gösterildiği gibi -c (oluştur) seçeneğiyle gpg komutu kullanılarak şifrelenebilir.

```
gpg -c file1.txt
```
Bu komutu çalıştırmak, orijinal 'file1.txt' dosyasının içeriğini şifrelemek için bir anahtar sözcük ister. Bu, file1.txt.gpg şifreli dosyasının oluşturulmasıyla sonuçlanır.

### Bir Dosyanın Şifresini Çözme ve Çıkarma

Şifreli bir dosyanın şifresini çözmek ve çıkartmak için aşağıdaki komut kullanılabilir.

```
gpg cfile.txt.gpg
```

## Referanslar

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

