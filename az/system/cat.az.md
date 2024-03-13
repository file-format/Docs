{
   "date":"2023-07-06",
   "keywords":[
"CAT",
"CAT faylı",
"CAT Windows",
"fayl",
"cat fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CAT Fayl Format - Windows Kataloq Faylı",
   "description":"CAT faylları yarada və aça bilən CAT formatı və API-lər haqqında məlumat əldə edin.",
   "linktitle":"CAT",
   "menu":{
      "docs":{
         "identifier":"system-cat-az",
         "parent":"system"
}
},
   "lastmod":"2023-07-06"
}

## CAT faylı nədir?

.cat faylı kimi tanınan Windows Kataloq Faylı müxtəlif faylların bütövlüyünü və həqiqiliyini təmin etməklə Windows əməliyyat sistemində mühüm rol oynayır. Əsasən, o, kataloqlaşdırdığı faylların kriptoqrafik hash dəyərlərini, eləcə də etibarlı orqandan rəqəmsal imzanı ehtiva edən rəqəmsal imzalanmış fayl kimi xidmət edir.

.cat faylının əsas məqsədi quraşdırma zamanı və ya sistem işləyərkən sistem fayllarının, sürücülərin və ya proqram komponentlərinin yoxlanılmasını təmin etməkdir. Siz sürücünü və ya proqram paketini quraşdırdığınız zaman Windows müvafiq .cat faylının rəqəmsal imzasını yoxlayır ki, istinad etdiyi faylların imzalandığı vaxtdan onlara müdaxilə olunmayıb və ya dəyişdirilməyib. .cat fayllarından istifadə etməklə, Windows faylların həqiqiliyini yoxlaya və hər hansı icazəsiz dəyişiklikləri aşkarlaya bilər. Bu təhlükəsizlik tədbiri Windows sistemində potensial zərərli və ya təhlükəyə məruz qalmış faylların quraşdırılmasının və ya icrasının qarşısını alır.

## Windows-da CAT

**Windows-da CAT əmri** mətn faylının məzmununu birbaşa əmr sorğusu pəncərəsində göstərmək üçün istifadə olunur. Bununla belə, doğma Windows əmr sorğusuna Unix əsaslı sistemlərdə olduğu kimi daxili pişik əmri daxil deyil.

Windows-da oxşar funksiyaya nail olmaq üçün yazın əmrindən istifadə edə bilərsiniz. Windows CMD-də type əmrindən necə istifadə olunacağına dair nümunə:

```
C:\>type filename.txt
```

filename.txt faylını göstərmək istədiyiniz mətn faylının faktiki yolu və adı ilə əvəz edin. Komanda faylın məzmununu birbaşa əmr satırı pəncərəsində çıxaracaq.

Alternativ olaraq, PowerShell-dən istifadə edirsinizsə, o, Məzmun əldə et əmri üçün pişik ləqəbini ehtiva edir. Budur bir nümunə:

```
PS C:\>cat filename.txt
```

Yenə də filename.txt yerini göstərmək istədiyiniz mətn faylının yolu və adı ilə əvəz edin.

Nəzərə alın ki, siz ikili fayllar və ya qeyri-mətn məzmunu ilə işləyirsinizsə, növ və ya pişik əmrindən istifadə mənalı nəticələr verə bilməz, çünki onlar əsasən mətn fayllarını göstərmək üçün nəzərdə tutulub.

## Unix komanda pişiyinin Windows ekvivalenti nədir?

Windows-da tip əmri yuxarıda qeyd edildiyi kimi Unix-də pişik əmrinə bərabərdir.

## Windows-da CAT əmrini simulyasiya etmək üçün PowerShell-dən istifadə edin

**Cat əmri standart olaraq Windows əmr sorğusuna (CMD) və ya PowerShell-ə uyğun deyil. Bununla belə, siz PowerShell-də `Get-Content` cmdletindən istifadə edərək oxşar funksionallığa nail ola bilərsiniz.** Budur bir nümunə:

```
Get-Content C:\Path\To\File.txt
``` 

Bu əmr göstərilən faylın məzmununu göstərəcək (bu misalda `File.txt`). Bir neçə faylın məzmununu birləşdirmək və göstərmək istəyirsinizsə, bir neçə fayl yolunu təmin edə bilərsiniz:

```
Get-Content C:\Path\To\File1.txt, C:\Path\To\File2.txt
```

Əgər siz hələ də Windows-da pişik” əmri ilə daha Unix-ə bənzər təcrübəyə üstünlük verirsinizsə, Windows-da Unix-ə bənzər mühiti təmin edən və pişik” daxil edən **Cygwin və ya Git Bash** kimi üçüncü tərəf alətlərindən istifadə edə bilərsiniz. ` əmri.

**Additionally, starting with Windows 10 version 1903 (May 2019 Update), you can enable the Windows Subsystem for Linux (WSL) and use Linux commands, including `cat`.** To do this, follow these steps:

1.  PowerShell-i Administrator olaraq açın və WSL-i aktivləşdirmək üçün aşağıdakı əmri işlədin:
    
`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsistem-Linux /all /norestart`
    
2.  Virtual Maşın Platforması funksiyasını aktivləşdirin:
    
`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`
    
3.  Microsoft Mağazasından (məsələn, Ubuntu) Linux paylanması quraşdırın.
    
4.  Linux paylamanızı qurun (istifadəçi hesabı və parol yaradın).
    
5.  Quraşdırılmış Linux paylanmasını (məsələn, Ubuntu) açın və adi Linux mühitində olduğu kimi `cat` əmrini işlədin.

## CAT faylının formatı nədir?

İkili


