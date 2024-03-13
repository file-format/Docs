{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SAFETENZORLAR - Stabil Diffuziya Modeli - SAFETENSORULAR nədir və onu necə açmaq olar?",
  "description":"SAFETENSORS Stable Diffusion Model faylı və onun necə açılacağını öyrənin.",
  "linktitle" : "SAFETENSORS",
  "menu" : {
    "docs" : {
      "identifier": "data-safetensors-az",
      "parent" : "data"
}
},
  "lastmod" : "2023-12-28"
}

## Safetensors nədir?

Safetensors Hugging Face tərəfindən hazırlanmış yeni seriallaşdırma formatıdır; bu, dərin öyrənmədə mühüm əhəmiyyət kəsb edən tensorlar adlanan böyük və mürəkkəb məlumat hissələrini saxlamaq və əldə etmək üçün xüsusi bir üsul kimidir; dərin öyrənmə çoxlu məlumatlarla işləməyi əhatə edir və bəzən bu böyük məlumat parçaları ilə məşğul olmaq çətin ola bilər; Safetensors dərin öyrənmə ilə işləyərkən bu böyük və mürəkkəb məlumat hissələrini idarə etməyi asanlaşdırmağa və daha səmərəli etməyə kömək edir.

## Safetensors faylı nədir?

Safetensors file stores algorithms to deal with tensors safely and used in machine learning model created by **Stable Diffusion** that **generates image from text description**. It is considered safe from any malicious code.

## tensor nədir?

Tensor fizika və kompüter elmləri daxil olmaqla müxtəlif sahələrdə istifadə olunan riyazi anlayışdır; verilənləri çoxölçülü massiv kimi təqdim etmək üsuludur; **dərin öyrənmə və süni intellekt** kontekstində tensorlar verilənləri təşkil etmək və manipulyasiya etmək üçün istifadə edilən fundamental məlumat strukturlarıdır; onlar vektorlar (1D massivlər), matrislər (2D massivlər) və ya daha çox ölçülərə malik ola bilərlər və öyrənmə prosesi zamanı neyron şəbəkələri tərəfindən yerinə yetirilən əməliyyatlarda həlledici rol oynayırlar; tensoru hesablamaları və məlumatların işlənməsini daha səmərəli etmək üçün xüsusi şəkildə təşkil edilmiş ədədi məlumatlar üçün konteyner kimi düşünün.

## Stabil diffuziya haqqında

Stabil Diffuziya 2022-ci ildə buraxılmış, dərin öyrənmədə diffuziya adlanan güclü texnikadan istifadə edən xüsusi növ kompüter proqramıdır; bu, süni intellektdə mövcud irəliləyiş dalğasının bir hissəsidir.

Its main job is to create detailed pictures based on written descriptions, but it can also be used for other tasks like filling in missing parts of images, creating new parts outside original image and transforming images based on written instructions. 

## SAFETENSORS faylını necə açmaq olar?

Stable Diffusion ilə SAFETENSOR faylından istifadə etmək istəyirsinizsə, onu Stable Diffusion-un modelləri axtardığı qovluğa qoymalısınız.

