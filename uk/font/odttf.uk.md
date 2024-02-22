{
  "date": "2023-01-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Файл ODTTF – формат файлу шрифту OpenType із запам’ятовуванням",
  "description": "Дізнайтеся про формат файлу ODTTF та API, які можуть створювати та відкривати файли ODTTF.",
  "linktitle": "ODTTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-odtt-ukf"
}
},
  "lastmod": "2023-01-13"
}

## Що таке файл ODTTF?

An ODTTF file is a font file format that is utilized by the [.XPS](/page-description-language/xps/) and Microsoft Office 2007 file formats. It contains obfuscated OpenType font that has been modified in order to make it difficult to extract the font's design information or to reverse-engineer the font's source code. ODTTF is based on the fonts used in the original documents but are not in plain format and may not be to read by third-party software to extract font data.

Ви можете відкривати файли ODTTF за допомогою Pagemark XpsViewer, Apple Safari з Pagemark XpsPlugin, Mozilla Firefox з Pagemark XpsPlugin,
NiXPS View і NiXPS Edit.

## Формат файлу ODTTF

Внутрішня структура файлового формату ODTTF невідома, оскільки вони зберігаються як вбудований обфускований формат. Їх можна вставляти в цифрові документи, наприклад .PDF або .DOCX.

## Список літератури
 * [Специфікації шрифтів OpenType від Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [Огляд TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

