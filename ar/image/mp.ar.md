{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"ملف MP - ملف LaTeX MetaPost" ,
  "description":"تعرف على تنسيق ملف MP وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات MP وفتحها." ,
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
} ,
  "lastmod" : "2022-02-23"
}

## ما هو ملف MP؟

ملف MP هو ملف صورة متجه تم إنشاؤه بواسطة لغة برمجة MetaPost لإنشاء الصور. يتم حفظ الصور المتجهة التي تم إنشاؤها باستخدام تنسيق ملف MP كملفات [EPS](/ar/ image / eps /) (Encapsulated PostScript). بالإضافة إلى ذلك ، يتم توزيع MetaPost مع إطار عمل TeX و Metafont ويمكن إنشاء ملفات MP من داخل ملفات TEX و LTX التي تستخدمها هذه التطبيقات. تحتوي ملفات MP على عبارات رسم ورسم حسابي رياضي لتقديم ملف EPS الناتج. يمكن لمحرك PDFTex استخدام EPS الذي تم إنشاؤه لإنشاء ملفات [PDF](/ar/ pdf /) مباشرة.

## تنسيق ملف MP

يتم حفظ ملفات MP على القرص كملفات ثنائية وإنشاء إخراج EPS عند تصديرها إلى تنسيق ملف صورة متجه. يتم تضمين الرسومات التي تم إنشاؤها باستخدام MetaPost في شكل منسق داخل المستندات الفنية ومنشورات المجلات التي تم إنشاؤها باستخدام LaTex.

### مثال ملف MetaPost MP

فيما يلي مثال مشار إليه من [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) ، والذي يحتوي على سهم والحرف "A" أعلى منتصف سهم.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## مراجع ##

* [MetaPost by Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Latex sample Metapost by Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

