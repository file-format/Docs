{
  "date": "2023-06-12",
  "keywords": [
"bak",
"bak faylı",
"Microsoft SQL Server verilənlər bazasının ehtiyat nüsxəsi",
"bak faylı nədir",
"bak faylını necə açmaq olar",
"fayl",
"bak fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BAK Fayl Format - Microsoft SQL Server verilənlər bazasının ehtiyat nüsxəsi",
  "description": "BAK faylları yarada və aça bilən BAK SQL Server Yedəkləmə formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "BAK SQL Server",
  "menu": {
    "docs": {
      "identifier": "database-bak-sqlserver-az",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## BAK faylı nədir?

Microsoft SQL Server kontekstində .bak faylı SQL Server verilənlər bazasının surətlərini saxlamaq üçün istifadə olunan ehtiyat fayl formatıdır. Bu fayllarda verilənlər bazasının müəyyən bir vaxtda təsviri, o cümlədən onun sxemi, verilənləri və digər əlaqəli məlumatlar var. Onlar SQL Serverin daxili ehtiyat nüsxəsindən istifadə edərək yaradılır və funksionallığı bərpa edir və bir neçə mühüm məqsədlərə xidmət edir:

1. **Data Recovery:** .bak faylları məlumat itkisi, korrupsiya və ya digər məsələlər halında verilənlər bazasını bərpa etmək üçün vasitə təmin edir. .bak faylından verilənlər bazasını bərpa etməklə siz onu əvvəlki vəziyyətinə qaytara, dayanma müddətini və məlumat itkisini minimuma endirə bilərsiniz.

2. **Miqrasiya və Klonlaşdırma:** Yedəkləmə faylları çox vaxt verilənlər bazalarını serverlər arasında köçürmək və ya sınaq, inkişaf və ya hesabat məqsədləri üçün verilənlər bazalarının surətlərini yaratmaq üçün istifadə olunur. Onlar verilənlər bazalarını mühitlər arasında köçürmək üçün ardıcıl və səmərəli yol təklif edirlər.

3. **Point-in-Time Recovery:** SQL Server sizə .bak fayllarından istifadə edərək vaxt ərzində bərpanı həyata keçirməyə imkan verir. Bu o deməkdir ki, siz tənzimləyicilərə uyğunluq və ya məlumatların auditi üçün vacib ola bilən verilənlər bazasını müəyyən bir vaxta bərpa edə bilərsiniz.

4. **Fəlakətin Bərpası:** .bak faylları fəlakətin bərpasının planlaşdırılmasının mühüm hissəsidir. Onlar məlumatlarınızın təhlükəsiz olmasını və avadanlıqların nasazlığı, təbii fəlakətlər və ya digər fəlakətli hadisələr zamanı tez bərpa oluna biləcəyini təmin edir.

## SQL Serverdə .BAK faylı yaradın

SQL Serverdə .bak faylı yaratmaq üçün siz adətən SQL Server Management Studio (SSMS) və ya Transact-SQL (T-SQL) əmrlərindən istifadə edirsiniz. T-SQL istifadə edərək verilənlər bazası ehtiyat nüsxəsini necə yarada biləcəyinizin sadələşdirilmiş nümunəsidir:

```
BACKUP DATABASE YourDatabaseName
TO DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## SQL Serverdə .BAK faylını bərpa edin

.bak faylından verilənlər bazasını bərpa etmək üçün siz DATABASE RESTORE əmrindən istifadə edə bilərsiniz:

```
RESTORE DATABASE YourRestoredDatabaseName
FROM DISK = 'C:\Path\To\Your\BackupFile.bak'
```

## SQL Serverdə BAK faylını necə açmaq olar?

.bak faylında saxlanılan məlumatları açmaq və onlara daxil olmaq üçün siz adətən onu Microsoft SQL Server nümunəsinə bərpa etməlisiniz. SQL Server Management Studio (SSMS) istifadə edərək .bak faylını açmaq üçün ümumi addımlar bunlardır:

1. **SQL Server Management Studio-nu işə salın**: Kompüterinizdə SSMS açın. Siz onu adətən Başlat Menyunuzda və ya SQL Server Management Studio axtarışında tapa bilərsiniz.

2. **SQL Server Nümunəsinə qoşulun**: SSMS-də verilənlər bazasını bərpa etmək istədiyiniz SQL Server nümunəsinə qoşulun. Bu əməliyyatı yerinə yetirmək üçün lazımi icazələrə ehtiyacınız olacaq.

3. **Verilənlər bazasını bərpa edin**:

a. Sol tərəfdəki Object Explorer panelində SQL Server nümunəsini genişləndirin.

b. Məlumat bazaları qovşağını genişləndirin.

c. Verilənlər bazaları üzərinə sağ vurun və Verilənlər bazasını bərpa et seçin.

4. **Mənbə və təyinatı göstərin**:

a. Verilənlər bazasını bərpa et” informasiya qutusunun Ümumi” səhifəsində Verilənlər bazasına” sahəsinə yeni verilənlər bazası üçün ad daxil edin. Bu bərpa edilmiş verilənlər bazasının adı olacaq.

b. Mənbə bölməsində ehtiyat media növü kimi Cihaz seçin.

c. Bərpa etmək istədiyiniz .bak faylına baxmaq üçün Cihaz sahəsinin yanındakı ... düyməsini basın.

d. Açmaq istədiyiniz .bak faylını seçin və OK düyməsini basın.

5. **Bərpa Seçimləri**: Lazım olduqda bərpa seçimlərini nəzərdən keçirin və konfiqurasiya edin. Mövcud verilənlər bazasının üzərinə yazılmağı, bərpa seçimlərini təyin etməyi və s. təyin edə bilərsiniz. Bu seçimləri tələblərinizə uyğun olaraq təyin etdiyinizə əmin olun.

6. **Bərpa etməyə başlayın**: Bərpa seçimlərini konfiqurasiya etdikdən sonra Verilənlər Bazasını Bərpa et dialoq qutusunda OK düyməsini klikləyin. SQL Server bərpa prosesinə başlayacaq.

7. **Bərpa edilmiş verilənlər bazasına daxil olun**: Uğurlu bərpadan sonra siz hər hansı digər verilənlər bazası kimi SQL Server Management Studio-da bərpa edilmiş verilənlər bazasına daxil ola bilərsiniz. Siz verilənlər bazası daxilində sorğular keçirə, cədvəllərə baxa və verilənlərlə işləyə bilərsiniz.

## Digər BAK faylları

**.bak** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Verilənlər bazası**
- [BAK - Database Backup File](/database/bak/)
- [BAK - Swiftpage Act! Database Backup](/database/bak-act/)

**Oyun**
- [BAK - Terraria World or Player Backup](/game/bak-terraria/)

**Müxtəlif**
- [BAK - Backup File](/misc/bak-backup/)
- [BAK - Chromium Bookmarks Backup](/misc/bak-chromium/)
- [BAK - Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK - MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Backup](/misc/bak-vegas/)

**Parametrlər**
- [BAK - Holo Launcher Backup](/settings/bak-holo/)

## İstinadlar
* [Backup and restore a SQL Server database with SSMS](https://learn.microsoft.com/en-us/sql/relational-databases/backup-restore/quickstart-backup-restore-database?view=sql-server-ver16&tabs=ssms)
