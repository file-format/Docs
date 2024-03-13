{
  "date": "2020-11-11",
  "keywords": [
"LDF",
"uzadılması",
"fayl",
"fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"Verilənlər Bazasının Faylları"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "LDF fayl formatı və LDF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "LDF - SQL Server Master verilənlər bazası fayl formatı",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-azf"
}
},
  "lastmod": "2020-08-12"
}

## LDF faylı nədir?

.ldf uzantısı olan fayl, əlaqəli verilənlər bazası idarəetmə sistemi (RDBMS) olan Microsoft SQL Server tərəfindən saxlanılan jurnal faylıdır. Əsas verilənlər bazası fayllarında ([MDF](/database/mdf/)) həyata keçirilən bütün əməliyyatlar (daxiletmə, yeniləmə, silmə kimi) LDF faylında qeyd olunur. LDF faylları istənilən verilənlər bazasının kritik komponentləridir. Sistem nasazlığı halında, log faylı verilənlər bazasını ardıcıl vəziyyətə qaytarmaq üçün istifadə olunur. Əməliyyatlar tam yerinə yetirilmədikdə, əməliyyatlar jurnalının ölçüsü arta bilər. LDF faylları Microsoft SQL Server proqram proqramı ilə açıla bilər.

## LDF faylında qeydə alınan əməliyyatlar

SQL log faylı aşağıdakı əməliyyatları qeyd edir:

 * Hər əməliyyatın başlanğıcı və sonu.

 * Hər bir məlumat məlumatının dəyişdirilməsi (daxil edin, yeniləyin və ya silin). Bu, həmçinin sistem cədvəlləri də daxil olmaqla istənilən cədvələ sistemdə saxlanılan prosedurlar və ya verilənlərin müəyyən edilməsi dili (DDL) ifadələri ilə dəyişikliklər daxildir.

 * Hər ölçü və səhifənin ayrılması və ya ayrılması.

 * Cədvəl və ya indeks yaratmaq və ya silmək.

## LDF fayl formatı

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Əməliyyatlar seriyalı şəkildə qeydə alındığından, LSN2 tərəfindən təsvir edilən dəyişiklik LSN1 jurnal qeydindən sonra həyata keçirilir. Müəyyən bir əməliyyat üçün qeydlər istifadə olunan göstəricilərdən istifadə edərək geriyə bağlanır və əməliyyatın geri qaytarılmasını sürətləndirir.
 
## İstinadlar

 * [Verilənlər Bazası Faylları və Fayl Qrupları](https://learn.microsoft.com/en-us/sql/relational-databases/database/database-files-and-filegroups?view=sql-server-ver15)
 * [Transaction Log Architecture and Management Guide](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -versiya 15)

