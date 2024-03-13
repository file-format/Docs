{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL - Hesabat səhifəsinin tərtibatı",
  "keywords": [
"rpl",
"Hesabat Səhifəsinin Düzəlişi",
"XSD",
"SQL Server",
"hesabat vermək"
],
  "description": "İzləyici nəzarətləri ilə əlaqə qurarkən Microsoft SQL Server Reporting Services tərəfindən istifadə edilən daxili ikili format olan RPL axın formatı haqqında məlumat əldə edin.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-azl"
}
},
  "lastmod": "2021-03-02"
}

## RPL faylı nədir? ##

RPL (Report Page Layout) axın formatı MS SQL Server Reporting Services tərəfindən serverdən müştəri izləyicisi idarəetməsinə qədər göstərmə işinin bir hissəsini azaltmaq üçün tamaşaçı nəzarətləri ilə əlaqə qurarkən istifadə olunan daxili ikili formatdır. Tərtibatçılar RPL-dən istifadə edərək xüsusi hesabat tərtibatçıları yarada bilərlər ki, bu da RPL yaradacaq, həmçinin hesabatları göstərmək üçün RPL faylını emal edən və göstərən xüsusi hesabat rendererləri.

## RPL strukturları

RPL axınına axın strukturu, hesabat strukturu, hesabat xüsusiyyətləri və siyahılar daxildir. Hər bir struktura aşağıdakılar daxildir:

- Quruluşun tərifi.

- Quruluş üçün Genişləndirilmiş Backus-Naur Forması (ABNF) qrammatikası.

- Quruluşun bir az diaqramı.

- Struktur daxilində olan bütün sahələrin tərifləri.

Bəzi RPL Strukturları haqqında qısa qeydlər:

### Yayım Strukturu
Axın strukturu bir sıra qeydlərdən ibarətdir. Qeyd hesabat tərtibatını ehtiva edən sıfır və ya daha çox strukturlaşdırılmış sahələrdən ibarətdir.

#### RPL axını
RPL axınında yalnız bir Hesabat qeydi olmalıdır və axın hesabat iyerarxiyasını saxlayan bir sıra ikili qeydlər olmalıdır.

#### Qeyd
Qeyd hesabat haqqında məlumatı saxlamaq üçün istifadə olunan əsas tikinti blokudur. Qeyd müxtəlif uzunluqlu bayt ardıcıllığından ibarətdir. Qeyd iki komponentdən ibarətdir:
- Rekord növü
- Həmin qeyd növünə xas olan qeyd məlumatları.
Qeyd növü qeyd tərəfindən hansı növ məlumatın təyin olunduğunu və qeydə aid qeyd məlumatlarının strukturunun necə sıralandığını və strukturlaşdırıldığını müəyyən edən bir baytdır. Qeydin dəyəri həmin qeyd üçün xüsusi olan məlumat növündən asılıdır.

#### Sadə Məlumat Tipli Strukturlar

Aşağıdakı cədvəl RPL axınındakı məlumat növlərini müəyyən edir.

|Təsvir| format|
---|---|
|Char|16-bit (2-bayt) rəqəmli (sıra) dəyəri təmsil edir.|
|Bayt|8-bit (1-bayt) işarəsiz tam ədədi təmsil edir.|
|Int16|16-bit (2-bayt) işarəli tam ədədi təmsil edir.|
|Tək|32 bit (4 bayt) tək dəqiqlikli üzən nöqtə dəyərini təmsil edir.|
|Onluq|128-bit (16-bayt) məlumat tipini təmsil edir.|
|DateTime|Tarix və vaxt dəyərinin 64-bit (8-bayt) kodlamasını təmsil edir.|
|Int64|64-bit (8-bayt) işarəli tam ədədi təmsil edir.|
|Int32|32-bit (4-bayt) işarəli tam ədədi təmsil edir.|
|Float|32-bit (4-bayt) tək dəqiqlikli üzən nöqtə dəyərini təmsil edir.|
|Boolean|8-bit (1-bayt) məntiqi Boolean tipi dəyərini təmsil edir. Etibarlı qiymətlər doğrudur (1) və yanlışdır (0).|
|Uzun|64-bit (8-bayt) işarəli tam ədədi təmsil edir.|
|String|All String values within the protocol MUST be UNICODE UTF-16. Varsayılan olaraq, bütün String dəyərləri String uzunluğunu təyin edən tam ədədlə başlayır. Sətir dəyərləri protokolda bayt massivi kimi təqdim olunur; baytların sayı Sətirdəki simvolların sayının ikiyə vurulmasına bərabər olmalıdır.|

### Hesabat Strukturları
Hesabat strukturlarına onların müvafiq strukturlarının və elementlərinin tərifləri və ölçüləri daxildir.

Aşağıdakı siyahı hesabat strukturlarını müəyyən edir:

- Hesabat
- Versiya
- Hesabat Xüsusiyyətləri
- Ofset Massiv Elementi
- Səhifənin məzmunu
- Səhifə
- Səhifə xüsusiyyətləri
- Səhifə tərtibatı
- Bölmə
- Sadə bölmə
- Qarışıq bölmə
- Bölmə Xüsusiyyətləri
- Bədən Sahəsi Elementi
- Səhifə başlığı elementi
- Səhifənin Altbilgi Elementi
- Bədən elementi
- Element xassələri
- Paylaşılan Element Xüsusiyyətləri
- Paylaşılan Element Xüsusiyyətlərindən istifadə edin
- InlineSharedElementProperties
- NonSharedElementProperties
- Stil
- SharedStyleProperties
- NonSharedStyleProperties
- Fəaliyyət məlumatı
- ActionInfoContent
- Fəaliyyət
- ActionImageMapAreaları
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- Hesabat maddəsi
- Xətt
- Şəkil
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreaları
- ImageMapArea
- Qrafik
- Ölçmə Paneli
- Xəritə
- Düzbucaqlı
- Alt hesabat
- RichTextBox
- Paraqraf məzmunu
- TextRun
- Paraqraf
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- Sütunların genişliyi
- ColumnInfo
- Sıra hündürlükləri
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Ölçmələr
- Ölçmə
- ReportElementEnd

### Xüsusiyyətlər
Aşağıda RPL Yayımında istifadə edilə bilən xassələrin siyahısı verilmişdir:

- şəxsiyyət vəsiqəsi
- Sütun sayı
- Sütun boşluğu
- UnikalAd
- Ad
- Etiket
- Əlfəcin
- Alət İpucu
- ToggleItem
- Təsvir
- Yer
- ConsumeContainerWhiteSpace (RPL 10.6)
- Dil
- İcra vaxtı
- Müəllif
- Avtomatik yeniləmə
- Hesabatın adı
- Səhifə hündürlüyü
- Səhifə eni
- MarginTop
- Sol kənar
- Margin Right
- Margin Bottom
- Sütunlar
- Səhifə Adı (RPL 10.6)
- Maili
- CanGrow
- CanBüzül
- Dəyər
- ToggleState
- CanSort
- SortState
- Düstur
- IsToggleParent
- TypeCode
- Orijinal Dəyər
- Sadə
- ContentOffset
- Axın Adı
- Ölçü
- LinkToChild
- PrintOnFirstPage
- Bölmələr arasında çap (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Şəkil Adı
- Genişlik
- Hündürlük
- Horizontal Resolution
- Vertical Resolution
- RawFormat
- Hiperlink
- BookmarkLink
- DrillthroughId
- DrillthroughUrl
- BorderColor
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- BorderWidth
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingRight
- PaddingTop
- PaddingBottom
- FontStyle
- FontFamily
- FontSize
- Font Ağırlığı
- Format
- TextDecoration
- TextAlign
- VerticalAlign
- Rəng
- LineHeight
- İstiqamət
- Yazı rejimi
- UnicodeBiDi
- Fon Şəkli
- Fon rəngi
- BackgroundRepeat
- Rəqəm dili
- Rəqəm Variantı
- Təqvim
- ColumnHeaderRows
- Satır Başlığı Sütunları
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Səviyyə
- MemberCellIndex
- CellItemOffset
- ColSpan
- Sıra Aralığı
- DefIndex
- ColumnIndex
- RowIndex
- GroupLabel
- RecursiveToggleLevel
- ListStyle
- ListLevel
- Paraqraf nömrəsi
- Sağdan girinti
- SolGiriş
- HangingIndent
- SpaceBefore
- SpaceAfter
- Birinci xətt
- İşarələmə
- ContentTop
- MəzmunSol
- Məzmun Genişliyi
- Məzmun hündürlüyü
- Dövlət
- CellItemState
- MemberDefState

### Sadalamalar
Aşağıdakı siyahı RPL axınında istifadə edilə bilən siyahıları göstərir:

- SortOptions
- Ölçülər
- ShapeType
- ImageRawFormat
- Font Styles
- Font Ağırlıqları
- Mətn bəzəkləri
- TextAlignments
- Şaquli Alignments
- İstiqamətlər
- Yazı rejimləri
- UnicodeBiDiTypes
- Təqvimlər
- BorderStyles
- BackgroundRepeatTypes
- Siyahı üslubları
- MarkupStyles
- TypeCode
- Dövlət Dəyərləri
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSölçüsü





## İstinadlar ##

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

