{
  "date" : "2020-08-20",
  "keywords" :[ "eot ファイル", "eot ファイル形式", "eot ファイルとは", "ファイル", "eot の例", "eot ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - TrueType フォント ファイル形式",
  "description":"EOT ファイル形式と,EOT ファイルを作成して開くための API について学びます。",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .EOT オプション番号

拡張子が .eot のファイルは、ドキュメントに埋め込まれた OpenType フォントです。これらは主に Web ページなどの Web ファイルで使用されます。 Microsoft によって作成され、PowerPoint プレゼンテーション [.pps](/presentation/pps) ファイルを含む Microsoft 製品でサポートされています。このファイルは主に使用するものではなく、メインのドキュメントまたは Web ページに付随するドキュメントのようなものです。 OTF フォントと同様に、EOT はグリフの Postscript と TrueType アウトラインの両方をサポートします。 EOT ファイルは、LZ 圧縮を使用して圧縮されているため、サイズが小さくなっています。 EOT は Microsoft ツールを使用して、既存の TTF/OTF フォントからフォントを作成します。

## 簡単な歴史

EOT フォントは 2007 年に CSS3 の一部として W3C に提出されましたが、リモート システムに永続的にインストールする必要があるため、却下の理由になりました。 2008 年 3 月に再提出されましたが、W3C は最終的に当時標準化されていた [Web フォント形式](/font/woff/) (WOFF) を選択しました。

## EOT ファイル形式

EOT ファイル形式の詳細は、[W3 サブミッション ページ](https://www.w3.org/Submission/EOT/#FileFormat) で見つけることができ、このフォント形式で使用される構造を詳しく説明しています。 EOT は、フォント名とサポートされる文字に関する十分な基本情報を提供する単一の EMBEDDEDFONT 構造体で構成されます。この情報のパックにより、ユーザー エージェントは、フォントが既にマシンに存在する場合に、フォントの解凍、圧縮解除、またはインストールを回避できます。

### EMBEDDEDFONT 構造体
EMBEDDEDFONT 構造体は 3 回改訂され、改訂ごとに構造体の末尾にデータが追加されています。 EMBEDDEDFONT 構造体の最後のリビジョンは次のとおりです。

|データ型|エントリ名|説明|
---|---|---|
|unsigned long|EOTSize|構造体の合計長 (バイト単位) (文字列とフォント データを含む)|
|unsigned long|FontDataSize|OpenType フォント (FontData) の長さ (バイト単位)|
|unsigned long|Version|この形式のバージョン番号 - 0x00020002|
|unsigned long|フラグ|処理フラグ|
|byte[10]|FontPANOSE|このフォントの PANOSE 値 - http://www.microsoft.com/typography/otspec/os2.htm#pan| を参照してください。
|byte|Charset|Windows では、これは TEXTMETRIC.tmCharSet から派生します。この値は、フォントの文字セットを指定します。 DEFAULT_CHARSET (0x01) は、設定がないことを示します。 - https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica| を参照してください。
|byte|Italic|OS/2.fsSelection で ITALIC のビットが設定されている場合、値は 0x01 になります - http://www.microsoft.com/typography/otspec/os2.htm#fss| を参照してください。
|unsigned long|Weight|このフォントのウェイト値 - http://www.microsoft.com/typography/otspec/os2.htm#wtc| を参照してください。
|unsigned short|fsType|埋め込み権限に関する情報を提供するタイプ フラグ - http://www.microsoft.com/typography/otspec/os2.htm#fst|を参照してください。
|unsigned short|MagicNumber|EOT ファイルのマジック ナンバー - 0x504C。データの破損をチェックするために使用されます。|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (ビット 0 ～ 31) - http://www.microsoft.com/typography/otspec/os2.htm#ur| を参照してください。
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (ビット 32 ～ 63) - http://www.microsoft.com/typography/otspec/os2.htm#ur| を参照してください。
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (ビット 64 ～ 95) - http://www.microsoft.com/typography/otspec/os2.htm#ur| を参照してください。
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (ビット 96 ～ 127) - http://www.microsoft.com/typography/otspec/os2.htm#ur| を参照してください。
|unsigned long|CodePageRange1|CodePageRange1 (ビット 0 ～ 31) - http://www.microsoft.com/typography/otspec/os2.htm#cpr| を参照してください。
|unsigned long|CodePageRange2|CodePageRange2 (ビット 32 ～ 63) - http://www.microsoft.com/typography/otspec/os2.htm#cpr| を参照してください。
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment - http://www.microsoft.com/typography/otspec/head.htm|を参照してください。
|unsigned long|Reserved1|予約済み - 必ず 0|
|unsigned long|Reserved2|予約済み - 必ず 0|
|unsigned long|Reserved3|予約済み - 必ず 0|
|unsigned long|Reserved4|予約済み - 必ず 0|
|unsigned short|Padding1|長いアライメントを維持するためのパディング。パディング値は常に 0x0000 に設定する必要があります。|
|unsigned short|FamilyNameSize|FamilyName 配列で使用されるバイト数|
|byte|FamilyName[FamilyNameSize]|FamilyNameSize バイトの長さの UTF-16 文字の配列。これは、フォントの名前テーブルにある英語のフォント ファミリ文字列です (名前 ID = 1) - http://www.microsoft.com/typography/otspec/name.htm| を参照してください。
|unsigned short|Padding2|パディング値は常に 0x0000 に設定する必要があります。|
|unsigned short|StyleNameSize|StyleName で使用されるバイト数|
|byte|StyleName[StyleNameSize]|StyleNameSize バイトの長さの UTF-16 文字の配列。これは、フォントの名前テーブルにある英語のフォント サブファミリ文字列です (名前 ID = 2) - http://www.microsoft.com/typography/otspec/name.htm| を参照してください。
|unsigned short|Padding3|パディング値は常に 0x0000 に設定する必要があります。|
|unsigned short|VersionNameSize|VersionName で使用されるバイト数|
|bytes|VersionName[VersionNameSize]|VersionNameSize バイトの長さの UTF-16 文字の配列。これは、フォントの名前テーブルにある英語版の文字列です (名前 ID = 5) - http://www.microsoft.com/typography/otspec/name.htm| を参照してください。
|unsigned short|Padding4|パディング値は常に 0x0000 に設定する必要があります。|
|unsigned short|FullNameSize|FullName が使用するバイト数|
|byte|FullName[FullNameSize]|FullNameSize バイトの長さの UTF-16 文字の配列。これは、フォントの名前テーブルにある英語のフル ネーム文字列です (名前 ID = 4) - http://www.microsoft.com/typography/otspec/name.htm| を参照してください。
|unsigned short|Padding5|パディング値は常に 0x0000 に設定する必要があります。|
|unsigned short|RootStringSize|RootString 配列で使用されるバイト数|
|byte|RootString[RootStringSize]|RootStringSize バイトの長さの UTF-16 文字の配列。|
|unsigned long|RootStringCheckSum|RootString CheckSum 値。以下の RootStringChecksum を処理するアルゴリズムを参照してください。|
|unsigned long|EUDCCodePage|EUDC フォントのサポートに必要なコードページ値。|
|unsigned short|Padding6|パディング値は常に 0x0000 に設定する必要があります。|
|unsigned short|SignatureSize|Signature 配列で使用されるバイト数。現在予約されており、0x0000 に設定する必要があります。|
|byte|Signature[SignatureSize]|現在予約されています。 SignatureSize が 0x0000 の場合、この配列の長さはありません。|
|unsigned long|EUDCFlags|EUDC フォントの処理フラグ。一般的な値は TTEMBED_XORENCRYPTDATA および TTEMBED_TTCOMPRESSED です。|
|unsigned long|EUDCFontSize|Signature 配列で使用されるバイト数。|
|byte|EUDCFontData[EUDCFontSize]|EUDC フォント データに使用されるバイト数。 EUDCFontSize が 0x00000000 の場合、この配列の長さはありません。|
|byte|FontData[FontDataSize]|この EOT ファイルのフォント データ。データは、処理フラグによって示されるように、圧縮または XOR 暗号化される場合があります。|

## 参考文献

※【EOTファイル形式】(https://www.w3.org/Submission/EOT/)
* [埋め込み OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [フォント埋め込み](https://en.wikipedia.org/wiki/Font_embedding)

