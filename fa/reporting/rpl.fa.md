{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL - گزارش طرح صفحه",
  "keywords": [
"rpl",
"گزارش طرح بندی صفحه",
"XSD",
"SQL Server",
"گزارش نویسی"
],
  "description": "در مورد قالب جریان RPL که یک فرمت باینری داخلی است که توسط Microsoft SQL Server Reporting Services هنگام تماس با کنترل‌های بیننده استفاده می‌شود، بیاموزید.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-fal"
}
},
  "lastmod": "2021-03-02"
}

## فایل RPL چیست؟ ##

فرمت جریانی RPL (Report Page Layout) یک فرمت باینری داخلی است که توسط MS SQL Server Reporting Services هنگام تماس با کنترل‌های بیننده برای کاهش برخی از کارهای رندر از سرور به کنترل بیننده مشتری استفاده می‌شود. توسعه دهندگان می توانند طراحان گزارش سفارشی را با استفاده از RPL ایجاد کنند، که RPL و همچنین رندرهای گزارش سفارشی تولید می کنند که فایل RPL را برای نمایش گزارش ها پردازش و نمایش می دهند.

## ساختارهای RPL

یک جریان RPL شامل ساختار جریان، ساختار گزارش، ویژگی های گزارش و شمارش است. هر ساختار شامل موارد زیر است:

- تعریفی از ساختار

- گرامر تقویت شده Backus-Naur Form (ABNF) برای ساختار.

- نمودار کمی از ساختار.

- تعاریف تمام فیلدهای موجود در ساختار.

در اینجا نکات مختصری در مورد برخی از ساختارهای RPL آمده است:

### ساختار جریان
ساختار جریان از یک سری رکورد تشکیل شده است. یک رکورد حاوی صفر یا چند فیلد ساختاریافته است که حاوی طرح گزارش است.

#### RPL Stream
جریان RPL باید فقط یک رکورد گزارش داشته باشد و جریان باید یک سری رکوردهای باینری باشد که سلسله مراتب گزارش را حفظ کند.

#### رکورد
رکورد یک بلوک ساختمانی اساسی است که برای نگهداری اطلاعات مربوط به یک گزارش استفاده می شود. یک رکورد از یک دنباله بایت با طول متفاوت تشکیل شده است. یک رکورد از دو جزء تشکیل شده است:
- یک نوع رکورد
- داده های رکوردی که مخصوص آن نوع رکورد است.
نوع رکورد یک بایت است که مشخص می‌کند چه نوع اطلاعاتی توسط رکورد مشخص می‌شود و ساختار داده‌های رکورد مربوط به رکورد چگونه مرتب شده و ساختار می‌یابد. مقدار رکورد به نوع داده ای که مخصوص آن رکورد است بستگی دارد.

#### ساختارهای نوع داده ساده

جدول زیر انواع داده ها را در یک جریان RPL تعریف می کند.

|توضیحات| قالب|
---|---|
|Char|نماینده یک مقدار عددی (ترتیبی) 16 بیتی (2 بایتی).|
|Byte|نماینده یک عدد صحیح 8 بیتی (1 بایتی) بدون علامت است.|
|Int16|نماینده یک عدد صحیح امضا شده 16 بیتی (2 بایتی).|
|Single|مقدار ممیز شناور تک دقیقی 32 بیتی (4 بایتی) را نشان می دهد.|
| Decimal|نماینده یک نوع داده 128 بیتی (16 بایتی).|
|DateTime|نماینده یک رمزگذاری 64 بیتی (8 بایتی) از مقدار تاریخ و زمان است.|
|Int64|نماینده یک عدد صحیح امضا شده 64 بیتی (8 بایتی).|
|Int32|نماینده یک عدد صحیح امضا شده 32 بیتی (4 بایتی).|
|Float|مقدار ممیز شناور تک دقیقی 32 بیتی (4 بایتی) را نشان می دهد.|
|Boolean| یک مقدار منطقی منطقی 8 بیتی (1 بایتی) را نشان می دهد. مقادیر معتبر true (1) و false (0) هستند.|
|Long|نماینده یک عدد صحیح امضا شده 64 بیتی (8 بایتی).|
|String|All String values within the protocol MUST be UNICODE UTF-16. به طور پیش فرض، تمام مقادیر String با یک عدد صحیح شروع می شوند که طول رشته را مشخص می کند. مقادیر رشته در پروتکل به صورت آرایه ای از بایت ها نمایش داده می شوند. تعداد بایت ها باید برابر با تعداد کاراکترهای رشته ضرب در دو باشد.|

### ساختارهای گزارش
ساختارهای گزارش شامل تعاریف و اندازه ساختارها و عناصر مربوطه خود می باشد.

لیست زیر ساختارهای گزارش را مشخص می کند:

- گزارش
- نسخه
- گزارش ویژگی ها
- عنصر آرایه افست
- محتوای صفحه
- صفحه
- ویژگی های صفحه
- طرح بندی صفحه
- بخش
- بخش ساده
- بخش مختلط
- ویژگی های بخش
- عنصر ناحیه بدن
- عنصر هدر صفحه
- عنصر پاورقی صفحه
- عنصر بدن
- ویژگی های عنصر
- ویژگی های عنصر مشترک
- از ویژگی های عنصر مشترک استفاده کنید
- InlineSharedElement Properties
- NonSharedElementProperties
- سبک
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- محتوای ActionInfo
- عمل
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- گزارش مورد
- خط
- تصویر
- ImageDataProperties
- از ویژگی های SharedImageData استفاده کنید
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- چارت سازمانی
- پنل سنج
- نقشه
- مستطیل
- گزارش فرعی
- RichTextBox
- محتوای پاراگراف
- TextRun
- پاراگراف
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- عرض ستون ها
- ColumnInfo
- ارتفاع ردیف
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
- اندازه گیری ها
- اندازه گیری
- ReportElementEnd

### خواص
در زیر لیستی از ویژگی هایی که می توان در یک RPL Stream استفاده کرد آمده است:

- شناسه
- ColumnCount
- فاصله ستون ها
- UniqueName
- نام
- برچسب
- نشانک
- نکته ابزار
- ToggleItem
- شرح
- محل
- ConsumeContainerWhiteSpace (RPL 10.6)
- زبان
- زمان اجرا
- نویسنده
- رفرش خودکار
- ReportName
- ارتفاع صفحه
- عرض صفحه
- حاشیه بالا
- حاشیه چپ
- حاشیه حق
- حاشیه پایین
- ستون ها
- نام صفحه (RPL 10.6)
- مایل
- CanGrow
- CanShrink
- ارزش
- ToggleState
- CanSort
- وضعیت مرتب سازی
- فرمول
- IsToggleParent
- TypeCode
- ارزش اصلی
- ساده است
- ContentOffset
- StreamName
- سایز بندی
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- نام تصویر
- عرض
- قد
- رزولوشن افقی
- وضوح عمودی
- فرمت خام
- هایپرلینک
- پیوند نشانک
- DrillthroughId
- DrillthroughUrl
- رنگ لبه
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- سبک مرزی
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- پهنای مرز
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingRight
- PaddingTop
- PaddingBottom
- نوع قلم
- FontFamily
- اندازه فونت
- وزن قلم
- فرمت
- دکوراسیون متن
- TextAlign
- Vertical Align
- رنگ
- ارتفاع خط
- جهت
- حالت نوشتن
- UnicodeBiDi
- تصویر پس زمینه
- رنگ پس زمینه
- BackgroundRepeat
- NumeralLanguage
- NumeralVariant
- تقویم
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- مرحله
- MemberCellIndex
- CellItemOffset
- کول اسپن
- RowSpan
- DefIndex
- ColumnIndex
- RowIndex
- برچسب گروه
- RecursiveToggleLevel
- ListStyle
- سطح لیست
- شماره پاراگراف
- RightIndent
- LeftIndent
- حلق آویز دندانه دار
- SpaceBefore
- SpaceAfter
- خط اول
- نشانه گذاری
- ContentTop
- ContentLeft
- ContentWidth
- ارتفاع محتوا
- حالت
- CellItemState
- MemberDefState

### شمارش
لیست زیر شمارش هایی را نشان می دهد که می توانند در جریان RPL استفاده شوند:

- SortOptions
- اندازه ها
- نوع شکل
- ImageRawFormat
- FontStyles
- وزن فونت
- تزئینات متن
- TextAlignments
- ترازهای عمودی
- جهت ها
- حالت های نوشتن
- UnicodeBiDiTypes
- تقویم ها
- سبک های مرزی
- BackgroundRepeatTypes
- ListStyles
- سبک های نشانه گذاری
- TypeCode
- ارزش های دولتی
- TablixMemberStateValues
- TablixMemberDefStateValues
- اندازه RPLS





## منابع ##

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

