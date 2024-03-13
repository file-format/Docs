{
  "date": "2023-03-01",
  "keywords": [
"çip faylı",
"çip faylı nədir",
"fayl",
"çip faylını necə açmaq olar",
"chip fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CHIP Fayl Format - Mikroarray Annotasiya Faylı",
  "description": "CHIP fayl formatı və CHIP faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip-az",
      "parent": "spreadsheet"
}
},
  "lastmod": "2023-03-01"
}

## CHIP faylı nədir?

CHIP faylı mikroarray annotasiya faylıdır və Gene Set Enrichment Analysis (GSEA) proqramı ilə bağlıdır. GSEA əvvəlcədən təyin edilmiş genlər dəstinin (gen dəsti) sağlam və xəstə toxuma və ya dərmanla müalicə olunan və müalicə olunmamış hüceyrələr kimi iki bioloji vəziyyət arasında statistik əhəmiyyətli fərqlər göstərib-göstərmədiyini qiymətləndirən hesablama üsuludur. GSEA-nı yerinə yetirmək üçün sizə gen ifadəsi verilənlər bazası və gen dəsti verilənlər bazası lazımdır. Gen dəsti verilənlər bazası gen dəstlərindəki genlər haqqında, məsələn, onların funksiyası, keçdiyi yol və ya toxuma spesifik ifadəsi kimi məlumatları ehtiva edir.

A CHIP file is a specific type of gene set database that is used by GSEA. It contains information about the genes and gene sets that are relevant to the microarray platform being used in the experiment. The CHIP file provides annotations for each probe on the microarray, such as the gene symbol, gene name, gene description, and chromosomal location. This information is used to match the probes with the genes in the gene expression dataset and to assign them to the appropriate gene sets for GSEA analysis.

GSEA-da CHIP faylından istifadə etmək üçün onu proqram təminatına idxal etməli və onu mikroarray verilənlər bazası ilə əlaqələndirməlisiniz. GSEA müxtəlif mikroarray platformalarını dəstəkləyir və onların bir çoxu üçün əvvəlcədən qurulmuş CHIP faylları təmin edir. Bununla belə, siz NCBI və ya Ensembl kimi xarici mənbələrdən annotasiya verilənlər bazalarından istifadə edərək öz CHIP faylınızı da yarada bilərsiniz.

## Ətraflı Məlumat

CHIP faylı elektron cədvəl deyil, lakin o, Microsoft Excel və ya Google Cədvəl kimi elektron cədvəl proqramında açıla və redaktə edilə bilər. CHIP faylı, baxmaq və redaktə etmək üçün asanlıqla elektron cədvəl proqramına idxal edilə bilən, nişanla ayrılmış məlumatları ehtiva edən mətn faylı növüdür.

Elektron cədvəl proqramında siz mikroarraydakı genlər və gen dəstləri üçün annotasiyalar əlavə etmək, silmək və ya dəyişdirmək üçün CHIP faylındakı məlumatları manipulyasiya edə bilərsiniz. Məsələn, orijinal CHIP faylına daxil olmayan genlər üçün xüsusi annotasiyalar əlavə etmək və ya müxtəlif mənbələrdən çoxlu CHIP fayllarını bir faylda birləşdirmək üçün elektron cədvəl proqramından istifadə edə bilərsiniz.

Bununla belə, qeyd etmək lazımdır ki, CHIP faylı GSEA proqramı ilə uyğunluq üçün saxlanılmalı olan xüsusi formata və struktura malikdir. Cədvəl proqramında CHIP faylının məzmununu dəyişdirsəniz, dəyişikliklərin fayl formatını və ya məzmununu GSEA təhlilinin düzgünlüyünə və ya etibarlılığına təsir edə biləcək şəkildə dəyişmədiyinə əmin olmalısınız.

## CHIP faylını necə açmaq olar?

Çünki, CHIP faylı nişanla ayrılmış məlumatları ehtiva edir, ona görə də elektron cədvəl məlumatlarına baxmaq istəyirsinizsə, onu Microsoft Excel-də aça bilərsiniz.

## İstinadlar
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
