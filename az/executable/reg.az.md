{
  "date": "2021-08-02",
  "keywords": [
"reg faylı",
"reg fayl formatı",
"reg faylı nədir",
"fayl",
"reg misal",
"reg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "REG fayl formatı və REG fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "REG - Windows Qeydiyyatı Faylı",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-re-azg"
}
},
  "lastmod": "2021-08-02"
}

## REG faylı nədir?

REG faylı sadəcə olaraq .reg uzantısı olan mətn faylıdır. Bu fayllar adətən Registrydən tipik açarların ixracı ilə yaradılır. Bu fayllar reyestrin ehtiyat nüsxəsi kimi də istifadə edilə bilər (Xüsusilə bu addım dəyişikliklər etməzdən əvvəl vacibdir!). Görə bilərsiniz ki, bəziləri onları reyestr sındırmasını necə həyata keçirəcəyinizi göstərən eyni saytlarda yüklənə bilən fayllar kimi təqdim edib. REG faylı Reyestrdə əl ilə dəyişikliklər etmək və bu dəyişiklikləri ixrac etmək üçün faydalıdır. Sadəcə faylı bir az təmizləyin və sonra başqaları ilə paylaşın.

## REG fayl formatı

REG fayl formatı INI əsaslı sintaksisdən istifadə edərək Windows reyestrinin hissələrinin ixracı və idxalı üçün nəzərdə tutulmuşdur. Windows Qeydiyyatı Microsoft Windows əməliyyat sistemi və Windows reyestrindən istifadə edən digər proqramlar üçün aşağı səviyyəli parametrləri saxlayan relational və ya iyerarxik verilənlər bazasıdır. Alternativ olaraq deyə bilərik ki, reyestr və ya Windows reyestri Microsoft Windows əməliyyat sistemlərinin bütün versiyalarında quraşdırılmış proqramlar və avadanlıqlar üçün məlumat, seçimlər, parametrlər və digər dəyərlərdən ibarətdir.

### REG faylının sintaksisi
REG fayl sintaksisinin bir hissəsi kimi bəzi əsas elementlər bunlardır:
- **RegistryEditorVersion**: Məsələn, Windows 2000, Windows XP və Windows Server 2003 üçün Windows Registry Editor Version 5.00.
- **Boş xətt**: Yeni reyestr yolunun başlanğıcını müəyyən edir.
- **RegistryPathx**: Import etdiyiniz ilk dəyəri saxlayan alt açarın yolu.
- **DataItemNamex**: Import etmək istədiyiniz məlumat elementinin adı.
- **DataTypex**: Reyestr dəyəri üçün məlumat növü.

Açarlar aşağıdakı sintaksisdən istifadə edərək .reg fayllarında saxlanılır:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Siz Dəyər Adı əvəzinə @ istifadə edərək açarın Defolt Dəyərini redaktə edə bilərsiniz:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Nümunə

Budur REG faylının nümunəsi
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## İstinadlar

* [Windows Registry- Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Windows_Registry)

* [Registr alt açarlarını və dəyərləri .reg faylından istifadə etməklə necə əlavə etmək, dəyişdirmək və ya silmək olar](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- registr-alt açarları-və-dəyərlər-a-reg-fayl-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


