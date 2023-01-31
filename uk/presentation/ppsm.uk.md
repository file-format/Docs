{
  "date" : "2019-10-11",
  "keywords" :[ "файл ppsm", "формат файлу ppsm", "що таке файл ppsm", "файл", "приклад ppsm", "розширення файлу ppsm", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPSM - файл презентації PowerPoint із підтримкою макросів",
  "description":"Дізнайтеся про формат файлу PPSM та API, які можуть створювати та відкривати файли PPSM.",
  "linktitle" : "PPSM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл PPSM?

Файли з розширенням PPSM представляють формат файлу слайд-шоу з підтримкою макросів, створений за допомогою Microsoft PowerPoint 2007 або новішої версії. Інший схожий формат файлу — [PPTM](/uk/presentation/pptm/), який відрізняється тим, що відкривається за допомогою Microsoft PowerPoint у форматі, який можна редагувати, а не як показ слайдів. Під час запуску у вигляді слайд-шоу файл PPSM показує слайди презентації з незмінним вмістом у слайд-шоу та за замовчуванням перебуває в режимі лише для читання. Файли PPSM все ще можна редагувати в Microsoft PowerPoint, відкривши їх у PowerPoint.

## Формат файлу ##

Формат файлу PPSM був представлений у PowerPoint 2007 і базується на форматі файлу OpenXML, який використовує комбінацію XML і [ZIP](/uk/стиснення/zip/) для зберігання його вмісту. Файли, згенеровані у форматі Office Open XML, — це колекція XML-файлів разом з іншими файлами, які забезпечують зв’язки між усіма складовими файлами. Ця колекція насправді є стислим архівом, який можна розпакувати, щоб переглянути його вміст. Для цього просто перейменуйте розширення файлу PPSM на zip і розпакуйте його для перегляду його вмісту.

Наступні розділи проливають світло на кожен із них.

### [Content_Types].xml ###

Це єдиний файл, який знайдено на базовому рівні, коли розпаковано zip. У ньому наведено типи вмісту для частин у пакеті. Усі посилання на XML-файли, включені в пакет, посилаються на цей XML-файл. Нижче наведено тип вмісту для частини слайда:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Якщо до пакета потрібно додати нові частини, це можна зробити, додавши нову частину та оновивши будь-які зв’язки у файлах .rels. Слід мати на увазі, що для такої зміни Content_Types.xml також потрібно оновити.

### \_rels (Папка) ###

Зв’язки між іншими частинами та ресурсами поза пакетом підтримуються частиною зв’язків. Папка Relationships містить один XML-файл, у якому зберігаються зв’язки на рівні пакета. Посилання на ключові частини файлів презентацій містяться в цьому файлі як URI. Ці URI ідентифікують тип зв’язку кожної ключової частини з пакетом. Це включає зв’язок із основним офісним документом, розміщеним як ppt/presentation.xml, та іншими частинами в docProps як основними та розширеними властивостями.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Кожна частина документа, яка є джерелом одного або кількох зв’язків, матиме власну частину зв’язків, де кожна така частина зв’язку знаходиться в підпапці \_rels цієї частини та називається шляхом додавання «.rels» до назви частина. Частина основного вмісту (presentation.xml) має власну частину зв’язків (presentation.xml.rels). Він містить зв’язки з іншими частинами вмісту, такими як slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml, а також URI для зовнішніх посилань.

#### Явний зв'язок ####

Для явного зв’язку посилання на ресурс здійснюється за допомогою атрибута Id для a<Relationship> елемент. Тобто ідентифікатор у джерелі безпосередньо відображається на ідентифікатор елемента зв’язку з явним посиланням на ціль.

Наприклад, слайд може містити таке гіперпосилання:
```
<a:hlinkClick r:id#"rId2">
```
r:id#"rId2" посилається на наступний зв’язок у частині зв’язків для слайда (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Неявний зв'язок ####

Для неявного зв’язку немає такого прямого посилання на `<Relationship> ID`. Натомість розуміється посилання.

### папка ppt ###

Це основна папка, яка містить усі відомості про вміст Презентації. За замовчуванням він має такі папки:

* \_rels
* тема
* слайди
* slideLayouts
* slideMasters

і такі файли xml:

* презентація.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Посилання ##

* [Формат файлу презентації OpenXML](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)
