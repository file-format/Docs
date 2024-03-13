{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PS Fayl Formatı",
  "description": "PS fayl formatı və PS fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-azs"
}
},
  "lastmod": "2019-09-10"
}

## .PS faylı nədir? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Qısa tarix ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Apple şirkətindən Stiv Cobs onlara baş çəkdi və onlara PostScript-i lazer printerləri idarə etmək üçün uyğunlaşdırmağı tövsiyə etdi.

1985-ci ilin martında daxili PostScript tərcüməçisi olan ilk printer masa üstü nəşriyyatda (DTP) inqilab edən Apple-ın LaserWriter-i oldu. Texniki möhkəmlik və geniş yayılmış əlçatanlıq PostScript-i masaüstü və elektron nəşrlər üçün seçim dili etdi. 1990-cı ildə PostScript dili üçün tərcüməçi lazer printerlərin vacib hissəsi idi.

## Əsas xüsusiyyətləri ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Formalar:** Təbiətcə ixtiyari, həm öz-özünə keçə bilən, həm də kəsilə bilən (bölmələrdə və deşiklərdə) düz xətlərdən, əyrilərdən, kvadratlardan və kub əyrilərdən ibarət ola bilər.

**Rəsm operatorları:** istənilən qalınlıqda, rəngdə forma konturuna icazə verir, doldurur və ya hər hansı digər qrafikin kəsilməsinə imkan vermək üçün formanın kəsmə kimi çəkilməsinə icazə verir.

**Rənglər:** boz rəng, RGB, CMYK və CIE kimi müxtəlifliyə malikdir. Rənglərin xüsusi növləri fərqli xüsusiyyət kimi modelləşdirilir: ləkə rəngləri, rəng xəritələşdirilməsi, hətta kölgələmə və təkrarlanan naxışlar.

**Mətn:** qrafika ilə tam inteqrasiya olunub. Bundan əlavə, adobe təsvir modeli mətn simvollarını istənilən normal qrafik operatorları tərəfindən idarə oluna bilən qrafik formalar kimi göstərməyə imkan verir.

**Nümunə götürülmüş şəkillər**: orijinal mənbələrdən (skan edilmiş fotoşəkillər) götürülmüş və ya sintetik olaraq hazırlana bilər. PostScript dili çıxış cihazında istənilən rezolyusiyada və müxtəlif rəng modellərinə uyğun olaraq şəkilləri bərpa etmək üçün müxtəlif vasitələr təklif edir.

Ümumi təyinatlı proqramlaşdırma dili öz çərçivəsinə P-ləri daxil etməklə PostScript dilinin qrafik imkanlarından istifadə edə bilər. Rəqəmlər, simvollar, massivlər və sətirlər kimi primitiv məlumat növləri; nəzarət primitivləri, məsələn, döngələr, prosedurlar və şərtlər; və bəzi qeyri-ənənəvi xüsusiyyətlər, məsələn, lüğətlər dildə göstərilmişdir. Bu xüsusiyyətlər proqramçılara daha yüksək səviyyəli əməliyyatları çağırmaq üçün əmrlər yazmağı asanlaşdırır. Bu yüksək səviyyəli əməliyyatlar kompleks tətbiq ehtiyaclarını ödəyir. Bu cür təcrübə sabit əsas əməliyyatlar dəstindən istifadə etməkdən daha yığcam və səmərəlidir.

PostScript-də yazılmış proqramlar ASCII mənbə mətni şəklində hazırlana, ötürülə və şərh edilə bilər. Bütün dil çap edilə bilən simvollar və boşluq şəklində müəyyən edilə bilər. Bu təmsil proqramçılara dili asanlıqla yaratmaq, manipulyasiya etmək və anlamaq üçün dəstək verir. Bundan əlavə, müxtəlif kompüterlər və əməliyyat sistemləri arasında faylların saxlanması və ötürülməsi maşın müstəqilliyi sayəsində rahat saxlanılır.

Proqramın PostScript tərcüməçisinə tam şəffaf kommunikasiya yolu təmin edildiyi zaman dilin ikili kodlaşdırılmış formaları mümkündür. Sənəd mübadiləsi və ya arxiv saxlama üçün Adobe-dən PS proqramlarının ASCII təqdimatına ciddi uyğunluq tövsiyə olunur.

## Versiyalar ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Hər bir versiya mühüm strukturlaşdırma şərhlərini müəyyən edir. Encapsulated PostScript File (EPS) düzbucaqlı qrafiki təyin etmək üçün dildən istifadə edən PostScript faylının xüsusi alt növüdür. PostScript Language Reference Manual EPS-ni belə təsvir edir: Encapsulated PostScript (EPS) faylı, ehtiva edən sənədə daxil etmək üçün digər proqramlar tərəfindən idxal edilə bilən formada ən çox tək səhifəni təsvir edən PostScript proqramıdır. PostScript sənəd faylı içindəki EPS faylını əhatə edə bilər. PostScript-in əlavə istifadəsi Display PostScript (DPS) kimi qeyd olunur. DPS PostScript təsvir modelindən və dilindən istifadə edən qrafik mühərriki vasitəsilə ekranda qrafika yaradır.

## İstinadlar ##

* [PostScript Format Ailəsi](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


